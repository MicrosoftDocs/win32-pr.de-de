---
description: WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Protokolldateien des WMI-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880010"
---
# <a name="wmi-provider-log-files"></a>Protokolldateien des WMI-Anbieters

WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.

Diese Protokolle befinden sich möglicherweise im Verzeichnis %systemroot% \\ system32 \\ wbem \\ logs.

-   [Wmiprov.log](#wmiprovlog)
-   [Ntevt.log](#ntevtlog)
-   [Dsprovider.log](#dsproviderlog)
-   [Zugehörige Themen](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov.log

Die Datei Wmiprov.log enthält Verwaltungsdaten und Ereignisse von WMI-fähigen WDM-Treibern (Windows Driver Model) und dem [WDM-Anbieter.](/windows/desktop/WmiCoreProv/wdm-provider) Er stellt Warnungs- und Fehlerinformationen in erster Linie für die Problembehandlung und das Debuggen des Anbieters und der Clientanwendungen zur Verfügung, die ihn verwenden.

Die Datei Wmiprov.log enthält:

-   Fehler vom [WDM-Anbieter oder](/windows/desktop/WmiCoreProv/wdm-provider) vom Gerätetreiber, z. B. fehler bei der binären MOF-Kompilierung oder fehler beim Abrufen von Daten.
-   Der Status der MOF-Kompilierung für jeden der Treiber, die das MOF-Format verwenden.
-   Anbieterkonstruktions- und Dekonstruktionsereignisse.
-   Ausdruck von WNODE.

## <a name="ntevtlog"></a>Ntevt.log

Die Datei Ntevt.log enthält Ablaufverfolgungsmeldungen vom [Ereignisprotokollanbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider.log

Die Datei Dsprovider.log enthält Ablaufverfolgungsinformationen und Fehlermeldungen für den [Active Directory-Anbieter](/previous-versions/windows/desktop/dsprov/active-directory-provider).

Die folgende Tabelle enthält einige häufige Probleme, die auftreten können, und bietet mögliche Ursachen und Lösungen.



| `Message`                                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider::InitializeLDAPProvider ADsGetObject on RootDSE FAILED : &lt; hresult&gt;                                                                                                                                                                                                                    | Fehler beim ADSI-Aufruf beim Versuch, den Stamm Ihrer Verzeichnisdienste zu erhalten. Stellen Sie sicher, dass Ihr Computer Mitglied einer Domäne ist.                                                                                                                                                                                                                                                                             |
| CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> with &lt; hresult&gt;                                                                                                                                                                                                  | Die Klasse, die Sie erhalten möchten, ist keine gültige Klasse im Verzeichnis. Überprüfen Sie, ob der Klassenname richtig ist.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync() ModifyExistingInstance FAILED for LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com with &lt; hresult&gt;                                                                                                                                       | Der Anbieter konnte keine geänderte Instanz in Verzeichnisdienste schreiben. Stellen Sie sicher, dass Sie die [**IWbemContext-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) verwenden, um den Satz von Eigenschaften anzugeben, die Sie ändern. Weitere Informationen zur Verwendung der **IWbemContext-Schnittstelle** mit [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))finden Sie unter [Aktualisieren einer gesamten Instanz.](updating-an-entire-instance.md) |
| CLDAPHelper::GetADSIInstance ADsOpenObject() FAILED on <class name> with &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync : GetADSIInstance() FAILED with &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync() FAILED für \_ ds-Benutzer. ADSIPath="<class name><br/> | Diese drei Meldungen geben an, dass die Instanz, die Sie erhalten möchten, im Verzeichnisdienst nicht vorhanden ist. Überprüfen Sie, **ob der ADSIPath-Wert** und der Klassenname richtig sind.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Protokolldateien](wmi-log-files.md)
</dt> </dl>

 

