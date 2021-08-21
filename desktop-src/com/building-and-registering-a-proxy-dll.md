---
title: Erstellen und Registrieren einer Proxy-DLL
description: Wenn Sie das Proxy-/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die C- und H-Dateien, die MIDL generiert hat, kompiliert und verknüpft werden, um eine Proxy-DLL zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients Ihre Schnittstellen finden können.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634cb7a17551a4b7925d0be3065c71037cc1d7ae8bf28c10fcdaee74771c302e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048848"
---
# <a name="building-and-registering-a-proxy-dll"></a>Erstellen und Registrieren einer Proxy-DLL

Wenn Sie das Proxy-/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die C- und H-Dateien, die MIDL generiert hat, kompiliert und verknüpft werden, um eine Proxy-DLL zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients Ihre Schnittstellen finden können. Die MIDL-generierte Datei Dlldata.c enthält die erforderlichen Routinen und andere Informationen zum Erstellen und Registrieren einer Proxy-/Stub-DLL.

Der erste Schritt beim Erstellen der DLL besteht darin, eine Moduldefinitionsdatei für den Linker zu schreiben, wie im folgenden Beispiel gezeigt:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Alternativ können Sie diese exportierten Funktionen in der LINK-Befehlszeile Ihres Makefiles angeben.

Die exportierten Funktionen werden in rpcproxy.h deklariert, was dlldata.c enthält, und Standardimplementierungen sind Teil der RPC-Laufzeitbibliothek. COM verwendet diese Funktionen, um eine Klassenfactory zu erstellen, DLLs zu entladen (nachdem sichergestellt wurde, dass keine Objekte oder Sperren vorhanden sind), Informationen über die Proxy-DLL abzurufen und die Proxy-DLL selbst zu registrieren und die Registrierung aufzuheben. Um diese vordefinierten Funktionen nutzen zu können, müssen Sie die Option Cpreprocessor /D (oder -D) aufrufen, wenn Sie die Dateien Dlldata.c und Example \_ p.c kompilieren, wie im folgenden Makefile gezeigt:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Wenn Sie diese Präprozessordefinitionen zur Kompilierzeit nicht angeben, werden diese Funktionen nicht automatisch definiert. (Das heißt, die Makros in Rpcproxy.c werden auf nichts erweitert.) Sie müssten sie explizit in einer anderen Quelldatei definiert haben, deren Modul auch in der endgültigen Verknüpfung und Kompilierung in der C-Compilerbefehlszeile enthalten wäre.

Wenn REGISTER \_ PROXY \_ DLL definiert ist, bietet Rpcproxy.h zusätzliche Steuerung der bedingten Kompilierung mit PROXY \_ CLSID=*guid,* PROXY \_ CLSID \_ IS=*explizitem Wert von GUID* und ENTRY \_ PREFIX=*Präfixzeichenfolge*. Diese Makrodefinitionen werden im MIDL-Programmierhandbuch unter [C-Compilerdefinitionen für Proxys/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) ausführlicher beschrieben.

## <a name="manually-registering-the-proxy-dll"></a>Manuelles Registrieren der Proxy-DLL

Wenn Sie aus irgendeinem Grund die Standardroutinen für die Proxystubregistrierung nicht verwenden können, können Sie die DLL manuell registrieren, indem Sie der Systemregistrierung mithilfe von Regedt32.exe die folgenden Einträge hinzufügen.

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[C-Compilerdefinitionen für Proxys/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 
