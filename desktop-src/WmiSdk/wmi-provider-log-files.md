---
description: WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Protokolldateien für WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b485c16c44ad5ac26c51db7551baa423ad1a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863755"
---
# <a name="wmi-provider-log-files"></a>Protokolldateien für WMI-Anbieter

WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.

Diese Protokolle befinden sich möglicherweise im Verzeichnis% systemroot% \\ system32 \\ WBEM \\ Logs.

-   [Wmiprov. log](#wmiprovlog)
-   ["Ntevt. log"](#ntevtlog)
-   [Dsprovider. log](#dsproviderlog)
-   [Zugehörige Themen](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov. log

Die Datei wmiprov. log enthält Verwaltungsdaten und Ereignisse von WMI-fähigen Windows-Treibermodell-Treibern (WDM) und dem [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider). Sie liefert Warn-und Fehlerinformationen in erster Linie für die Problembehandlung und das Debuggen von Anbieter-und Client Anwendungen, von denen

Die Datei "wmiprov. log" enthält Folgendes:

-   Fehler des [WDM-Anbieters](/windows/desktop/WmiCoreProv/wdm-provider) oder des Gerätetreibers, z. b. das binäre MOF-Kompilierungsfehler oder Fehler beim Abrufen von Daten.
-   Der Status der MOF-Kompilierung für jeden der Treiber, die das MOF-Format verwenden.
-   Anbieter Erstellung und Dekonstruktion von Ereignissen.
-   PrintOut von wnode.

## <a name="ntevtlog"></a>"Ntevt. log"

Die Datei "ntevt. log" enthält Ablauf Verfolgungs Meldungen vom [Ereignisprotokoll Anbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider. log

Die Datei "dsprovider. log" enthält Ablauf Verfolgungs Informationen und Fehlermeldungen für den [Active Directory-Anbieter](/previous-versions/windows/desktop/dsprov/active-directory-provider).

In der folgenden Tabelle werden einige häufige Probleme aufgelistet, die auftreten können, und mögliche Ursachen und Lösungen.



| `Message`                                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler bei cldapclassprovider:: initializeldapprovider ADsGetObject bei RootDSE: <hresult>                                                                                                                                                                                                                    | Der ADSI-Befehl konnte nicht ausgeführt werden, um den Stammverzeichnis Dienst abzurufen. Überprüfen Sie, ob der Computer Mitglied einer Domäne ist.                                                                                                                                                                                                                                                                             |
| Cdsclassprovider:: GetObjectAsync () getclassfromcacheoradsi failed for <class name> with <hresult>                                                                                                                                                                                                  | Die Klasse, die Sie abrufen möchten, ist keine gültige Klasse im Verzeichnis. Vergewissern Sie sich, dass der Klassenname richtig ist.                                                                                                                                                                                                                                                                                                |
| Cldapinstanceprovider::P utinstanceasync () modifyexistinginstance konnte für LDAP nicht ausgeführt werden://CN = foo1, CN = Users, DC = dsprovider, DC = nttest, DC = Microsoft, DC = com mit <hresult>                                                                                                                                       | Der Anbieter konnte keine geänderte Instanz in Verzeichnisdienste schreiben. Stellen Sie sicher, dass Sie die [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Schnittstelle verwenden, um die Gruppe der Eigenschaften anzugeben, die Sie ändern. Weitere Informationen zum Verwenden der **IWbemContext** -Schnittstelle mit [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))finden Sie unter [Aktualisieren einer gesamten Instanz](updating-an-entire-instance.md). |
| Cldaphelper:: getadsiinstance ADsOpenObject ()-Fehler <class name> bei mit <hresult><br/> Cldapinstanceprovider:: GetObjectAsync: getadsiinstance ()-Fehler mit <hresult><br/> Fehler bei cldapinstanceprovider:: GetObjectAsync () für DS- \_ Benutzer. Adsipath = "<class name><br/> | Diese drei Nachrichten zeigen an, dass die Instanz, die Sie abrufen möchten, im Verzeichnisdienst nicht vorhanden ist. Überprüfen Sie, ob der **adsipath** -Wert und der Klassenname richtig sind.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Protokolldateien](wmi-log-files.md)
</dt> </dl>

 

