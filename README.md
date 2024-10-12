# -DEV1
Ubuntu'da Python'un farklı sürümleriyle çalışırken çakışmaları engellemek veya kontrol eden sistem var mı ?

Pyenv:
Pyenv, birden fazla Python sürümünü yönetmenizi ve aralarında kolayca geçiş yapmanızı sağlayan bir araçtır. Pyenv ile her proje için farklı Python sürümleri kullanabilirsiniz1.
Kurulum için terminalde şu komutları çalıştırabilirsiniz:
curl https://pyenv.run | bash

Kurulum tamamlandıktan sonra, .bashrc veya .zshrc dosyanıza aşağıdaki satırları ekleyin:
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"

Daha sonra terminali yeniden başlatın ve pyenv install <sürüm> komutunu kullanarak istediğiniz Python sürümünü yükleyin.
Virtualenv:
Virtualenv, her proje için izole edilmiş bir Python ortamı oluşturmanıza olanak tanır. Bu sayede, projelerinizin bağımlılıkları birbirinden bağımsız olur ve çakışmalar önlenir.
Kurulum için terminalde şu komutu çalıştırabilirsiniz:
sudo apt install python3-venv

Bir sanal ortam oluşturmak için:
python3 -m venv myenv

Sanal ortamı etkinleştirmek için:
source myenv/bin/activate

Conda:
Conda, özellikle veri bilimi ve makine öğrenimi projeleri için popüler bir paket yönetim ve ortam yönetim aracıdır. Conda ile farklı Python sürümleri ve bağımlılıkları kolayca yönetebilirsiniz.
Conda’yı kurmak için Anaconda veya Miniconda yükleyicisini kullanabilirsiniz.
Yeni bir ortam oluşturmak için:
conda create --name myenv python=3.x

Ortamı etkinleştirmek için:
conda activate myenv
