---
title: Registrieren von DSP-Plug-ins
description: Registrieren von DSP-Plug-ins
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player-Plug-ins, Registrierungseinträge
- Plug-ins, Registrierungseinträge
- Plug-Ins für die digitale Signalverarbeitung, Registrierungseinträge
- DSP-Plug-ins, Registrierungseinträge
- Registrierung, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948439"
---
# <a name="registering-dsp-plug-ins"></a>Registrieren von DSP-Plug-ins

Um Ihr DSP-Plug-in in Media Player Windows verfügbar zu machen, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und Einträge erstellen.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für das DSP-Plug-in spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Pluginclsid*             | Eine GUID, die der Klassen Bezeichner für die primäre Klasse des DSP-Plug-ins ist. Dies ist die Klasse, die **imediaobject**, **ipluginenable** und möglicherweise **ISpecifyPropertyPages** implementiert. In einem Dual-Mode-Plug-in implementiert diese Klasse auch **IMF Transform** und **IMF GetService**. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *Pluginclassfriendlyname* | Ein Anzeige Name für die primäre Klasse des DSP-Plug-ins. Beispiel: "prosewaredsp Class"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *Pluginmodulename*        | Der voll qualifizierte Pfad zu der dll, die das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Threading*               | Eine Zeichenfolge, die das Threading Modell für das Plug-in angibt. Wenn das Plug-in mit Windows Media Player 11 unter Windows Vista ausgeführt wird, muss dieser Registrierungs Eintrag gleich "beide" sein. Wenn das Plug-in unter Windows XP oder älteren Betriebssystemen ausgeführt werden soll, kann dieser Registrierungs Eintrag entweder "Apartment" oder "both" lauten.                                                                                           |



 

Wenn Ihr DSP-Plug-in eine benutzerdefinierte Schnittstelle implementiert und das Plug-in unter Windows Media Player 11 unter Windows Vista ausgeführt wird, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und-Einträge erstellen.


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen, numerische Werte und global eindeutige Bezeichner (GUIDs), die für das DSP-Plug-in spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter           | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Proxystubclsid*      | Eine GUID, die der Klassen Bezeichner für die Klasse ist, die die Proxys und stubwerte für die benutzerdefinierten Schnittstellen des DSP-Plug-Ins implementiert. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *Proxystubmodulename* | Der voll qualifizierte Pfad zu der dll, die die Proxy-und Stub-Schnittstellen für das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *Custominterfakeid*   | Eine GUID, die der Schnittstellen Bezeichner für eine benutzerdefinierte Schnittstelle ist, die durch das DSP-Plug-in implementiert wird. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *Custominterfakename* | Der Name einer benutzerdefinierten Schnittstelle, die vom DSP-Plug-in implementiert wird. Beispiel: "iprosewaredsp"<br/>                                                                                                                                                                  |
| *Anzahlungsmethoden*     | Die Anzahl der Methoden, einschließlich der geerbten Methoden, die durch eine benutzerdefinierte Schnittstelle definiert werden. Beispiel: "5"<br/>                                                                                                                                                                  |



 

Wenn Ihr DSP-Plug-in eine Eigenschaften Seite bereitstellt, müssen Sie auf dem Computer des Benutzers die folgenden Registrierungs Unterschlüssel und Einträge erstellen.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für das DSP-Plug-in spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter                 | BESCHREIBUNG                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Proppageclsid*             | Eine GUID, die der Klassen Bezeichner für die Eigenschaften Seiten Klasse ist, die vom DSP-Plug-in bereitgestellt wird. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *Proppageclassfriendlyname* | Ein Anzeige Name für die Eigenschaften Seiten Klasse. Beispiel: "prosewaredsp Property Page Class"<br/>                                                                                                                                     |
| *Pluginmodulename*          | Der voll qualifizierte Pfad zu der dll, die das DSP-Plug-in implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Iwmppluginregistrar wird aufgerufen**

Zusätzlich zu den in den vorangehenden Listen und Tabellen beschriebenen Registrierungs unter Schlüsseln und Einträgen müssen Sie einige Registrierungsschlüssel und-Einträge erstellen, indem Sie [iwmpmediapluginregistrar:: wmpregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin)aufrufen. Diese Methode führt die erforderliche Registrierung aus, damit Windows Media Player Ihr Plug-in erkennen und als Option für den Benutzer präsentieren kann.

Rufen Sie in der **DllRegisterServer** -Funktion des Plug-ins den Befehl **iwmpmediapluginregistrar:: wmpregisterplayerplugin** auf, und rufen Sie in der **DllUnregisterServer** -Funktion des Plug-ins den Befehl [iwmpmediapluginregistername](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) auf. Um einen Zeiger auf eine **iwmpmediapluginregistrar** -Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und CLSID \_ wmpmediapluginregistrar als Klassen-ID übergeben. Die Konstante CLSID \_ wmpmediapluginregistrar ist in wmpservices. h definiert.

**Registrierung im DSP-Plug-in-Assistenten**

Der DSP-Plug-in-Assistent, der in der Windows SDK enthalten ist, generiert Beispielcode, der auf Active Template Library (ATL) basiert. Die **DllRegisterServer** -Funktion des Plug-Ins für das Beispiel ruft die **RegisterServer** -Funktion von ATL auf, mit der Registrierungs Unterschlüssel und Einträge gemäß zwei Registrierungs Skriptdateien im Visual Studio-Projekt erstellt werden. Die Datei " *ProjectName*. RGS" enthält das Skript zum Registrieren der Hauptklasse des Plug-ins, und die Datei " *ProjectName* PropPage. RGS" enthält das Skript zum Registrieren der Eigenschaften Seiten Klasse des Plug-ins. Die **DllRegisterServer** -Funktion des Plug-Ins für das Beispiel ruft auch **iwmppluginregistrar:: wmpregisterplayerplugin** auf.

Der DSP-Plug-in-Assistent generiert auch Code für eine ProxyStub-Komponente, bei der es sich um eine selbst registrierte DLL-Datei handelt. Der Registrierungscode für diese Datei befindet sich in "dlldata. cpp". Die Makro- **dlldata- \_ Routinen** werden so erweitert, dass Sie eine Implementierung von **DllRegisterServer** enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Iwmpmediapluginregistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





