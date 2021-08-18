---
description: WinHTTP-Protokolle können zur Problembehandlung von WSDAPI-Anwendungen verwendet werden. Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder die SSL/TLS-Aushandlung fehlschlägt.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Erfassen von WinHTTP-Protokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 648ebb95182096fc4a853c2685f896fa2902a828c8ed0ab143ce89c04831c7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991780"
---
# <a name="capturing-winhttp-logs"></a>Erfassen von WinHTTP-Protokollen

[WinHTTP-Protokolle](/windows/desktop/WinHttp/winhttp-start-page) können zur Problembehandlung von WSDAPI-Anwendungen verwendet werden. Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder die SSL/TLS-Aushandlung fehlschlägt.

In diesem Verfahren wird gezeigt, wie WinHTTP-Protokolle auf dem Client-PC erfasst werden. Die WSDAPI-basierte Clientanwendung darf nicht ausgeführt werden, wenn die Protokollierung aktiviert ist. Wenn die Clientanwendung ausgeführt wird, wenn die Protokollierung aktiviert ist, müssen der Client und/oder der PC neu gestartet werden, bevor WS-Discovery und Metadatenaustauschdatenverkehr in den WinHTTP-Protokollen angezeigt wird.

**So erfassen Sie WinHTTP-Protokolle**

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten auf dem Client-PC.
2.  Führen Sie den folgenden Befehl aus: **netsh winhttp set tracing trace-file-prefix="C: \\ Temp \\ dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**

    Dieser Befehl aktiviert die WinHTTP-Protokollierung. Alle Protokolldateien werden im Verzeichnis C: Temp gespeichert, und die \\ Dateinamen beginnen mit dem Präfix dpws. Es werden mindestens 1 GB Protokolldateien gespeichert.

3.  Wenn der Prozess, der WinHTTP auf dem Client verwendet, bereits ausgeführt wird, starten Sie den Computer neu. Wenn beispielsweise die [Funktionsermittlungs-APIs](/previous-versions/windows/desktop/fundisc/fd-portal) verwendet werden, muss der Computer neu gestartet werden. Die Funktionsermittlungs-APIs rufen WinHTTP von einem Diensthost aus auf, der möglicherweise bereits gestartet wurde, als die Ablaufverfolgung aktiviert wurde.
4.  Starten Sie die WSDAPI-basierte Clientanwendung. Die Anwendung, die debuggt wird, oder der WSD-Debugclient kann verwendet werden.
5.  Reproduzieren Sie den Anwendungsfehler.
6.  Beenden Sie die WSDAPI-basierte Clientanwendung.
7.  Wenn der Prozess, der WinHTTP verwendet, nicht mit der Clientanwendung beendet wird, starten Sie den Computer neu. Wenn beispielsweise die [Funktionsermittlungs-APIs](/previous-versions/windows/desktop/fundisc/fd-portal) verwendet werden, muss der Computer neu gestartet werden.
8.  Führen Sie den folgenden Befehl aus: **netsh winhttp set tracing state=disabled**

    Dieser Befehl deaktiviert die WinHTTP-Protokollierung.

9.  Überprüfen Sie die DPWS-Protokolle in C: Temp, und überprüfen Sie, ob \\ die erforderlichen Anforderungen und Nachrichten gesendet wurden.
10. Wenn https-Kommunikation (Secure Channel) verwendet wird, überprüfen Sie auf SSL/TLS-Fehler.

Nachdem WinHTTP-Protokolle erfasst wurden, können die Protokolle untersucht werden, um nach der Ursache eines WSDAPI-Anwendungsfehlers zu suchen. Beachten Sie, dass der Text-Editor, der zum Anzeigen dieser Protokolle verwendet wird, als Administrator ausgeführt werden muss. Weitere Informationen finden Sie unter [Verwenden der WinHTTP-Protokollierung zum Überprüfen des Get-Datenverkehrs.](using-winhttp-logging-to-verify-get-traffic.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Verwenden der WinHTTP-Protokollierung zum Überprüfen des Get-Datenverkehrs](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
