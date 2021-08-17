---
title: Registrierungsschlüssel und Einträge für eine Onlinedatenbank vom Typ 2 Store
description: Registrierungsschlüssel und Einträge für eine Onlinedatenbank vom Typ 2 Store
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player,Registrierung
- Onlineshops, Registrierung
- 'Typ 2: Onlineshops, Registrierung'
- Registrierung,Typ 2 Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01a5494f56a4c3fa7ea91d9537f6177453a1df54f684aa73c347029574f8dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746451"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Registrierungsschlüssel und Einträge für eine Onlinedatenbank vom Typ 2 Store

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Um einen Onlineshop vom Typ 2 in Windows Media Player verfügbar zu machen, muss der Onlineshopanbieter die folgenden Registrierungsunterschlüssel und -einträge auf dem Computer des Benutzers erstellen.


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



In der obigen Registrierungssyntax sind die symbole italisch Platzhalter für Namen und GUIDs (Globally Unique Identifiers), die für den Onlineshop spezifisch sind. In der folgenden Tabelle werden diese Platzhalter beschrieben.



| Platzhalter    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Eine Zeichenfolge, die zwischen Microsoft und dem Onlineshop vereinbart wurde. Diese Zeichenfolge identifiziert den Onlineshop eindeutig. Beispiel: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | Ein bitweises **OR** eines oder mehrere Plug-In-Funktionsflags Diese Flags geben an, ob Windows Media Player bestimmte Methoden von [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) und [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)aufrufen soll. Informationen zu unterstützten Flags finden Sie in der Tabelle der Plug-In-Funktionsflags, die dieser Tabelle folgen. Beispiel: 00000037<br/> |
| *Clsid*        | Eine GUID, die der Klassenbezeichner (CLSID) für die Klasse ist, die **IWMPSubscriptionService** im Plug-In des Onlineshops implementiert. Diese GUID muss im Registrierungsformat vorliegen und mit geschweiften Klammern vervollständigen. Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *friendlyname* | Ein Benutzername für den Onlineshop. Beispiel: "Proseware Musik Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Ein Name für das Plug-In des Onlineshops. Beispiel: "Proseware-Dienst-Plug-In"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Der Name der Klasse, die **IWMPSubscriptionService** im Plug-In des Onlineshops implementiert. Beispiel: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | Der vollqualifizierte Pfad zur DLL, die das Plug-In des Onlineshops implementiert. Beispiel: "C: \\ Programme \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

In der folgenden Tabelle werden die Plug-In-Funktionsflags beschrieben.



| Flag                                    | Wert | Beschreibung                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ABONNEMENTOBERGRENZE \_ – ALLOWPLAY            | 0X1   | Windows Media Player sollte [IWMPSubscriptionService::allowPlay aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)                                                                                                                      |
| \_ \_ ABONNEMENTOBERGRENZE ALLOWCD WIEGE          | 0X2   | Windows Media Player sollte [IWMPSubscriptionService::allowCDZeichnet aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)                                                                                                                  |
| \_ \_ ABONNEMENTOBERGRENZE ALLOWPDATRANSFER     | 0X4   | Windows Media Player sollte [IWMPSubscriptionService::allowPDATransfer aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)                                                                                                        |
| HINTERGRUNDVERARBEITUNG \_ FÜR \_ ABONNEMENTOBERGRENZE | 0X8   | Windows Media Player sollte [IWMPSubscriptionService::startBackgroundProcessing aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing)                                                                                      |
| \_ \_ ABONNEMENTOBERGRENZE GERÄT VERFÜGBAR      | 0X10  | Windows Media Player sollte [IWMPSubscriptionService2::d eviceAvailable aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)                                                                                                        |
| \_ABONNEMENTOBERGRENZE \_ PREPAREFORSYNC       | 0X20  | Windows Media Player sollte [IWMPSubscriptionService2::p repareForSync aufrufen.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync)                                                                                                          |
| ABONNEMENT \_ \_ V1-OBERGRENZEN                  | 0XF   | Standard. Dieser Wert wird verwendet, wenn keiner registriert ist. Dies entspricht der Kombination von SUBSCRIPTION \_ CAP \_ ALLOWPLAY, SUBSCRIPTION \_ CAP \_ ALLOWCDILLA, SUBSCRIPTION \_ CAP \_ ALLOWPDATRANSFER und SUBSCRIPTION \_ CAP \_ BACKGROUNDPROCESSING. |



 

**Registrierungseinträge für Entwicklung und Tests**

Wenn Sie mit der Entwicklung Ihres Onlineshops beginnen, stellt Ihnen Microsoft zwei Schlüssel zur Verfügung: einen Testschlüssel und einen Produktionsschlüssel. Während der Entwicklungs- und Testphase wird Ihr Onlineshop nur dann in Windows Media Player angezeigt, wenn sich Ihr Testschlüssel oder Ihr Produktionsschlüssel in der Registrierung auf dem Computer des Benutzers befindet. Weitere Informationen zu den Test- und Produktionsschlüsseln finden Sie unter Test- und Produktionsschlüssel für einen [Typ 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).

Platzieren Sie den Test- oder Produktionsschlüssel an folgendem Speicherort in der Registrierung.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Beachten Sie, dass der Wert des Registrierungseintrags TestParameter mehrere Test- oder Produktionsschlüssel angeben kann. Angenommen, Proseware hat den Testschlüssel "1234", und Contoso hat den Testschlüssel "2345". Der folgende Registrierungseintrag gibt an, dass die Testspeicher für Proseware und Contoso in der Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**ActiveService-Registrierungseintrag**

Wenn der Benutzer einen Onlineshop aktiviert, schreibt Windows Media Player Informationen in die Registrierung, die den aktiven Onlineshop identifizieren. Windows Media Player die Informationen an folgendem Speicherort in der Registrierung auf dem Computer des Benutzers ab.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



In der obigen Registrierungssyntax ist *serviceInfo* ein Platzhalter für eine Zeichenfolge, die beschreibende Informationen zum aktiven Onlineshop enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 2-Onlineshops**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





