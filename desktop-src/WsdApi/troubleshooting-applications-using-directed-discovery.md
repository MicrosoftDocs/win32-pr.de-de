---
description: Anwendungen, die die gesteuerte Ermittlung verwenden, senden Testnachrichten über HTTP oder HTTPS, um Geräte zu ermitteln.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Problembehandlung bei WSDAPI-Anwendungen mithilfe der gesteuerten Ermittlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528574"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Problembehandlung bei WSDAPI-Anwendungen mithilfe der gesteuerten Ermittlung

Anwendungen, die die gesteuerte Ermittlung verwenden [, senden Test](probe-message.md) Nachrichten über HTTP oder HTTPS, um Geräte zu ermitteln. Die entsprechenden [Probe Matches](probematches-message.md) -Nachrichten, die als Antwort gesendet werden, werden auch über HTTP oder HTTPS gesendet. Die gesteuerte Ermittlung kann mit dem Assistenten zum Hinzufügen von Druckern, einem Funktions Ermittlungs Client oder einer WSDAPI-Anwendung initiiert werden. Die Test-und Probe Matches-Meldungen sind strukturell identisch mit den über UDP gesendeten. Den Nachrichten werden die entsprechenden http-oder HTTPS-Header vorangestellt.

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einer Anwendung mithilfe der gesteuerten Ermittlung zu identifizieren.

**So beheben Sie Probleme mit einer WSDAPI-Anwendung mithilfe der gesteuerten Ermittlung**

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für eine Anwendung mithilfe der gesteuerten](inspecting-network-traces-for-applications-using-directed-discovery.md)Ermittlung.

Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Problembehandlung beim Hinzufügen von Drucker](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Problembehandlung bei WSDAPI-Anwendungen](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



