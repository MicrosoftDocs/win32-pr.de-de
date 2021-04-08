---
title: Aktivieren der EAPHost-Ablauf Verfolgung
description: Kann Benutzer bei der Suche nach den Hauptursachen von Problemen unterstützen, die während des EAP-Authentifizierungs Vorgangs auftreten. Zu den Debuginformationen können API-Aufrufe ausgeführt werden, interne Funktionsaufrufe durchgeführt und Zustandsübergänge ausgeführt werden.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104039882"
---
# <a name="enabling-eaphost-tracing"></a>Aktivieren der EAPHost-Ablauf Verfolgung

Ablauf Verfolgungs Protokolle mit Debuginformationen können Benutzer bei der Suche nach den Hauptursachen von Problemen unterstützen, die während des EAP-Authentifizierungs Vorgangs auftreten. Zu den Debuginformationen können API-Aufrufe ausgeführt werden, interne Funktionsaufrufe durchgeführt und Zustandsübergänge ausgeführt werden.

Die Ablauf Verfolgung kann sowohl auf der Clientseite als auch auf der Authenticator-Seite aktiviert werden. Die Ablauf Verfolgung kann auch für Aufrufe der APIs für den [Routing-und RAS-Dienst (RRAS)](/windows/desktop/RRAS/routing-start-page) aktiviert werden. Weitere Informationen finden Sie unter Ablauf [Verfolgung für den Routing-und RAS-Dienst](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> Ablauf Verfolgungs Protokolle sind nur in englischer Sprache verfügbar.

 

Wenn die EAPHost-Ablauf Verfolgung aktiviert ist, werden die Protokollierungs Informationen in einer ETL-Datei an einem vom Benutzer angegebenen Speicherort gespeichert. Wenn während der EAP-Authentifizierung Fehler auftreten, generiert die Ablauf Verfolgung eine ETL-Datei, die für die Fehlerursachen Analyse an Developer Support Microsoft gesendet werden kann. Partner, die Zugriff auf Microsoft Windows Build-Freigaben,-Symbole und traceformat-Dateien haben, können die ETL-Dateien mithilfe des **tracerpt** -Tools in eine einfache Textdatei konvertieren.

NPS-Fehler (Network Policy Server, Netzwerk Richtlinien Server) werden in den EAPHost-Protokollen nicht erfasst. Wenn Sie versuchen, einen NPS-Fehler zu beheben, sehen Sie sich den iassam an. Log und [iasnap. Protokoll](https://go.microsoft.com/fwlink/p/?linkid=84108) Dateien.

## <a name="tracing-on-the-client"></a>Ablauf Verfolgung auf dem Client

So aktivieren Sie die Ablauf Verfolgung auf der Clientseite:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **logman** **Start Trace** **eaphostpeer** **-o** **. \\ Eaphostpeer. ETL** **-p** **{5f31090b-d990-4e91-b16d-46121d0255aa} 0x4000ffff 0** **-ETS**
3.  Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.
4.  Führen Sie den folgenden Befehl aus: **logman** **stoppt** **eaphostpeer** **-ETS** .
5.  Konvertieren Sie die ETL-Datei mithilfe des folgenden Befehls in Text: **tracerpt eaphostpeer. ETL** **– PDB** **&lt; PDBPATH &gt;** **-tp** **&lt; tracemessagefilesdirector &gt; ypath** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Wenn Sie keinen Zugriff auf das tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie die ETL-Datei an Microsoft Developer Support.

     

## <a name="tracing-on-the-authenticator"></a>Ablauf Verfolgung für den Authentifikator

So aktivieren Sie die Ablauf Verfolgung auf der Authentifikator-Seite:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **logman** **Start Trace** **eaphostauthr** **-o** **. \\ Eaphostauthr. ETL** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**
3.  Reproduzieren Sie das Szenario, das Sie nachverfolgen möchten.
4.  Führen Sie den folgenden Befehl aus: **logman** **stoppt** **eaphostauthr** **-ETS** .
5.  Konvertieren Sie die ETL-Datei mithilfe des folgenden Befehls in Text: **tracerpt eaphostauthr. ETL** **– PDB** **&lt; PDBPATH &gt;** **-tp** **&lt; tracemessagefilesdirecterypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Wenn Sie keinen Zugriff auf das tracerpt-Tool haben, vermeiden Sie den letzten Schritt, und senden Sie stattdessen die ETL-Datei an Microsoft Developer Support.

     

## <a name="event-tracing"></a>Ereignisablaufverfolgung

In Windows 7 und höheren Versionen von Windows bietet EAPHost eine ereignisbasierte Ablauf Verfolgung für den Authentifikator und den Peer. Der Vorteil der ereignisbasierten Ablauf Verfolgung besteht darin, dass zum Anzeigen der Ablauf Verfolgungs Meldungen keine Symbol Dateien erforderlich sind. So aktivieren Sie die Ereignis Ablauf Verfolgung:

1.  Öffnen Sie **Event Viewer**.
2.  Wichtige EAPHost-Nachrichten werden unter "benutzerdefinierte Ansichten \\ Administrative Ereignisse" protokolliert.
3.  Nicht kritische Nachrichten werden unter "Anwendungen und Dienste \\ Microsoft \\ Windows \\ EAPHost" protokolliert.
4.  Ereignismeldungen vom Typ "Analyse" und "Debuggen" können unter demselben Pfad angezeigt werden, indem Sie in der Titelleiste im Menü **Ansicht** die Option **analytische und Debugprotokolle anzeigen** auswählen.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Ablauf Verfolgung für den Routing-und RAS-Dienst

So aktivieren Sie die RRAS-Ablauf Verfolgung:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **netsh** **RAS** **set** **TR** **\* *_ _* en**
3.  **% Systemroot%-Ablauf \\ Verfolgung** öffnen, um RAS-Ablauf Verfolgungen anzuzeigen

So deaktivieren Sie die RRAS-Ablauf Verfolgung:

1.  Öffnen Sie ein Eingabeaufforderungsfenster mit erhöhten Rechten.
2.  Führen Sie den folgenden Befehl aus: **netsh** **RAS** **set** **TR** **\* *_ _* DIS**

Weitere Informationen finden Sie unter [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[Routing- und RAS-Dienst (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 