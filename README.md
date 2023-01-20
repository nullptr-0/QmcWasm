# QmcWasm
WASM for Qmc Encryption & Decryption
- QmcWasm是从属于[音乐解锁Web]项目的Qmc类加密文件的WASM解密组件，属于[音乐解锁]系列项目之一。
- QmcWasm只提供对读入内存的加密内容进行解密的功能，并不能直接使用。如需直接使用，请转到[Web预构建版本]或[CLI预构建版本]。
- QmcWasm项目以学习和研究为初衷，并基于您同意并遵守[授权协议]各项条款在此项目上之应用的条件向您开放源代码。

## 支持的格式

- [x] QQ音乐 Legacy (.qmc*)
- [x] QQ音乐 iOS (.tm*)
- [x] QQ音乐 Modern (.m*)

## 构建与使用

QmcWasm使用[GitHub Actions]构建和发布npm包，您可以在项目的配置中使用包名`@xhacker/qmcwasm`进行引用

### 使用方法

- 您可以参照[qmc_wasm.ts]中的使用方法
- 您也可以在您的项目中直接引用[qmc_wasm.ts]文件，例如：
```
import { DecryptQmcWasm } from '@/qmc_wasm';
// 其他代码 ...
const decrypted= (await DecryptQmcWasm(cipherText, extension)).data;
```

### 自行构建

#### Linux
在此项目根目录中执行 `./build-wasm` 即可构建。构建结果将位于此项目根目录的npm子目录中。
#### Windows
在此项目根目录中执行 `build-wasm.cmd` 即可构建。构建结果将位于此项目根目录的npm子目录中。

[音乐解锁Web]: https://git.unlock-music.dev/um/web
[音乐解锁]: https://unlock-music.dev/
[Web预构建版本]: https://git.unlock-music.dev/um/-/packages/generic/web-build/
[CLI预构建版本]: https://git.unlock-music.dev/um/-/packages/generic/cli-build/
[授权协议]: https://github.com/xhacker-zzz/QmcWasm/blob/master/LICENSE.txt
[qmc_wasm.ts]: https://github.com/xhacker-zzz/QmcWasm/blob/master/qmc_wasm.ts
[GitHub Actions]: https://github.com/xhacker-zzz/QmcWasm/actions
