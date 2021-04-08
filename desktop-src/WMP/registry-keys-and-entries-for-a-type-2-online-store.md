---
title: Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher
description: Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player Online Stores, Registrierung
- Online Stores, Registrierung
- Typ 2 Online Stores, Registrierung
- Registrierung, Typ 2 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101334"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Registrierungsschlüssel und-Einträge für einen Typ 2-Online Speicher

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Um einen Onlinespeicher vom Typ 2 in Windows Media Player verfügbar zu machen, muss der Onlinespeicher Anbieter die folgenden Registrierungs Unterschlüssel und Einträge auf dem Computer des Benutzers erstellen.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



In der vorangehenden Registrierungs Syntax sind die Symbole in kursiv Platzhalter für Namen und Global Unique Identifier (GUIDs), die für den Online Store spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Eine Zeichenfolge, die zwischen Microsoft und dem Online Store vereinbart wurde. Diese Zeichenfolge identifiziert den Online Store eindeutig. Beispiel: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | Eine bitweise **or** -Funktion von mindestens einem Plug-in-funktionsflags diese Flags geben an, ob Windows-Media Player bestimmte Methoden von [iwmpabonneptionservice](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) und [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)aufruft. Weitere Informationen zu unterstützten Flags finden Sie in der Tabelle mit den Plug-in-funktionsflags, die dieser Tabelle folgt. Beispiel: 00000037<br/> |
| *CLSID*        | Eine GUID, bei der es sich um den Klassen Bezeichner (CLSID) für die Klasse handelt, die im Plug-in des Online Stores **iwmpabonnementservice** implementiert. Diese GUID muss das Registrierungs Format aufweisen und mit den geschweiften Klammern vervollständigt werden. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *FriendlyName* | Ein Anzeige Name für den Online Shop. Beispiel: "Proseware Music Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Ein Name für das Plug-in des Online Stores. Beispiel: "Proxy Dienst-Plug-in"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Der Name der Klasse, die im Plug-in des Online Stores **iwmpabonneptionservice** implementiert. Beispiel: "cprosewareservice"<br/>                                                                                                                                                                                                                                                                |
| *ModuleName*   | Der voll qualifizierte Pfad zu der dll, die das Plug-in des Online Stores implementiert. Beispiel: "C: \\ Program Files \\ proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

In der folgenden Tabelle werden die Plug-in-funktionsflags beschrieben.



| Flag                                    | Wert | BESCHREIBUNG                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abonnement- \_ Cap \_ allowplay            | 0X1   | Der Windows-Media Player sollte [iwmpabonneptionservice:: allowplay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)aufruft.                                                                                                                      |
| Abonnement \_ Grenze \_ allowcdburn          | 0X2   | Windows Media Player sollte [iwmpabonneptionservice:: allowcdburn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)aufruft.                                                                                                                  |
| Abonnement- \_ Cap \_ allowpdatransfer     | 0X4   | Der Windows-Media Player sollte [iwmpabonneptionservice:: allowpdatransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)aufruft.                                                                                                        |
| \_ \_ backgroundprocessing für Abonnement Abdeckung | 0X8   | Windows Media Player sollte [iwmpabonneptionservice:: startbackgroundprocessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing)aufrufen.                                                                                      |
| Abonnement \_ Abdeckung \_ deviceavailable      | 0X10  | Windows Media Player muss [IWMPSubscriptionService2::d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)aufgerufen werden.                                                                                                        |
| Abonnement- \_ Cap \_ prepareforsync       | 0X20  | Windows Media Player muss [IWMPSubscriptionService2::p Analyse forsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| Abonnement \_ v1- \_ Caps                  | 0XF   | Standard. Dieser Wert wird verwendet, wenn keine registriert ist. Dies entspricht der Kombination von Abonnement- \_ Cap \_ allowplay, Abonnement Abdeckung \_ \_ allowcdburn, Abonnement Abdeckung \_ \_ allowpdatransfer und Abonnement Abdeckung \_ \_ backgroundprocessing. |



 

**Registrierungseinträge für Entwicklung und Tests**

Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei Schlüssel: einen Testschlüssel und einen Produktions Schlüssel. Während der Entwicklungs-und Testphase wird der Online Shop in Windows Media Player nur angezeigt, wenn sich der Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet. Weitere Informationen zu den Test-und Produktions Schlüsseln finden Sie unter [Test-und Produktions Schlüssel für einen Online Store vom Typ 2](test-and-production-keys-for-a-type-2-online-store.md).

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

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





