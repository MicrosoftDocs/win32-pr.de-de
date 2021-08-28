---
title: C-Compilerdefinitionen für Proxys/Stubs
description: Die Headerdatei Rpcproxy.h enthält die folgenden Makrodefinitionen, von denen jede beim Erstellen einer verteilten COM-Anwendung nützlich sein kann. Diese Makros werden mit dem Präprozessorschalter /D (oder -D) zur C-Kompilierzeit aufgerufen.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL-Compiler MIDL, C-Compiler, Definitionen für Proxys/Stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b272b8b540420930366864c45e993172f5c00e67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882055"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>C-Compilerdefinitionen für Proxys/Stubs

Die Headerdatei Rpcproxy.h enthält die folgenden Makrodefinitionen, von denen jede beim Erstellen einer verteilten COM-Anwendung nützlich sein kann. Diese Makros werden mit dem [**Präprozessorschalter /D**](-d.md) (oder -D) zur C-Kompilierzeit aufgerufen.



| MACRO                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REGISTRIEREN DER \_ \_ PROXY-DLL                                                                                                                                                                            | Generiert die Funktionen **DllMain,** **DllRegisterServer** und **DllUnregisterServer** zum automatischen Registrieren einer Proxy-DLL.                                                                                       |
| PROXY \_ CLSID= &lt; clsid&gt;                                                                                                                                                                      | Gibt einen Klassenbezeichner für den Server an. Wenn dieses Makro nicht definiert ist, ist die STANDARD-CLSID der erste Schnittstellenbezeichner, den der MIDL-Compiler in der IDL-Spezifikation für den Proxy/Stub-Server findet. |
| PROXY \_ CLSID \_ IS={0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}} | Gibt den Wert des Klassenbezeichners des Servers im binären Hexadezimalformat an.                                                                                                                                           |



 

Durch Definieren des **REGISTER \_ PROXY \_ DLL-Makros** beim Kompilieren von Dlldata.c schließt ihre Proxy-/Stub-Marshalling-DLL automatisch Standarddefinitionen für die Funktionen **DllMain,** **DllRegisterServer** und **DllUnregisterServer** ein. Sie können diese Funktionen verwenden, um Ihre Proxy-DLL selbst in der Systemregistrierung zu registrieren.

Dieser Standardregistrierungscode verwendet die GUID der ersten Schnittstelle, die als CLSID zum Registrieren des gesamten Proxy-/Stub-DLL-Servers gefunden wurde. COM verwendet diese CLSID später, um den kompilierten Proxy-/Stubserver für das Marshalling einer der Schnittstellen zu suchen und zu laden, für die der Server registriert ist. Wenn eine Anwendung einen Schnittstellenmethodenaufruf vornimmt, der Thread-, Prozess- oder Computergrenzen überschreitet, verwendet COM den Registrierungseintrag des Schnittstellenbezeichners, um den CLSID-Registrierungseintrag für den Proxy-/Stub-Marshallingserver zu suchen. Anschließend wird diese CLSID verwendet, um den Server zu laden (sofern er noch nicht geladen ist), sodass der Schnittstellenaufruf gemarshallt werden kann.

Verwenden Sie das **PROXY \_ CLSID clsid-Makro,** = &lt; wenn Sie &gt; die CLSID des Proxy-/Stubservers explizit angeben möchten, anstatt sich auf die STANDARD-CLSID zu verlassen. Wenn Sie z. B. eine standardmäßige Marshalling-DLL als eigenen IN-Process-COM-Server erstellen oder eine eigene **DllMain-Datei** definieren müssen, um DLL PROCESS ATTACH zu \_ \_ verarbeiten.

Verwenden Sie **PROXY \_ CLSID \_ IS**= macro anstelle von **PROXY \_ CLSID,** um den Wert der CLSID im hexadezimalen Binärformat zu definieren, das vom **DEFINE \_ GUID-Makro** verwendet wird.

Beachten Sie außerdem, dass der Server bei Ausführung der **DllRegisterServer-Standardfunktion** mit ThreadingModel=Both registriert wird.

Im folgenden Makefilebeispiel werden die **Makros REGISTER \_ PROXY \_ DLL** und **PROXY \_ CLSID**= verwendet:

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

Weitere Informationen zur [](-d.md) /D-Präprozessoroption finden Sie in der C-Compilerdokumentation.

 

 




