---
title: C-compilerdefinitionen für Proxy/Stub
description: Die Header Datei Rpcproxy. h enthält die folgenden Makro Definitionen, die bei der Erstellung verteilter com-Anwendungen möglicherweise praktisch sind. Diese Makros werden mit dem präprozessorschalter/D (oder-D) zum Zeitpunkt der C-Kompilierung aufgerufen.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- Mittel l-compilermittell, C-Compiler, Definitionen für Proxy/Stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037358"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>C-compilerdefinitionen für Proxy/Stub

Die Header Datei Rpcproxy. h enthält die folgenden Makro Definitionen, die bei der Erstellung verteilter com-Anwendungen möglicherweise praktisch sind. Diese Makros werden mit dem präprozessorschalter [**/D**](-d.md) (oder-D) zum Zeitpunkt der C-Kompilierung aufgerufen.



| MACRO                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Proxy- \_ dll registrieren                                                                                                                                                                            | Generiert die Funktionen **DllMain**, **DllRegisterServer** und **DllUnregisterServer** für die automatische Registrierung einer Proxy-dll.                                                                                       |
| Proxy- \_ CLSID =<clsid>                                                                                                                                                                      | Gibt einen Klassen Bezeichner für den Server an. Wenn dieses Makro nicht definiert ist, ist die Standard-CLSID der erste Schnittstellen Bezeichner, den der Mittell-Compiler in der IDL-Spezifikation für den Proxy-/Stubserver trifft. |
| Proxy- \_ CLSID \_ ist = {0x *8hexziffern*, 0x *4hexziffern*, 0x *4 Hexziffern*, {0x *2hexziffern*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexziffern*, 0x *2hexdigits*, 0x *2hexziffern*, 0x *2hexdigits*,}} | Gibt den Wert des Klassen Bezeichners des Servers im binären Hex-Format an.                                                                                                                                           |



 

Durch die Definition des Makros " **\_ Proxy- \_ dll registrieren** " beim Kompilieren von "dlldata. c" enthält die Proxy-/Stub-marshallingdll automatisch Standarddefinitionen für die Funktionen " **DllMain**", " **DllRegisterServer**" und " **DllUnregisterServer** ". Mit diesen Funktionen können Sie Ihre Proxy-dll selbst in der Systemregistrierung registrieren.

Dieser Standard Registrierungscode verwendet die GUID der ersten Schnittstelle, die als CLSID für die Registrierung des gesamten Proxy-/Stub-DLL-Servers gefunden wurde. COM verwendet diese CLSID später, um den kompilierten Proxy-/Stubserver für das Marshalling der Schnittstellen zu suchen und zu laden, die der Server für die Verarbeitung registriert hat. Wenn eine Anwendung einen Schnittstellen Methoden aufzurufen, der Thread-, Prozess-oder Computer Grenzen überschreitet, verwendet com den Registrierungs Eintrag der Schnittstellen Kennung, um den CLSID-Registrierungs Eintrag für den Proxy-/Stub-marshallingserver zu suchen. Anschließend wird diese CLSID verwendet, um den Server zu laden (falls er nicht bereits geladen wurde), sodass der Schnittstellen Aufrufvorgang gemarshallt werden kann.

Verwenden Sie das **Proxy- \_ CLSID** = <clsid> -Makro, wenn Sie die CLSID des Proxy-/stubservers explizit angeben möchten, anstatt die Standard-CLSID zu verwenden. Wenn Sie z. b. eine standardmäßige marshallingdll als eigenen Prozess internen com-Server entwickeln, oder wenn Sie einen eigenen **DllMain** definieren müssen, um das Anfügen von dll-Prozessen zu verarbeiten \_ \_ .

Verwenden Sie die **Proxy- \_ CLSID \_ is**= Macro anstelle der **Proxy- \_ CLSID** , um den Wert der CLSID im binären Hexadezimal Format zu definieren, das das **definierende \_ GUID** -Makro verwendet.

Beachten Sie auch, dass beim Ausführen der standardmäßigen **DllRegisterServer** -Funktion der Server bei ThreadingModel = both registriert wird.

Im folgenden Makefile-Beispiel werden die Makros **Register \_ Proxy \_ dll** und **Proxy \_ CLSID**= verwendet:

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

Weitere Informationen zur [**/D**](-d.md) -Präprozessoroption finden Sie in der C-Compilerdokumentation.

 

 




