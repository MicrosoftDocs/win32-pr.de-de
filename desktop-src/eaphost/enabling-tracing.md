---
title: Aktivieren der EAPHost-Ablaufverfolgung
description: Kann Benutzern dabei helfen, die Grundursachen von Problemen zu finden, die während des EAP-Authentifizierungsprozesses auftreten. Die Debuginformationen können ausgeführte API-Aufrufe, ausgeführte interne Funktionsaufrufe und ausgeführte Zustandsübergänge umfassen.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c638fa7f546028cd9cf66227cfe3c302d6599492d1cbbfcfdac6c2b428273db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086292"
---
# <a name="enabling-eaphost-tracing"></a>Aktivieren der EAPHost-Ablaufverfolgung

Ablaufverfolgungsprotokolle, die Debuginformationen enthalten, können Benutzern helfen, die Grundursachen von Problemen zu finden, die während des EAP-Authentifizierungsprozesses auftreten. Die Debuginformationen können ausgeführte API-Aufrufe, ausgeführte interne Funktionsaufrufe und ausgeführte Zustandsübergänge umfassen.

Die Ablaufverfolgung kann sowohl auf clientseitiger als auch auf Authentatorseite aktiviert werden. Die Ablaufverfolgung kann auch für Aufrufe der [RRAS-APIs (Routing and Remote Access Service)](/windows/desktop/RRAS/routing-start-page) aktiviert werden. Weitere Informationen finden Sie unter [Ablaufverfolgung für den Routing- und RAS-Dienst.](#tracing-on-the-routing-and-remote-access-service)

> [!Note]  
> Ablaufverfolgungsprotokolle sind nur auf Englisch verfügbar.

 

Wenn die EAPHost-Ablaufverfolgung aktiviert ist, werden Protokollierungsinformationen in einer ETL-Datei an einem vom Benutzer angegebenen Speicherort gespeichert. Wenn während der EAP-Authentifizierung Fehler auftreten, generiert die Ablaufverfolgung eine ETL-Datei, die zur Ursachenanalyse an Microsoft-Entwickler Support gesendet werden kann. Partner, die Zugriff auf Microsoft Windows-Buildfreigaben, Symbole und Traceformatdateien haben, können die ETL-Dateien mithilfe des **Tracerpt-Tools** in eine Nur-Text-Datei konvertieren.

NpS-Fehler (Netzwerkrichtlinienserver) werden in den EAPHost-Protokollen nicht erfasst. Wenn Sie versuchen, einen NPS-Fehler zu beheben, sehen Sie sich den IASSAM an. LOG und [IASNAP. LOG-Dateien.](https://go.microsoft.com/fwlink/p/?linkid=84108)

## <a name="tracing-on-the-client"></a>Ablaufverfolgung auf dem Client

So aktivieren Sie die Ablaufverfolgung auf Clientseite:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **logman** **start trace** **EapHostPeer** **-o** **. \\ EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**
3.  Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.
4.  Führen Sie den folgenden Befehl aus: **logman** **stop** **EapHostPeer** **-ets**
5.  Konvertieren Sie die etl-Datei mit dem folgenden Befehl in Text: **tracerpt EapHostPeer.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Wenn Sie keinen Zugriff auf das Tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie die ETL-Datei an Microsoft-Entwickler Support.

     

## <a name="tracing-on-the-authenticator"></a>Ablaufverfolgung im Authenticator

So aktivieren Sie die Ablaufverfolgung auf Authentatorseite:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **logman** **start trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**
3.  Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.
4.  Führen Sie den folgenden Befehl aus: **logman** **stop** **EapHostAuthr** **-ets**
5.  Konvertieren Sie die etl-Datei mit dem folgenden Befehl in Text: **tracerpt EapHostAuthr.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Wenn Sie keinen Zugriff auf das Tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie stattdessen die ETL-Datei an Microsoft-Entwickler Support.

     

## <a name="event-tracing"></a>Ereignisablaufverfolgung

In Windows 7 und neueren Versionen von Windows stellt EapHost eine ereignisbasierte Ablaufverfolgung für den Authentator und den Peer zur Verfügung. Der Vorteil der ereignisbasierten Ablaufverfolgung ist, dass zum Anzeigen der Ablaufverfolgungsmeldungen keine Symboldateien erforderlich sind. So aktivieren Sie die Ereignisablaufverfolgung:

1.  Öffnen **Sie EventViewer.**
2.  Kritische EapHost-Nachrichten werden unter "Administrative Ereignisse für benutzerdefinierte \\ Ansichten" protokolliert.
3.  Nicht kritische Meldungen werden protokolliert unter: "Anwendungen und Dienste \\ Microsoft \\ Windows \\ EapHost
4.  Ereignismeldungen vom Typ "Analytics" und "Debug" können unter demselben Pfad angezeigt  werden, indem Sie im Ansichtsmenü in der Titelleiste Analyse- und **Debugprotokolle** anzeigen auswählen.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Ablaufverfolgung für den Routing- und RAS-Dienst

So aktivieren Sie die RRAS-Ablaufverfolgung:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **netsh** **ras** **set** **tr** **\* *_ _* en**
3.  Öffnen der **Ablaufverfolgung %systemroot% \\** zum Anzeigen von RAS-Ablaufverfolgungen

So deaktivieren Sie die RRAS-Ablaufverfolgung:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **netsh** **ras** **set** **tr** _ **\* *_* dis**

Weitere Informationen finden Sie unter [Netsh-Befehle.](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[Routing- und RAS-Dienst (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 