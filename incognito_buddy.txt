function myFunction() {
if (document.f.q.value.match("hello")) {
if (confirm("Psssst, you may want to go Incognito")){
window.open("https://www.google.com/search?q=" + document.f.q.value)
}
}

};

var timeout = null;


document.f.q.onkeyup = function () {
    clearTimeout(timeout);
    timeout = setTimeout(function() {myFunction()}, 1200);
};
