---
description: WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: WMI-Anbieterprotokolldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea35a4841d86de06abe56d894e0570ef20456a78d24ce83c3fe6039cb4e2a67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030310"
---
# <a name="wmi-provider-log-files"></a>WMI-Anbieterprotokolldateien

WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.

Diese Protokolle können sich im Verzeichnis %systemroot% \\ system32 \\ wbem \\ logs befinden.

-   [Wmiprov.log](#wmiprovlog)
-   [Ntevt.log](#ntevtlog)
-   [Dsprovider.log](#dsproviderlog)
-   [Zugehörige Themen](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov.log

Die Datei Wmiprov.log enthält Verwaltungsdaten und Ereignisse von WMI-fähigen WDM-Treibern (Windows Driver Model) und dem [WDM-Anbieter](/windows/desktop/WmiCoreProv/wdm-provider). Sie stellt Warnungs- und Fehlerinformationen in erster Linie für die Problembehandlung und das Debuggen des Anbieters und der Clientanwendungen bereit, die ihn verwenden.

Die Datei Wmiprov.log enthält Folgendes:

-   Fehler des [WDM-Anbieters](/windows/desktop/WmiCoreProv/wdm-provider) oder des Gerätetreibers, z. B. Fehler bei der binären MOF-Kompilierung oder Fehler beim Abrufen von Daten.
-   Der Status der MOF-Kompilierung für jeden Treiber, der das MOF-Format verwendet.
-   Anbietererstellungs- und Dekonstruktionsereignisse.
-   Ausgabe von WNODE.

## <a name="ntevtlog"></a>Ntevt.log

Die Datei Ntevt.log enthält Ablaufverfolgungsmeldungen vom [Ereignisprotokollanbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider.log

Die Datei Dsprovider.log enthält Ablaufverfolgungsinformationen und Fehlermeldungen für den [Active Directory-Anbieter](/previous-versions/windows/desktop/dsprov/active-directory-provider).

In der folgenden Tabelle sind einige häufig auftretende Probleme aufgeführt, die mögliche Ursachen und Lösungen bieten.



| `Message`                                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider::InitializeLDAPProvider ADsGetObject on RootDSE FAILED : <hresult>                                                                                                                                                                                                                    | Fehler beim ADSI-Aufruf beim Abrufen des Stammverzeichnisses Ihrer Verzeichnisdienste. Überprüfen Sie, ob Ihr Computer Mitglied einer Domäne ist.                                                                                                                                                                                                                                                                             |
| CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> with <hresult>                                                                                                                                                                                                  | Die Klasse, die Sie abrufen möchten, ist keine gültige Klasse im Verzeichnis. Überprüfen Sie, ob der Klassenname korrekt ist.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync() ModifyExistingInstance FAILED for LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com with <hresult>                                                                                                                                       | Der Anbieter konnte keine geänderte Instanz in Verzeichnisdienste schreiben. Stellen Sie sicher, dass Sie die [**IWbemContext-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) verwenden, um den Satz von Eigenschaften anzugeben, die Sie ändern. Weitere Informationen zur Verwendung der **IWbemContext-Schnittstelle** mit [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))finden Sie unter [Aktualisieren einer gesamten Instanz.](updating-an-entire-instance.md) |
| CLDAPHelper::GetADSIInstance ADsOpenObject() FAILED on <class name> with <hresult><br/> CLDAPInstanceProvider::GetObjectAsync : GetADSIInstance() FAILED with <hresult><br/> CLDAPInstanceProvider::GetObjectAsync() FAILED für \_ ds-Benutzer. ADSIPath="<class name><br/> | Diese drei Meldungen weisen darauf hin, dass die Instanz, die Sie abrufen möchten, im Verzeichnisdienst nicht vorhanden ist. Überprüfen Sie, ob der **ADSIPath-Wert** und der Klassenname korrekt sind.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Protokolldateien](wmi-log-files.md)
</dt> </dl>

 

