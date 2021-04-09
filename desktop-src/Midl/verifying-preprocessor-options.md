---
title: Überprüfen von Präprozessoroptionen
description: Der mittlerer l-Compiler ruft implizit den Präprozessor auf und zeigt seine präprozessorswitches nicht an.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- Mittel l-compilermittell, überprüfen von Präprozessoroptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a047980c9f2f9dc8deffdcf85de767e4dc8705
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856323"
---
# <a name="verifying-preprocessor-options"></a>Überprüfen von Präprozessoroptionen

Der mittlerer l-Compiler ruft implizit den Präprozessor auf und zeigt seine präprozessorswitches nicht an. Wenn der [**/cpp \_**](-cpp-opt.md) -Schalter (Mittelwert) nicht vorhanden ist, besteht die präprozessorbefehlszeile aus allen [**/I**](-i.md)-, [**/D**](-d.md) -und [**/U**](-u.md) -Switches, die in der mittleren Befehlszeile verwendet werden, sowie aus **/E** -und [**/nologo**](-nologo.md) -Switches. Verwenden Sie den [**/Confirm**](-confirm.md) -Schalter des Compilers, um die an den Präprozessor weiter gegebenen Switches anzuzeigen.

Beispielsweise die folgende Zeile

**midl.exe-D \_ Win32 \_ Winnt = 0x501-robust-dntenv = 1-ID: \\ NT \\ Public \\ SDK \\ Inc-Confirm-Oicf-ERV Win32-out x86 Stub. idl**

erzeugt die folgende Ausgabe:

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




