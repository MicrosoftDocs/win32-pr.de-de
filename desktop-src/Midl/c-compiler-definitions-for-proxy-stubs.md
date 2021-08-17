---
title: C-Compilerdefinitionen für Proxy/Stubs
description: Die Headerdatei Rpcproxy.h enthält die folgenden Makrodefinitionen, von denen jede beim Erstellen einer verteilten COM-Anwendung praktisch sein kann. Diese Makros werden mit dem Präprozessorschalter /D (oder -D) zur C-Kompilierungszeit aufgerufen.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL-Compiler MIDL, C-Compiler, Definitionen für Proxy/Stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12b9fd1e2688545137dba870816c1765102ce3593d09ea3cb062bd8250c7c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807834"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>C-Compilerdefinitionen für Proxy/Stubs

Die Headerdatei Rpcproxy.h enthält die folgenden Makrodefinitionen, von denen jede beim Erstellen einer verteilten COM-Anwendung praktisch sein kann. Diese Makros werden mit dem [**Präprozessorschalter /D**](-d.md) (oder -D) zur C-Kompilierungszeit aufgerufen.



| MACRO                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRIEREN DER \_ \_ PROXY-DLL                                                                                                                                                                            | Generiert **dllMain-,** **DllRegisterServer-** und **DllUnregisterServer-Funktionen** für die automatische Registrierung einer Proxy-DLL.                                                                                       |
| PROXY \_ CLSID=<clsid>                                                                                                                                                                      | Gibt einen Klassenbezeichner für den Server an. Wenn dieses Makro nicht definiert ist, ist die STANDARD-CLSID der erste Schnittstellenbezeichner, auf den der MIDL-Compiler in der IDL-Spezifikation für den Proxy-/Stub-Server trifft. |
| PROXY \_ CLSID \_ IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *0x 22hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}} | Gibt den Wert des Klassenbezeichners des Servers im binären Hexadezimalformat an.                                                                                                                                           |



 

Durch das Definieren des **REGISTER \_ PROXY \_ DLL-Makros** beim Kompilieren von Dlldata.c enthält Ihre Proxy-/Stub-Marshalling-DLL automatisch Standarddefinitionen für die **DllMain-,** **DllRegisterServer-** und **DllUnregisterServer-Funktionen.** Sie können diese Funktionen verwenden, um Ihre Proxy-DLL in der Systemregistrierung selbst zu registrieren.

Dieser Standardregistrierungscode verwendet die GUID der ersten Schnittstelle, die als CLSID für die Registrierung des gesamten Proxy-/Stub-DLL-Servers gefunden wurde. COM verwendet diese CLSID später, um den kompilierten Proxy-/Stubserver für das Marshalling einer der Schnittstellen zu suchen und zu laden, für die der Server registriert ist. Wenn eine Anwendung einen Schnittstellenmethode-Aufruf sendet, der Thread-, Prozess- oder Computergrenzen überschreitet, verwendet COM den Registrierungseintrag der Schnittstellen-ID, um den CLSID-Registrierungseintrag für den Proxy-/Stub-Marshallingserver zu suchen. Anschließend wird diese CLSID verwendet, um den Server zu laden (sofern er noch nicht geladen ist), damit der Schnittstellenaufruf dann gemarshallt werden kann.

Verwenden Sie **das PROXY \_ CLSID-Makro,** wenn Sie die CLSID des Proxy-/Stubservers explizit angeben möchten, anstatt sich auf die = <clsid> STANDARD-CLSID zu verlassen. Beispiel: Sie erstellen eine standardmäßige Marshalling-DLL als eigenen prozessübergreifenden COM-Server, oder sie müssen ihr eigenes **DllMain** definieren, um DLL PROCESS ATTACH zu \_ \_ verarbeiten.

Verwenden **Sie das PROXY \_ CLSID \_ IS**=-Makro anstelle von **PROXY \_ CLSID,** um den Wert der CLSID im binären Hexadezimalformat zu definieren, das vom **DEFINE \_ GUID-Makro** verwendet wird.

Beachten Sie außerdem, dass die **Standardmäßige DllRegisterServer-Funktion** den Server bei ThreadingModel=Both registriert.

Im folgenden Makefile-Beispiel werden die **Makros REGISTER \_ PROXY \_ DLL** und **PROXY \_ CLSID**= verwendet:

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

Weitere Informationen zur [**/D-Präprozessoroption**](-d.md) finden Sie in der C-Compilerdokumentation.

 

 




