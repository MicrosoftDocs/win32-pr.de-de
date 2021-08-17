---
description: Eine falsch konfigurierte Firewall kann dazu führen, dass WSD-Anwendungen fehlschlagen.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Überprüfen von Adapter- und Firewall-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ea14051ac65dbd0b749fa00566afc9ed82e5571f6027dafa003e12013888b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130782"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Überprüfen von Adapter- und Firewall-Einstellungen

Eine falsch konfigurierte Firewall kann dazu führen, dass WSD-Anwendungen fehlschlagen. Dieses Thema enthält einige Verfahren zur Problembehandlung, die verwendet werden können, wenn sich WSD-Clients und -Hosts im Netzwerk nicht gegenseitig sehen können. Die Firewalleinstellungen sollten überprüft werden, bevor Sie ein anderes Verfahren zur Problembehandlung für Anwendungen verwenden.

**So überprüfen Sie die Adapter- und Firewalleinstellungen**

1.  Überprüfen Sie, ob **die Netzwerkermittlungsausnahme** aktiviert ist.
2.  Überprüfen Sie, ob keine anwendungsspezifischen Firewallregeln die Anwendung blockieren.
3.  Aktivieren Sie explizit die Ports, die für die Ermittlung und den Metadatenaustausch verwendet werden.
4.  Deaktivieren Sie die Firewall, und testen Sie die Anwendung erneut.
    > [!Note]  
    > Die Firewall sollte nach Abschluss dieses Schritts erneut aktiviert werden.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Überprüfen, ob die Netzwerkermittlungsausnahme aktiviert ist

Wenn eine WS-Discovery ausgeführt wird, muss die **Netzwerkermittlungsfirewallausnahme** zulässig sein.

**So aktivieren Sie die Firewallausnahme für die Netzwerkermittlung**

1.  Klicken **Sie auf Start**, klicken Sie auf **Ausführen,** und geben Sie **dannfirewall.cpl.** Dadurch wird das **Windows Firewall Systemsteuerung** geöffnet.
2.  Wählen **Sie Programm über Windows Firewall zulassen aus.**
3.  Aktivieren Sie **auf der** Registerkarte Ausnahmen das **Kontrollkästchen Netzwerkermittlung.**
4.  Klicken Sie **auf OK,** um das Firewall-Applet zu schließen.

Testen Sie das Programm erneut, nachdem Sie diese Firewalländerung geändert haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Gehen Sie andernfalls mit dem nächsten Schritt fort.

## <a name="checking-for-application-specific-firewall-rules"></a>Überprüfen auf anwendungsspezifische Firewallregeln

Die erweiterte Konfiguration der Windows-Firewall kann in einem MMC-Snap-In (Microsoft Management Control) mit dem Namen **Windows Firewall mit erweiterter Sicherheit stattfinden.** Dieses Snap-In kann verwendet werden, um vermutete Firewallprobleme zu beheben.

Entwickler können die [Windows Firewall mit](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) erweiterten Sicherheits-APIs verwenden, um Firewallregeln zu erstellen, die für ihre WSD-Anwendungen gelten. Insbesondere kann die [**Add-Methode**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) der [**INetFwRules-Schnittstelle**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) verwendet werden, um eine neue Firewallregel hinzuzufügen. Wenn Firewallregeln falsch erstellt werden, können sich Clients und Hosts im Netzwerk möglicherweise nicht gegenseitig sehen.

**So überprüfen Sie auf anwendungsspezifische Firewallregeln**

1.  Klicken **Sie auf Start**, klicken Sie auf **Ausführen,** und geben Sie **dann wf.msc ein.**
2.  Suchen Sie nach anwendungsspezifischen Regeln, die den Datenverkehr möglicherweise blockieren. Weitere Informationen finden Sie unter [Windows Firewall mit erweiterter Sicherheit – Diagnose- und Problembehandlungstools](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Entfernen sie anwendungsspezifische Regeln.

Wenn keine anwendungsspezifischen Regeln gefunden wurden, gehen Sie mit dem nächsten Schritt fort. Wenn eine anwendungsspezifische Regel gefunden und entfernt wurde, testen Sie das Programm erneut, nachdem Sie die Firewalländerung geändert haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Gehen Sie andernfalls mit dem nächsten Schritt fort.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Aktivieren der ports, die für die Ermittlung und den Metadatenaustausch verwendet werden

WS-Discovery verwendet den UDP-Port 3702 für den Nachrichtenaustausch. Darüber hinaus werden die TCP-Ports 5357 und 5358 manchmal für den Metadatenaustausch verwendet. Diese Ports können mithilfe der unter Öffnen eines Ports in der Firewall beschriebenen Verfahren explizit in der [Firewall Windows werden.](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)

Testen Sie das Programm erneut, nachdem Sie diese Firewalländerung geändert haben. Wenn das Programm nun erfolgreich funktioniert, wurde die Ursache des Problems identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Gehen Sie andernfalls mit dem nächsten Schritt fort.

## <a name="disabling-the-firewall"></a>Deaktivieren der Firewall

Die Windows Firewall kann deaktiviert werden, um die Behandlung vermuteter Probleme zu unterstützen. Andere anwendbare Firewalls (z. B. die Firewall auf einem Router) können auch zu Problembehandlungszwecken deaktiviert werden. Informationen zum Aktivieren und Deaktivieren der Windows Firewall finden Sie unter Aktivieren oder Deaktivieren Windows [Firewall.](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)

Testen Sie die Anwendung erneut, nachdem Sie alle anwendbaren Firewalls deaktiviert haben. Wenn das Programm nun erfolgreich funktioniert, blockierte die Firewall den Datenverkehr. Es gibt einige mögliche Ursachen für blockierten Datenverkehr.

-   Anwendungsspezifische Ausnahmen blockierten den Datenverkehr. Überprüfen Sie wie oben beschrieben nach anwendungsspezifischen Firewallregeln.
-   Das Gerät hat zu lange ge dauern, um auf UDP-Anforderungen zu reagieren. Die Windows Firewall kann UDP-Antworten blockieren, die mehr als 4 Sekunden nach dem Senden der ersten Anforderung zurückgeben. Fahren Sie mit der Problembehandlung fort, indem Sie die Unter Verwenden eines generischen Hosts und Clients für [die UDP-WS-Ermittlung](using-a-generic-host-and-client-for-udp-ws-discovery.md) angegebenen Verfahren verwenden, um zu sehen, ob das Problem mit einem Host reproduziert wird, der in weniger als 4 Sekunden antwortet.

Wenn die Anwendung nach dem Deaktivieren der Firewall weiterhin fehlschlägt, verursacht die Firewall den Anwendungsfehler nicht. Aktivieren Sie die Firewalls erneut, und setzen Sie die Problembehandlung fort, indem Sie die Unter Verwenden eines generischen Hosts und Clients für [die UDP-WS-Ermittlung angegebenen Verfahren verwenden.](using-a-generic-host-and-client-for-udp-ws-discovery.md)

Firewalls sollten nach Abschluss der Problembehandlung immer wieder aktiviert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
