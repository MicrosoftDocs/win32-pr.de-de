---
description: WinHTTP-Protokolle können verwendet werden, um die Problembehandlung von WSDAPI-Anwendungen zu unterstützen. Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder wenn die SSL/TLS-Aushandlung fehlschlägt.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Erfassen von WinHTTP-Protokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131144"
---
# <a name="capturing-winhttp-logs"></a>Erfassen von WinHTTP-Protokollen

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokolle können verwendet werden, um die Problembehandlung von WSDAPI-Anwendungen zu unterstützen. Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder wenn die SSL/TLS-Aushandlung fehlschlägt.

In diesem Verfahren wird gezeigt, wie Sie WinHTTP-Protokolle auf dem Client-PC erfassen. Die auf WSDAPI basierende Client Anwendung darf nicht ausgeführt werden, wenn die Protokollierung aktiviert ist. Wenn die Client Anwendung ausgeführt wird, während die Protokollierung aktiviert ist, müssen der Client und/oder der PC neu gestartet werden, bevor WS-Discovery und Metadatenaustausch-Datenverkehr in den WinHTTP-Protokollen angezeigt wird.

**So erfassen Sie WinHTTP-Protokolle**

1.  Öffnen Sie auf dem Client-PC ein Eingabe Aufforderungs Fenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **netsh WinHTTP Set Tracing Trace-File-prefix = "C: \\ Temp \\ DPWS" Level = Verbose Format = ANSI State = aktivierte Max-Trace-File-size = 1073741824**

    Dieser Befehl aktiviert die WinHTTP-Protokollierung. Alle Protokolldateien werden im Verzeichnis "C: Temp" gespeichert \\ , und die Dateinamen beginnen mit dem DPWS-Präfix. Es werden höchstens 1 GB Protokolldateien gespeichert.

3.  Wenn der Prozess, der auf dem Client mit WinHTTP ausgeführt wird, bereits ausgeführt wird, starten Sie den Computer neu. Wenn z. b. die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlungs-APIs verwendet werden, muss der Computer neu gestartet werden. Von den funktionsermittlungs-APIs wird WinHTTP von innerhalb eines Dienst Hosts aufgerufen, der möglicherweise bereits gestartet wurde, als die Ablauf Verfolgung aktiviert wurde.
4.  Starten Sie die auf WSDAPI basierende Client Anwendung. Die Anwendung, die gedebuggt wird, oder der WSD-Debugclient kann verwendet werden.
5.  Reproduzieren Sie den Anwendungsfehler.
6.  Beenden Sie die auf WSDAPI basierende Client Anwendung.
7.  Wenn der Prozess, der WinHTTP verwendet, nicht mit der Client Anwendung beendet wird, starten Sie den Computer neu. Wenn z. b. die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlungs-APIs verwendet werden, muss der Computer neu gestartet werden.
8.  Führen Sie den folgenden Befehl aus: **netsh WinHTTP Set Tracing State = deaktiviert** .

    Mit diesem Befehl wird die WinHTTP-Protokollierung deaktiviert.

9.  Überprüfen Sie die DPWS-Protokolle in C: \\ Temp, und überprüfen Sie, ob die erforderlichen Anforderungen und Nachrichten gesendet wurden.
10. Wenn die HTTPS-Kommunikation (Secure Channel) verwendet wird, überprüfen Sie auf SSL/TLS-Fehler.

Nachdem WinHTTP-Protokolle erfasst wurden, können die Protokolle untersucht werden, um die Ursache für einen WSDAPI-Anwendungsfehler zu suchen. Beachten Sie, dass der Text-Editor, der zum Anzeigen dieser Protokolle verwendet wird, als Administrator ausgeführt werden muss. Weitere Informationen finden Sie unter [Verwenden der WinHTTP-Protokollierung zum Überprüfen von Datenverkehr](using-winhttp-logging-to-verify-get-traffic.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Verwenden der WinHTTP-Protokollierung zum Überprüfen von Daten](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
