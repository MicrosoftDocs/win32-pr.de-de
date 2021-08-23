---
title: Remotedesktopdienste Berechtigungen
description: Sie können die für Remotedesktopdienste bereitgestellten Berechtigungen verwenden, um zu steuern, wie Benutzer und Gruppen auf den Server zugreifen.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668bf4902ffb133c403e5ea2f74bbc165cf99bca500c95eed5d5dac3cb48a710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999890"
---
# <a name="remote-desktop-services-permissions"></a>Remotedesktopdienste Berechtigungen

Sie können die für Remotedesktopdienste bereitgestellten Berechtigungen verwenden, um zu steuern, wie Benutzer und Gruppen auf den Server zugreifen. Eine Beschreibung der Standardberechtigungstypen und ausführlichere Informationen zu Remotedesktopdienste Berechtigungen im Allgemeinen finden Sie in der Dokumentation zum Remotedesktopdienste Configuration-Verwaltungstool. Informationen zum Konfigurieren dieser Berechtigungen für Windows Server 2008 finden Sie unter [Konfigurieren von Berechtigungen für Remotedesktopdienste Verbindungen.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11))

Im Folgenden finden Sie eine Liste der Berechtigungen, die Sie festlegen können, und der Aufgaben, die die Berechtigungen zulassen.



| Wert                        | Bedeutung                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abfrageinformationen<br/> | Fragen Sie Sitzungen und Server nach Informationen ab.<br/>                                                                                                                |
| Festlegen von Informationen<br/>   | Konfigurieren von Verbindungseigenschaften.<br/>                                                                                                                           |
| Remotesteuerung<br/>    | Anzeigen oder aktives Steuern der Sitzung eines anderen Benutzers.<br/>                                                                                                           |
| Anmelden<br/>             | Melden Sie sich bei einer Sitzung auf dem Server an.<br/>                                                                                                                         |
| Abmelden (Logoff)<br/>            | Melden Sie einen Benutzer von einer Sitzung ab. Beachten Sie, dass das Abmelden eines Benutzers ohne Warnung zum Verlust von Daten auf dem Client führen kann.<br/>                                  |
| `Message`<br/>           | Senden sie eine Nachricht an die Sitzungen eines anderen Benutzers.<br/>                                                                                                                 |
| Verbinden<br/>           | Verbinden zu einer anderen Sitzung.<br/>                                                                                                                                |
| Trennen<br/>        | Trennen sie eine Sitzung.<br/>                                                                                                                                      |
| Virtuelle Kanäle<br/>  | Verwenden Sie virtuelle Kanäle. Beachten Sie, dass durch das Deaktivieren virtueller Kanäle einige Remotedesktopdienste Features deaktiviert werden, z. B. zwischenablage und Druckerumleitung.<br/> |
| Reset<br/>             | Beenden sie eine Sitzung. Beachten Sie, dass das Beenden einer Sitzung ohne Warnung zum Verlust von Daten auf dem Client führen kann.<br/>                                                    |



 

Die Anmeldeberechtigung ist erforderlich, damit sich ein Benutzer bei einer neuen Remotedesktopdienste Sitzung anmelden kann. Alle anderen Remotedesktopdienste Berechtigungen gelten für die Steuerung der Remotedesktopdienste Sitzung eines anderen Benutzers.

Remotedesktopdienste Berechtigungen können für einzelne Benutzer oder Gruppen erteilt oder festgelegt werden. Benutzer können berechtigungen auch erben, wenn sie ein Gruppenmitglied sind. Die Verweigerung einer Berechtigung überschreibt jedoch eine geerbte Berechtigung. Beispielsweise wird Mitgliedern der Gruppe Remotedesktop Benutzer (RDU) standardmäßig die Abfrageberechtigung erteilt. Wenn ein Administrator die Abfrageberechtigung für diesen Benutzer auf "Verweigern" festlegt, kann der Benutzer die Sitzung eines anderen Benutzers nicht abfragen. Nachdem sich ein Benutzer bei einer Sitzung anmeldet, erhält er alle anderen Remotedesktopdienste Berechtigungen für seine Sitzung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopdienste-Verwaltungsanwendungen](terminal-services-management-applications.md)
</dt> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

