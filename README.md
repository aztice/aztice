<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=aztice&show_icons=true&theme=radical" /><br/>
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&pause=1000&color=F75C7E&center=true&vCenter=true&width=500&lines=Hi+there,i+am+ice!" /><br/>
  <img src="https://skillicons.dev/icons?i=python,html,css,javascript,php,cs" /><br/>
  <img src="https://komarev.com/ghpvc/?username=aztice&color=blue" />
</p>

```php
<?php
// yup, there was a little bit of situation changed.
// it seems that i changed my self-introduction (?
// a new style will be shown.
// also my lover, PHP.
class Profile{
  public function __construct() {
    $funcs = [
      [$this, "greeting"],
      [$this, "interests"],
      [$this, "dreams"],
      [$this, "promotion"]
    ];
    $contents = "";
    foreach ($funcs as $fn) {
      $contents .= $fn();
    }
    $contents = $this -> docsify($contents);
    exit($contents);
  }
  public function docsify($str) : string {
    $filter = ["[+]" => "\n"];
    foreach($filter as $target => $replaced) {
      $str = str_replace($target, $replaced, $str);
    }
    return $str;
  }
  public function greeting() : string {
    return "Hi there, im ice";
  }
  public function interests() : string {
    return "### My interest [+]
 - PHP (Without frame, i hate this)
 - HTML+CSS+JS (No Vue cause i love flexible and tiny one)
 - Python (Mainly BigData)
 - SCP:SL Plugins' Development (i like to do so without rs)[+]";
  }
  public function dreams() : string {
    return "### Dreams [+]
 - Be a real Ai Researcher which never take a back seat.
 - Got a nice Offer From enterprise || maybe i will set up a start-up?
 - Find the one who can engage me doing the followings, both `bro` and `GF`[+]";
  }
  public function promotion() : string {
    return "> btw, i found a dev team when i were a primary stu., if u are interested in, feel free to reach out us via our qq group (`494512016`)";
  }
}
new Profile();
