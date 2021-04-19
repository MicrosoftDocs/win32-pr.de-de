---
title: Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher
description: Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player Online Stores, Registrierung
- Online Stores, Registrierung
- Typ 1 Online Stores, Registrierung
- Registrierung, Typ 1 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339868"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Registrierungsschlüssel und-Einträge für einen Typ-1-Online Speicher

Um einen Onlinespeicher vom Typ 1 in Windows Media Player verfügbar zu machen, muss der Onlinespeicher Anbieter die folgenden Registrierungs Unterschlüssel und Einträge auf dem Computer des Benutzers erstellen.


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
> Das Festlegen des Werts von dllersatz auf die leere Zeichenfolge gibt an, dass die com-Laufzeit das Plug-in des Online Stores in das standardmäßige DLL-Ersatz Zeichen (dllhost.exe) lädt.

 

In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für den Online Store spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Eine Zeichenfolge, die zwischen Microsoft und dem Online Store vereinbart wurde. Diese Zeichenfolge identifiziert den Online Store eindeutig. Beispiel: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | Eine bitweise **or** -Funktion von mindestens einem Plug-in-funktionsflags diese Flags geben an, ob Windows Media Player bestimmte Methoden von [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)aufruft. Weitere Informationen zu unterstützten Flags finden Sie in der Tabelle mit den Plug-in-funktionsflags, die dieser Tabelle folgt. Beispiel: 00000058<br/> |
| *CLSID*        | Eine GUID, bei der es sich um den Klassen Bezeichner (CLSID) für die Klasse handelt, die **iwmpcontentpartner** im Online Store-Plug-in implementiert. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *FriendlyName* | Ein Anzeige Name für den Online Shop. Beispiel: "Proseware Music Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | Eine GUID, bei der es sich um den Anwendungs Bezeichner (AppID) für das Plug-in des Online Stores handelt. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Ein Name für das Plug-in des Online Stores. Beispiel: "Proseware Content Partner Plug-in"<br/>                                                                                                                                                                                                                                   |
| *className*    | Der Name der Klasse, die **iwmpcontentpartner** im Plug-in des Online Stores implementiert. Beispiel: "cprosewarepartner"<br/>                                                                                                                                                                                              |
| *ModuleName*   | Der voll qualifizierte Pfad zu der dll, die das Plug-in des Online Stores implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Der Typ des Apartment, in dem das Plug-in ausgeführt wird. "ThreadingModel" = "Apartment" gibt an, dass das Plug-in in einem Single Thread-Apartment (STA) ausgeführt wird. "ThreadingModel" = "Free" gibt an, dass das Plug-in im Multithread-Apartment (MTA) ausgeführt wird.                                                                                     |



 

In der folgenden Tabelle werden die Plug-in-funktionsflags beschrieben.



| Flag                                    | Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ backgroundprocessing für Abonnement Abdeckung | 0x8   | Windows Media Player sollte [iwmpcontentpartner:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) anrufen, um das Plug-in zu informieren, wenn die Hintergrundverarbeitung gestartet und beendet werden soll.                                                                                                     |
| Abonnement \_ Abdeckung \_ deviceavailable      | 0x10  | Windows Media Player sollte [iwmpcontentpartner:: updatedevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice)aufrufen.                                                                                                                                                                   |
| Abonnement \_ Grenze \_ ist \_ Contentpartner   | 0x40  | Informiert Windows Media Player, dass das Plug-in die **iwmpcontentpartner** -Schnittstelle implementiert. Dieses Flag muss von allen Online Store-Plug-ins vom Typ 1 festgelegt werden.                                                                                                                         |
| Abonnement- \_ Cap- \_ altanmeldung             | 0x80  | Informiert Windows Media Player, dass das Plug-in eine Alternative Anmeldung unterstützt. Wenn das Plug-in eine Alternative Anmeldung unterstützt, ruft Windows Media Player die Alternative Anmelde-URL und Beschriftung durch Aufrufen von [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)ab. |



 

**Registrierungseinträge für Entwicklung und Tests**

Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei Schlüssel: einen Testschlüssel und einen Produktions Schlüssel. Während der Entwicklungs-und Testphase wird der Online Shop in Windows Media Player nur angezeigt, wenn sich der Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet. Weitere Informationen zu Test-und Produktions Schlüsseln finden Sie unter [Test-und Produktions Schlüssel für einen Online Store vom Typ 1](test-and-production-keys-for-a-type-1-online-store.md).

Platzieren Sie den Test-oder Produktions Schlüssel an folgendem Speicherort in der Registrierung.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Beachten Sie, dass der Wert des Registrierungs Eintrags Testparameter mehrere Test-oder Produktions Schlüssel angeben kann. Nehmen wir beispielsweise an, dass Proseware einen Testschlüssel mit dem Wert "1234" hat und dass die Datei "" den Testschlüssel "2345" hat. Der folgende Registrierungs Eintrag gibt an, dass die Test Speicher für Proseware und Microsoft Configuration Manager in der Windows-Media Player angezeigt werden.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**ActiveService-Registrierungs Eintrag**

Wenn der Benutzer einen Online Shop aktiviert, schreibt Windows Media Player Informationen in die Registrierung, die den aktiven Online Store identifiziert. In Windows Media Player werden die Informationen an folgendem Speicherort in der Registrierung auf dem Computer des Benutzers abgelegt.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



In der vorangehenden Registrierungs Syntax ist *serviceInfo* ein Platzhalter für eine Zeichenfolge, die beschreibende Informationen zum aktiven Online Store enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 1-Onlineshops**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





