# Cooolis-ms

[Wiki Documentation](https://github.com/Rvn0xsy/Cooolis-ms/wiki)

--------

![README](./Pic/view-1.png)


`Cooolis-ms`This is a code execution tool incorporating the Metasploit Payload Loader, Cobalt Strike External C2 Loader, and Reflective DLL injection. Its purpose is to evade static detection of certain code we intend to execute that contains detectable signatures, enabling red team personnel to transition more efficiently from web container environments to C2 environments for further operations.

### How do I download it?

- You can clone the repository directly from GitHub to obtain the source code：`git clone https://github.com/Rvn0xsy/Cooolis-ms`

### Basic Description

1. `Cooolis-ms`was based on[Metasploit API 文档](https://docs.rapid7.com/metasploit/standard-api-methods-reference/)The functionality of the RPC service client has been implemented, enabling`Cooolis-ms`The server can send arbitrary payloads.，Let`Cooolis-ms`The flexibility has been enhanced.
2. `Cooolis-ms`draws upon[MemoryModule](https://github.com/fancycode/MemoryModule)Achieved PE loading, enabling`Cooolis-ms`The execution characteristics are reduced, lowering the detection and elimination probability.
3. `Cooolis-ms`draws upon[ReflectiveDLLInjection](https://github.com/stephenfewer/ReflectiveDLLInjection)Achieved the loading, execution, and injection of reflective DLLs, enabling`Cooolis-ms`The execution characteristics are reduced, lowering the detection and elimination probability.
4. `Cooolis-ms`was based on[External C2 (Third-party Command and Control)](https://cobaltstrike.com/help-externalc2)Achieved basic External C2 execution, enabling`Cooolis-ms`The execution characteristics are reduced, lowering the detection and elimination probability.
5. `Cooolis-ms`Additionally, it considers automatically loading files stored on Aliyun OSS servers as executable code into memory for execution, enabling`Cooolis-ms`The flexibility has been enhanced.

### Instructions for Use

At present`Cooolis-ms`It has the following subcommands:

```
[~\Documents\Cooolis-ms\Cooolis-ms-Loader\Release]> .\Cooolis-ms.exe -h
Version v1.2.6
Usage: C:\Users\Administrator\Documents\Cooolis-ms\Cooolis-ms-Loader\Release\Cooolis-ms.exe [OPTIONS] SUBCOMMAND

Options:
  -h,--help                   Print this help message and exit

Subcommands:
  metasploit                  Metasploit RPC Loader
  cobaltstrike                Cobalt Strike External C2 Loader
  reflective                  Reflective DLL injection
  shellcode                   Shellcode Loader
```

By adding after the subcommand`-h/--help`Retrieve detailed parameters for the corresponding subcommand:

```
[~\Documents\Cooolis-ms\Cooolis-ms-Loader\Release]> .\Cooolis-ms.exe metasploit -h
Metasploit RPC Loader
Usage: C:\Users\Administrator\Documents\Cooolis-ms\Cooolis-ms-Loader\Release\Cooolis-ms.exe metasploit [OPTIONS]

Options:
  -h,--help                   Print this help message and exit
  -p,--payload TEXT=windows/meterpreter/reverse_tcp
                              Payload Name, e.g. windows/meterpreter/reverse_tcp
  -o,--options TEXT           Payload options, e.g. LHOST=1.1.1.1,LPORT=8866
  -P,--PORT UINT:INT in [1 - 65535]=8899 REQUIRED
                              RPC Server Port
  -H,--HOST TEXT:IPV4 REQUIRED
                              RPC Server Host
```

### Detailed Explanation of Subcommand Usage

- [metasploit](https://github.com/Cooolis-ms/wiki/module-metasploit)
- [cobaltstrike](https://github.com/Cooolis-ms/wiki/module-cobaltstrike)
- [reflective](https://github.com/Cooolis-ms/wiki/module-reflective)
- [shellcode](https://github.com/Cooolis-ms/wiki/module-shellcode)


### Learning and Extending

You can refer to this resource to create your own great projects.

- [Static Malicious Code Escape（Lesson One）](https://payloads.online/archivers/2019-11-10/1)
- [Static Malicious Code Escape（Lesson Two）](https://payloads.online/archivers/2019-11-10/2)
- [Static Malicious Code Escape（Lesson Tree）](https://payloads.online/archivers/2019-11-10/3)
- [Static Malicious Code Escape（Lesson Four）](https://payloads.online/archivers/2019-11-10/4)
- [Static Malicious Code Escape（Lesson Five）](https://payloads.online/archivers/2019-11-10/5)
- [Static Malicious Code Escape（Lesson Six）](https://payloads.online/archivers/2020-01-02/1)
- [Static Malicious Code Escape（Lesson Seven）](https://payloads.online/archivers/2020-10-23/1)
- [Static Malicious Code Escape（Lesson Eight）](https://payloads.online/archivers/2020-11-29/1)
- [Static Malicious Code Escape（Lesson Nine）](https://payloads.online/archivers/2020-11-29/2)


## About Other

If you like this project, please give it a Star～


## issue

I would like to submit a suggestion or question

## LICENSE

GNU General Public License v3.0

