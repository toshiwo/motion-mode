# motion-mode
## DESCRIPTION
motion-mode provide the simple dictionary code-completion on RubyMotion enviroment by [auto-complete-mode](http://github.com/auto-complete/auto-complete).  
motion-mode detect which your project is a RubyMotion project or not.  
So, when you open a source file in RubyMotion projects, the emacs open it by motion-mode.  
But, when you open noraml ruby's source file (*.rb), the emacs open it by ruby-mode.  

## USAGE
```sh
$ git clone https://github.com/ainame/motion-mode.git
$ cd motion-mode
$ find /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS6.1.sdk/System/Library/Frameworks -name "*.h" | xargs ruby make_dict.rb
$ cp ./motion-mode ~/.emacs.d/ac-dict
$ cp ./motion-mode.el ~/.emacs.d/path/to/elisp/
$ emacs ~/.emacs.d/init.el # add following setting
(require 'motion-mode)
(add-hook 'ruby-mode-hook 'motion-upgrade-major-mode-if-motion-project)
(add-to-list 'ac-modes 'motion-mode)
(add-to-list 'ac-sources 'ac-source-dictionary)
(define-key motion-mode-map (kbd "C-c C-c") 'motion-execute-rake)
```
## SEE ALSO
make_dict.rb cite from [roupam/yasobjc](https://github.com/roupam/yasobjc).
