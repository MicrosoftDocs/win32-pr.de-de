---
description: Eine falsch konfigurierte Firewall kann dazu führen, dass WSD-Anwendungen fehlschlagen.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Überprüfen der Adapter-und Firewalleinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344878"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Überprüfen der Adapter-und Firewalleinstellungen

Eine falsch konfigurierte Firewall kann dazu führen, dass WSD-Anwendungen fehlschlagen. Dieses Thema enthält einige Verfahren zur Problembehandlung, die verwendet werden können, wenn WSD-Clients und-Hosts sich nicht gegenseitig im Netzwerk sehen. Die Firewalleinstellungen sollten vor der Verwendung anderer anwendungsproblembehandlungs-Verfahren überprüft werden.

**So überprüfen Sie die Adapter-und Firewalleinstellungen**

1.  Vergewissern Sie sich, dass die **Netzwerk** Ermittlungs Ausnahme aktiviert ist.
2.  Stellen Sie fest, dass die Anwendung nicht durch anwendungsspezifische Firewallregeln blockiert wird.
3.  Aktivieren Sie die Ports, die für den Discovery-und Metadatenaustausch verwendet werden
4.  Deaktivieren Sie die Firewall, und testen Sie die Anwendung erneut.
    > [!Note]  
    > Die Firewall sollte nach Abschluss dieses Schritts erneut aktiviert werden.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Es wird überprüft, ob die Netzwerk Ermittlungs Ausnahme aktiviert ist.

Wenn WS-Discovery Anwendungen ausgeführt werden, muss die Firewallausnahme für die **Netzwerk** Ermittlung zugelassen werden.

**So aktivieren Sie die Firewallausnahme für die Netzwerk Ermittlung**

1.  Klicken Sie im **Startmenü** auf **Ausführen**, und geben Sie dann **firewall.cpl** ein. Dadurch wird das Applet **Windows-Firewall-Systemsteuerung** geöffnet.
2.  Wählen Sie **Programm durch Windows-Firewall zulassen** aus.
3.  Aktivieren Sie auf der Registerkarte **Ausnahmen** das Kontrollkästchen **Netzwerk** Ermittlung.
4.  Klicken Sie auf **OK** , um das Applet Firewall zu schließen.

Testen Sie das Programm erneut, nachdem Sie diese firewalländerung vorgenommen haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Fahren Sie andernfalls mit dem nächsten Schritt fort.

## <a name="checking-for-application-specific-firewall-rules"></a>Überprüfen auf anwendungsspezifische Firewallregeln

Die erweiterte Konfiguration der Windows-Firewall kann in einem MMC-Snap-in (Microsoft Management Control) namens **Windows-Firewall mit** erweiterter Sicherheit stattfinden. Dieses Snap-in kann verwendet werden, um verdächtige Firewallprobleme zu beheben.

Entwickler können die APIs der [Windows-Firewall mit](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) erweiterter Sicherheit verwenden, um Firewallregeln zu erstellen, die für Ihre WSD-Anwendungen gelten. Insbesondere kann die [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) -Methode der [**inetfwrules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) -Schnittstelle verwendet werden, um eine neue Firewallregel hinzuzufügen. Wenn Firewallregeln nicht ordnungsgemäß erstellt werden, können Clients und Hosts möglicherweise nicht im Netzwerk angezeigt werden.

**So überprüfen Sie anwendungsspezifische Firewallregeln**

1.  Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, und geben Sie dann **WF. msc** ein.
2.  Suchen Sie nach anwendungsspezifischen Regeln, die den Datenverkehr möglicherweise blockieren. Weitere Informationen finden Sie unter [Windows-Firewall mit erweiterter Sicherheit-Diagnose und Tools zur Problem](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink)Behandlung.
3.  Entfernen Sie anwendungsspezifische Regeln.

Wenn keine anwendungsspezifischen Regeln gefunden werden, fahren Sie mit dem nächsten Schritt fort. Wenn eine anwendungsspezifische Regel gefunden und entfernt wurde, testen Sie das Programm erneut, nachdem Sie die Firewall geändert haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Fahren Sie andernfalls mit dem nächsten Schritt fort.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Aktivieren der Ports, die für Ermittlungs-und Metadatenaustausch verwendet werden

WS-Discovery verwendet den UDP-Port 3702 für den Nachrichtenaustausch. Außerdem werden die TCP-Ports 5357 und 5358 manchmal für Metadatenaustausch verwendet. Diese Ports können mithilfe der unter [Öffnen eines Ports in der Windows-Firewall](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)beschriebenen Verfahren explizit in der Firewall geöffnet werden.

Testen Sie das Programm erneut, nachdem Sie diese firewalländerung vorgenommen haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Fahren Sie andernfalls mit dem nächsten Schritt fort.

## <a name="disabling-the-firewall"></a>Deaktivieren der Firewall

Die Windows-Firewall kann deaktiviert werden, um die Behandlung von verdächtigen Problemen zu unterstützen. Andere anwendbare Firewalls (z. b. die Firewall auf einem Router) können auch zu Problem Behandlungszwecken deaktiviert werden. Informationen zum Aktivieren und Deaktivieren der Windows-Firewall finden Sie unter Aktivieren oder Deaktivieren der [Windows](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)-Firewall.

Testen Sie die Anwendung neu, nachdem Sie alle anwendbaren Firewalls deaktiviert haben. Wenn das Programm nun erfolgreich funktioniert, hat die Firewall den Datenverkehr blockiert. Es gibt einige mögliche Ursachen für blockierten Datenverkehr.

-   Anwendungsspezifische Ausnahmen haben den Datenverkehr blockiert. Suchen Sie wie oben beschrieben nach anwendungsspezifischen Firewallregeln.
-   Das Gerät benötigte zu lange, um auf UDP-Anforderungen zu reagieren. Die Windows-Firewall blockiert möglicherweise UDP-Antworten, die mehr als 4 Sekunden nach dem Senden der ursprünglichen Anforderung zurückgeben. Setzen Sie die Problembehandlung fort, indem Sie die Anweisungen unter [Verwenden eines generischen Hosts und Clients für die UDP-WS-](using-a-generic-host-and-client-for-udp-ws-discovery.md) Ermittlung befolgen, um festzustellen, ob das Problem mit einem Host, der in weniger als 4 Sekunden antwortet, neu erzeugt

Wenn die Anwendung nach der Deaktivierung der Firewall weiterhin ausfällt, verursacht die Firewall nicht den Anwendungsfehler. Aktivieren Sie die Firewalls erneut, und fahren Sie mit der Problembehandlung fort, indem Sie die Anweisungen unter [Verwenden eines generischen Hosts und Clients für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)befolgen.

Firewalls sollten nach Abschluss der Problembehandlung immer erneut aktiviert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
