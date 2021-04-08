---
title: Entwickeln und Registrieren einer Proxy-dll
description: Wenn Sie Proxy/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die. c-und. h-Dateien, die von der mittleren l generiert werden, kompiliert und verknüpft werden, um eine Proxy-dll zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients ihre Schnittstellen suchen können.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730513"
---
# <a name="building-and-registering-a-proxy-dll"></a>Entwickeln und Registrieren einer Proxy-dll

Wenn Sie Proxy/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die. c-und. h-Dateien, die von der mittleren l generiert werden, kompiliert und verknüpft werden, um eine Proxy-dll zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients ihre Schnittstellen suchen können. Die von der Mitte generierte Datei "dlldata. c" enthält die erforderlichen Routinen und weitere Informationen zum Erstellen und Registrieren einer Proxy-/Stub-DLL.

Der erste Schritt beim Erstellen der dll besteht darin, eine Modul Definitionsdatei für den Linker zu schreiben, wie im folgenden Beispiel gezeigt:

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Alternativ können Sie diese exportierten Funktionen in der Link Befehlszeile Ihres Makefile angeben.

Die exportierten Funktionen werden in RpcProxy. h deklariert, was dlldata. c umfasst, und Standard Implementierungen sind Teil der RPC-Lauf Zeit Bibliothek. COM verwendet diese Funktionen zum Erstellen einer Klassenfactory, zum Entladen von DLLs (nachdem sichergestellt ist, dass keine Objekte oder Sperren vorhanden sind), zum Abrufen von Informationen über die Proxy-dll und zum selbst registrieren und Aufheben der Registrierung der Proxy-dll. Um diese vordefinierten Funktionen nutzen zu können, müssen Sie die Option "cpreprocessor/D (oder-D)" aufrufen, wenn Sie die Dateien "dlldata. c" und "example \_ p. c" kompilieren, wie im folgenden Makefile gezeigt:

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
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Wenn Sie diese Präprozessordefinitionen nicht zum Zeitpunkt der Kompilierung angeben, werden diese Funktionen nicht automatisch definiert. (Das heißt, die Makros in RpcProxy. c werden zu Nothing erweitert.) Sie müssten diese explizit in einer anderen Quelldatei definieren, deren Modul auch in der endgültigen Verknüpfung und Kompilierung in der C-Compilerbefehlszeile enthalten wäre.

Wenn \_ Proxy- \_ dll registrieren definiert ist, bietet RpcProxy. h zusätzliche bedingte Kompilierungs Steuerung mit Proxy \_ CLSID =*GUID*, Proxy \_ CLSID \_ ist =*expliziter Wert der GUID* und Eintrags \_ Präfix =*Präfix Zeichenfolge*. Diese Makro Definitionen werden ausführlicher in [C-compilerdefinitionen für Proxy/Stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) im Programmier Handbuch für Mittel l beschrieben.

## <a name="manually-registering-the-proxy-dll"></a>Manuelles Registrieren der Proxy-dll

Wenn Sie die standardmäßigen ProxyStub-Registrierungs Routinen aus irgendeinem Grund nicht verwenden können, können Sie die dll manuell registrieren, indem Sie die folgenden Einträge in der Systemregistrierung mithilfe von Regedt32.exe hinzufügen.

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

[C-compilerdefinitionen für Proxy/Stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 