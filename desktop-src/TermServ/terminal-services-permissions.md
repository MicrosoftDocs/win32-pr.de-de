---
title: Remotedesktopdienste Berechtigungen
description: Sie können die für Remotedesktopdienste bereitgestellten Berechtigungen verwenden, um zu steuern, wie Benutzer und Gruppen auf den Server zugreifen.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1358a4360889bc013beefcee4e029f3572c9c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390434"
---
# <a name="remote-desktop-services-permissions"></a>Remotedesktopdienste Berechtigungen

Sie können die für Remotedesktopdienste bereitgestellten Berechtigungen verwenden, um zu steuern, wie Benutzer und Gruppen auf den Server zugreifen. Eine Beschreibung der Standard Berechtigungs Typen und ausführlichere Informationen zu Remotedesktopdienste Berechtigungen im Allgemeinen finden Sie in der Dokumentation, die das Verwaltungs Tool für die Remotedesktopdienste Konfiguration begleitet. Weitere Informationen zum Konfigurieren dieser Berechtigungen für Windows Server 2008 finden Sie unter [Konfigurieren von Berechtigungen für Remotedesktopdienste-Verbindungen](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

Im folgenden finden Sie eine Liste der Berechtigungen, die Sie festlegen können, sowie die Aufgaben, die die Berechtigungen zulassen.



| Wert                        | Bedeutung                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrage Informationen<br/> | Fragen Sie Sitzungen und Server nach Informationen ab.<br/>                                                                                                                |
| Festlegen von Informationen<br/>   | Verbindungs Eigenschaften konfigurieren.<br/>                                                                                                                           |
| Remotesteuerung<br/>    | Anzeigen oder aktives Steuern der Sitzung eines anderen Benutzers.<br/>                                                                                                           |
| Anmelden<br/>             | Melden Sie sich bei einer Sitzung auf dem Server an.<br/>                                                                                                                         |
| Abmelden (Logoff)<br/>            | Abmelden eines Benutzers von einer Sitzung. Beachten Sie, dass die Protokollierung eines Benutzers ohne Warnung zu einem Datenverlust auf dem Client führen kann.<br/>                                  |
| `Message`<br/>           | Sendet eine Nachricht an die Sitzungen eines anderen Benutzers.<br/>                                                                                                                 |
| Verbinden<br/>           | Verbindung mit einer anderen Sitzung herstellen.<br/>                                                                                                                                |
| Trennen<br/>        | Trennen Sie eine Sitzung.<br/>                                                                                                                                      |
| Virtuelle Kanäle<br/>  | Verwenden Sie virtuelle Kanäle. Beachten Sie, dass durch das Ausschalten von virtuellen Kanälen einige Remotedesktopdienste Features wie Zwischenablage und Drucker Umleitung deaktiviert werden.<br/> |
| Reset<br/>             | Beenden Sie eine Sitzung. Beachten Sie, dass das Beenden einer Sitzung ohne Warnung dazu führen kann, dass Daten auf dem Client verloren gehen.<br/>                                                    |



 

Die Anmelde Berechtigung ist erforderlich, damit sich ein Benutzer bei einer neuen Remotedesktopdienste Sitzung anmelden kann. Alle anderen Remotedesktopdienste Berechtigungen gelten für die Steuerung der Remotedesktopdienste Sitzung eines anderen Benutzers.

Remotedesktopdienste Berechtigungen können für einzelne Benutzer oder Gruppen erteilt oder festgelegt werden. Benutzer können auch Berechtigungen erben, weil Sie ein Gruppenmitglied sind. Durch die Verweigerung einer Berechtigung wird jedoch eine geerbte Berechtigung überschrieben. Beispielsweise wird den Mitgliedern der Gruppe Remotedesktop Benutzer (RDU) standardmäßig die Abfrage Berechtigung erteilt. Wenn ein Administrator die Abfrage Berechtigung für diesen Benutzer auf "ablehnen" festlegt, kann der Benutzer die Sitzung eines anderen Benutzers nicht Abfragen. Nachdem sich ein Benutzer bei einer Sitzung angemeldet hat, erhält der Benutzer alle anderen Remotedesktopdienste Berechtigungen für seine Sitzung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopdienste Verwaltungs Anwendungen](terminal-services-management-applications.md)
</dt> <dt>

[**Win32- \_ Konto**](win32-tsaccount.md)
</dt> </dl>

 

