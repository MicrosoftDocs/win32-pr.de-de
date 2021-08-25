---
title: Registrierungsschlüssel und -einträge für eine Online-Store vom Typ 1
description: Registrierungsschlüssel und -einträge für eine Online-Store vom Typ 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player Onlineshops,Registrierung
- Onlineshops, Registrierung
- Geben Sie 1 Onlineshops ein, Registrierung
- Registrierung, Geben Sie 1 Onlineshops ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e42b1b75b64a8736c1491ccc058fe5548d78808ba51e142b3272d17d3c0eba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861530"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Registrierungsschlüssel und -einträge für eine Online-Store vom Typ 1

Um einen Onlineshop vom Typ 1 in Windows Media Player verfügbar zu machen, muss der Onlineshopanbieter die folgenden Registrierungsunterschlüssel und -einträge auf dem Computer des Benutzers erstellen.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> Das Festlegen des Werts von DllSurrogate auf die leere Zeichenfolge gibt an, dass die COM-Runtime das Plug-In des Onlineshops in das Standardmäßige DLL-Ersatzzeichen dllhost.exe lädt.

 

In der obigen Registrierungssyntax sind die symbole in italic Platzhalter für Namen und GUIDs (Globally Unique Identifiers), die für den Onlineshop spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Eine Zeichenfolge, die zwischen Microsoft und dem Onlineshop vereinbart wurde. Diese Zeichenfolge identifiziert den Onlineshop eindeutig. Beispiel: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | Ein bitweises **OR** eines oder mehrerer Plug-In-Funktionsflags Diese Flags geben an, ob Windows Media Player bestimmte Methoden von [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)aufrufen sollen. Informationen zu unterstützten Flags finden Sie in der Tabelle der Plug-In-Funktionsflags, die auf diese Tabelle folgen. Beispiel: 00000058<br/> |
| *Clsid*        | Eine GUID, die der Klassenbezeichner (CLSID) für die Klasse ist, die **IWMPContentPartner** im Plug-In des Onlineshops implementiert. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/>                                                                  |
| *friendlyname* | Ein Anzeigename für den Onlineshop. Beispiel: "Proseware Musik Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | Eine GUID, die die Anwendungs-ID (AppID) für das Plug-In des Onlineshops ist. Diese GUID muss das Registrierungsformat aufweisen und die geschweiften Klammern aufweisen. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Ein Name für das Plug-In des Onlineshops. Beispiel: "Proseware Content Partner Plug-In"<br/>                                                                                                                                                                                                                                   |
| *className*    | Der Name der Klasse, die **IWMPContentpartner** im Plug-In des Onlineshops implementiert. Beispiel: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | Der vollqualifizierte Pfad zur DLL, die das Plug-In des Onlineshops implementiert. Beispiel: "C: \\ Programme \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Der Typ des Apartments, in dem das Plug-In ausgeführt wird. "ThreadingModel"="Apartment" gibt an, dass das Plug-In in einem Singlethread-Apartment (STA) ausgeführt wird. "ThreadingModel"="Free" gibt an, dass das Plug-In im Multithread-Apartment (MTA) ausgeführt wird.                                                                                     |



 

In der folgenden Tabelle werden die Plug-In-Funktionsflags beschrieben.



| Flag                                    | Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ ABONNEMENTOBERGRENZE – HINTERGRUNDVERARBEITUNG | 0x8   | Windows Media Player sollte [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) aufrufen, um das Plug-In darüber zu informieren, wann die Hintergrundverarbeitung gestartet und beendet werden soll.                                                                                                     |
| \_ \_ ABONNEMENTOBERGRENZE GERÄT VERFÜGBAR      | 0x10  | Windows Media Player sollte [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice)aufrufen.                                                                                                                                                                   |
| \_ABONNEMENTOBERGRENZE \_ IST \_ CONTENTPARTNER   | 0x40  | Informiert Windows Media Player, dass das Plug-In die **IWMPContentPartner-Schnittstelle** implementiert. Für alle Onlineshop-Plug-Ins vom Typ 1 muss dieses Flag festgelegt werden.                                                                                                                         |
| \_ABONNEMENTOBERGRENZE \_ ALTLOGIN             | 0x80  | Informiert Windows Media Player, dass das Plug-In eine alternative Anmeldung unterstützt. Wenn das Plug-In eine alternative Anmeldung unterstützt, ruft Windows Media Player die alternative Anmelde-URL und beschriftung ab, indem [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)aufgerufen wird. |



 

**Registrierungseinträge für Entwicklung und Tests**

Wenn Sie mit der Entwicklung Ihres Onlineshops beginnen, stellt Microsoft Ihnen zwei Schlüssel zur Verfügung: einen Testschlüssel und einen Produktionsschlüssel. Während der Entwicklungs- und Testphase wird Ihr Onlineshop nur dann in Windows Media Player angezeigt, wenn sich Ihr Testschlüssel oder Ihr Produktionsschlüssel in der Registrierung auf dem Computer des Benutzers befindet. Weitere Informationen zu den Test- und Produktionsschlüsseln finden Sie unter [Test- und Produktionsschlüssel für einen Typ 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).

Platzieren Sie Ihren Test- oder Produktionsschlüssel an folgendem Speicherort in der Registrierung.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Beachten Sie, dass der Wert des Registrierungseintrags TestParameter mehrere Test- oder Produktionsschlüssel angeben kann. Angenommen, Proseware hat den Testschlüssel "1234" und Contoso den Testschlüssel "2345". Der folgende Registrierungseintrag gibt an, dass die Testspeicher für Proseware und Contoso in Windows Media Player angezeigt werden.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**ActiveService-Registrierungseintrag**

Wenn der Benutzer einen Onlineshop aktiviert, schreibt Windows Media Player Informationen in die Registrierung, die den aktiven Onlineshop identifizieren. Windows Media Player platziert die Informationen am folgenden Speicherort in der Registrierung auf dem Computer des Benutzers.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



In der obigen Registrierungssyntax ist *serviceInfo* ein Platzhalter für eine Zeichenfolge, die beschreibende Informationen zum aktiven Onlineshop enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 1-Onlineshops**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





