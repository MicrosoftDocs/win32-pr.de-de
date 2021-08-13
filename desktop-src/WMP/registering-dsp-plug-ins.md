---
title: Registrieren von DSP-Plug-Ins
description: Registrieren von DSP-Plug-Ins
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player-Plug-Ins, Registrierungseinträge
- Plug-Ins, Registrierungseinträge
- Plug-Ins für die digitale Signalverarbeitung, Registrierungseinträge
- DSP-Plug-Ins, Registrierungseinträge
- Registrierung, DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7671c59dfe64094afbc5f0537bcae237b3812699f4db1a06519054b14ef295f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570380"
---
# <a name="registering-dsp-plug-ins"></a>Registrieren von DSP-Plug-Ins

Um Ihr DSP-Plug-In in Windows Media Player verfügbar zu machen, müssen Sie die folgenden Registrierungsunterschlüssel und -einträge auf dem Computer des Benutzers erstellen.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



In der obigen Registrierungssyntax sind die italischen Symbole Platzhalter für Namen und GUIDs (Globally Unique Identifiers), die für das DSP-Plug-In spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Plug-InClsid*             | Eine GUID, die der Klassenbezeichner für die primäre Klasse des DSP-Plug-Ins ist. Dies ist die Klasse, die **IMediaObject,** **IPluginEnable** und möglicherweise **ISpecifyPropertyPages** implementiert. In einem Dual-Mode-Plug-In implementiert diese Klasse auch **DIE** NSDTRANSTRANSFORM und **DIE NSGET-Funktion**. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Ein Anzeigename für die primäre Klasse des DSP-Plug-Ins. Beispiel: "ProsewareDSP-Klasse"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Der vollqualifizierte Pfad zur DLL, die das DSP-Plug-In implementiert. Beispiel: "C: \\ Programme \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Threading*               | Eine Zeichenfolge, die das Threadingmodell für das Plug-In angibt. Wenn das Plug-In mit Windows Media Player 11 auf Windows Vista ausgeführt wird, muss dieser Registrierungseintrag gleich "Both" sein. Wenn das Plug-In auf Windows XP oder älteren Betriebssystemen ausgeführt wird, kann dieser Registrierungseintrag entweder gleich "Apartment" oder "Both" sein.                                                                                           |



 

Wenn Ihr DSP-Plug-In eine benutzerdefinierte Schnittstelle implementiert und ihr Plug-In in Windows Media Player 11 auf Windows Vista ausgeführt wird, müssen Sie die folgenden Registrierungsunterschlüssel und -einträge auf dem Computer des Benutzers erstellen.


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



In der obigen Registrierungssyntax sind die italischen Symbole Platzhalter für Namen, numerische Werte und GUIDs (Globally Unique Identifiers), die spezifisch für das DSP-Plug-In sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter           | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | Eine GUID, die der Klassenbezeichner für die Klasse ist, die die Proxys und Stubs für die benutzerdefinierten Schnittstellen des DSP-Plug-Ins implementiert. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | Der vollqualifizierte Pfad zur DLL, die die Proxy- und Stubschnittstellen für das DSP-Plug-In implementiert. Beispiel: "C: \\ Programme \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | Eine GUID, die der Schnittstellenbezeichner für eine benutzerdefinierte Schnittstelle ist, die vom DSP-Plug-In implementiert wird. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | Der Name einer benutzerdefinierten Schnittstelle, die vom DSP-Plug-In implementiert wird. Beispiel: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | Die Anzahl von Methoden, einschließlich geerbter Methoden, die von einer benutzerdefinierten Schnittstelle definiert werden. Beispiel: "5"<br/>                                                                                                                                                                  |



 

Wenn ihr DSP-Plug-In eine Eigenschaftenseite bereitstellt, müssen Sie die folgenden Registrierungsunterschlüssel und -einträge auf dem Computer des Benutzers erstellen.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



In der obigen Registrierungssyntax sind die italischen Symbole Platzhalter für Namen und GUIDs (Globally Unique Identifiers), die für das DSP-Plug-In spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter                 | BESCHREIBUNG                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | Eine GUID, die der Klassenbezeichner für die Eigenschaftenseitenklasse ist, die vom DSP-Plug-In bereitgestellt wird. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen.<br/> Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Ein Anzeigename für die Eigenschaftenseitenklasse. Beispiel: "ProsewareDSP-Eigenschaftenseitenklasse"<br/>                                                                                                                                     |
| *PluginModuleName*          | Der vollqualifizierte Pfad zur DLL, die das DSP-Plug-In implementiert. Beispiel: "C: \\ Programme \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Aufrufen von IWMPPluginRegistrar**

Zusätzlich zu den Registrierungsunterschlüsseln und -einträgen, die in den vorherigen Listen und Tabellen beschrieben sind, müssen Sie einige Registrierungsschlüssel und -einträge erstellen, indem Sie [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin)aufrufen. Diese Methode führt die erforderliche Registrierung aus, damit Windows Media Player Ihr Plug-In erkennen und dem Benutzer als Option zur Verfügung stellen kann.

Rufen Sie **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in der **DllRegisterServer-Funktion** Ihres Plug-Ins auf, und rufen Sie [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in der **DllUnregisterServer-Funktion** Ihres Plug-Ins auf. Um einen Zeiger auf eine **IWMPMediaPluginRegistrar-Schnittstelle** abzurufen, rufen Sie **CoCreateInstance** auf, und übergeben Sie CLSID \_ WMPMediaPluginRegistrar als Klassen-ID. Die konstante CLSID \_ WMPMediaPluginRegistrar wird in wmpservices.h definiert.

**Registrierung im DSP-Plug-In-Assistenten**

Der DSP-Plug-In-Assistent, der im Windows SDK enthalten ist, generiert Beispielcode, der auf Active Template Library (ATL) basiert. Die **DllRegisterServer-Funktion** des Beispiel-Plug-Ins ruft die **RegisterServer-Funktion** von ATL auf, die Registrierungsunterschlüssel und -einträge gemäß zwei Registrierungsskriptdateien im projekt Visual Studio erstellt. Die Datei *ProjectName*.rgs enthält das Skript zum Registrieren der Hauptklasse des Plug-Ins, und die Datei *ProjectName* PropPage.rgs enthält das Skript zum Registrieren der Eigenschaftenseitenklasse des Plug-Ins. Die **DllRegisterServer-Funktion** des Beispiel-Plug-Ins ruft auch **IWMPPluginRegistrar::WMPRegisterPlayerPlugin** auf.

Der DSP-Plug-In-Assistent generiert auch Code für eine Proxystubkomponente, bei der es sich um eine selbst registrierende .dll-Datei handelt. Der Registrierungscode für diese Datei befindet sich in dlldata.cpp. Das Makro **DLLDATA \_ ROUTINES** wird erweitert, um eine Implementierung von **DllRegisterServer** einzuschließt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





