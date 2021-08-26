---
description: Steuerung der Winsock-Ablaufverfolgung
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Steuerung der Winsock-Ablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc80251410b95e2d02106474ae97ab3c6ea57759dcfdbc76987d6621794c822e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996810"
---
# <a name="control-of-winsock-tracing"></a>Steuerung der Winsock-Ablaufverfolgung

Die Winsock-Ablaufverfolgung kann mit einer der folgenden Methoden gesteuert werden:

-   Befehlszeilentools

    In Windows Vista und Windows Server 2008 sind zwei Befehlszeilentools enthalten, mit denen die Ablaufverfolgung gesteuert und die binäre Ablaufverfolgungsprotokolldatei in lesbaren Text konvertiert wird.

    Das **logman.exe** Tool wird verwendet, um die Winsock-Ablaufverfolgung zu starten oder zu beenden.

    Das **tracerpt.exe** Tool wird verwendet, um die binäre Ablaufverfolgungsprotokolldatei in eine lesbare Textdatei zu konvertieren.

-   Ereignisanzeige

    Die Ereignisanzeige auf Windows Vista und höher kann auch verwendet werden, um die Winsock-Ablaufverfolgung zu aktivieren. Auf die Ereignisanzeige kann unter den Verwaltungstools über die Startmenü zugegriffen werden.

## <a name="using-logman-and-tracert"></a>Verwenden von logman und tracert

Die Winsock-Netzwerkereignisablaufverfolgung ist auf Windows Vista und höher standardmäßig deaktiviert.

Der folgende Befehl startet die Winsock-Netzwerkereignisablaufverfolgung auf einem Computer, legt den Namen der Ereignisablaufverfolgungssitzung auf mywinsocksession fest und sendet die Ausgabe an eine binäre Protokolldatei namens winsocklogfile.etl:

**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**

Protokolldateien werden im aktuellen Verzeichnis mit Dateinamen im Format winsocklogfile \_ 000001.etl erstellt.

Mit dem folgenden Befehl wird die oben genannte Winsock-Ablaufverfolgung auf einem Computer für die Sitzung mywinsocksession beendet:

**logman stop -ets mywinsocksession**

Eine binäre Protokolldatei wird an den Speicherort geschrieben, der durch den -o-Parameter angegeben wird. Um die Binärdatei in eine lesbare Textdatei zu übersetzen, **wirdtracerpt.exe** verwendet:

**tracerpt.exe <Name der ETL-Datei> –o winsocktracelog.txt**

Wenn eine Ausgabedatei bevorzugt wird, die xml anstelle von Nur-Text enthält, wird der folgende Befehl verwendet:

**tracerpt.exe <Name der ETL-Datei> –o winsocktracelog.xml –von xml**

Die Ablaufverfolgung für Winsock-Katalogänderungen ist standardmäßig auf Windows Vista und höher aktiviert.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 und Windows Server 2012 [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Der folgende Befehl startet die Winsock Catalog Change-Ablaufverfolgung für mehrstufige Dienstanbieter (LSPs) auf einem Computer, legt den Namen der Ereignisablaufverfolgungssitzung auf mywinsockcatalogsession fest und sendet die Ausgabe an eine binäre Protokolldatei namens winsockcataloglogfile.etl:

**logman start -ets mywinsockcatalogsession -o winsockcataloglogfile.etl -p Microsoft-Windows-Winsock-WS2HELP**

Protokolldateien werden im aktuellen Verzeichnis mit Dateinamen im Format winsockcataloglogfile \_ 000001.etl erstellt.

Mit dem folgenden Befehl wird die oben genannte Winsock-Ablaufverfolgung auf einem Computer für die Sitzung mysession beendet:

**logman stop -ets mywinsockcatalogsession**

Eine binäre Protokolldatei wird an den Speicherort geschrieben, der durch den -o-Parameter angegeben wird. Um die Binärdatei in eine lesbare Textdatei zu übersetzen, **wirdtracerpt.exe** verwendet:

**tracerpt.exe <Name der ETL-Datei> –o winsockcatalogtracelog.txt**

Wenn eine Ausgabedatei bevorzugt wird, die xml anstelle von Nur-Text enthält, wird der folgende Befehl verwendet:

**tracerpt.exe <Name der ETL-Datei> –o winsockcatalogtracelog.xml –von xml**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Verwenden von Ereignisanzeige zum Starten der Winsock-Netzwerkereignisablaufverfolgung

Wenn Sie Ereignisanzeige öffnen, enthält der linke Bereich die Liste der Ereignisse. Öffnen Sie **Anwendungs- und Dienstprotokolle,** navigieren Sie zu **Microsoft Windows \\ \\ Winsock Network Event** als Quelle, und wählen Sie **Betriebsbereit** aus.

Wählen Sie im Bereich Aktion die Option **Protokolleigenschaften** aus, und aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren.** Sobald die Protokollierung aktiviert ist, können Sie bei Bedarf auch die Größe der Protokolldatei ändern.

Die Winsock-Netzwerkereignisablaufverfolgung ist jetzt aktiviert, und Sie müssen lediglich die Aktion Aktualisieren drücken, um die Liste der protokollierten Ereignisse zu aktualisieren. Um die Protokollierung zu beenden, deaktivieren Sie einfach das gleiche Optionsfeld.

Möglicherweise müssen Sie die Protokollgröße erhöhen, je nachdem, wie viele Ereignisse Sie anzeigen möchten. Ein Nachteil der Verwendung des Ereignisanzeige für die Winsock-Ablaufverfolgung besteht darin, dass nicht alle Zeichenfolgenressourcen geladen werden, sodass die im Feld Beschreibung angezeigten Meldungen (nachdem Sie ein Ereignis ausgewählt haben) manchmal schwer zu lesen sind (ein Argument, das als hexadezimal formatiert werden soll, wird z. B. als Dezimalzahl angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignisbeschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel einfacher zu verstehende Argumente enthält.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Verwenden von Ereignisanzeige zum Starten der Winsock-Katalogänderungsablaufverfolgung

Wenn Sie Ereignisanzeige öffnen, enthält der linke Bereich die Liste der Ereignisse. Öffnen Sie **Anwendungs- und Dienstprotokolle,** navigieren Sie zu **Microsoft Windows \\ \\ Winsock-Katalogänderung** als Quelle, und wählen Sie **Betriebsbereit** aus.

Wählen Sie im Bereich Aktion die Option **Protokolleigenschaften** aus, und aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren.** Sobald die Protokollierung aktiviert ist, können Sie bei Bedarf auch die Größe der Protokolldatei ändern.

Die Ablaufverfolgung für Winsock-Katalogänderungen ist jetzt aktiviert, und Sie müssen lediglich die Aktion Aktualisieren ausführen, um die Liste der protokollierten Ereignisse zu aktualisieren. Um die Protokollierung zu beenden, deaktivieren Sie einfach das gleiche Optionsfeld.

Möglicherweise müssen Sie die Protokollgröße erhöhen, je nachdem, wie viele Ereignisse Sie anzeigen möchten. Ein Nachteil der Verwendung des Ereignisanzeige für die Winsock-Ablaufverfolgung besteht darin, dass nicht alle Zeichenfolgenressourcen geladen werden, sodass die im Feld Beschreibung angezeigten Meldungen (nachdem Sie ein Ereignis ausgewählt haben) manchmal schwer zu lesen sind (ein Argument, das als hexadezimal formatiert werden soll, wird z. B. als Dezimalzahl angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignisbeschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel einfacher zu verstehende Argumente enthält.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretieren von Winsock-Ablaufverfolgungsprotokollen

Alle Winsock-Ablaufverfolgungsereignisse in einem Protokoll enthalten zwei Arten von Informationen:

-   System
-   EventData

Die Systeminformationen enthalten den Protokolliergrad, den Zeitpunkt der Erstellung des Protokolleintrags, die Ereignis-ID, die den Ereignistyp darstellt, die Ausführungsprozess-ID, die Ausführungsthread-ID und andere Systeminformationen. Der Protokolliergrad 4 in der Winsock-Ablaufverfolgung stellt die Protokollierung von Informationsereignissen dar. Der Protokolliergrad 5 in der Winsock-Ablaufverfolgung stellt die ausführliche Ereignisprotokollierung dar.

Die Ausführungsprozess-ID und thread-ID in den Systeminformationen geben den Prozess und Thread an, der beim Auftreten des Ereignisses ausgeführt wurde. In vielen Fällen stellt dies einen Kernel- oder Workerthread und -prozess dar, nicht einen Benutzermodusthread und den Prozess der Anwendung. Daher ist dieses Feld normalerweise nicht sehr nützlich.

Jeder Winsock-Ablaufverfolgungsereignistyp verfügt über eine eindeutige Ereignis-ID im Systemabschnitt der protokollierten Daten. Diese Ereignis-IDs können problemlos verwendet werden, um eine Protokolldatei nach bestimmten Winsock-Ablaufverfolgungsereignissen zu filtern.

Die eventdata-Daten enthalten spezifische Informationen für den Ereignistyp.

Der Process-Parameter in den eventdata-Informationen ist die Kernel-EPROCESS-Strukturadresse für den Prozess, nicht die tatsächliche PID. Um ein Ereignis mit der Benutzermodus-PID abzugleichen, verwenden Sie den Wert Process aus den eventdata-Informationen aus jedem Protokolleintrag, und suchen Sie weiter oben im Protokoll nach einem Socketerstellungsereignis mit dem Wert Prozess. Sobald eine Übereinstimmung gefunden wurde, ist der letzte Parameter in den Socketerstellungsereignisdaten die Prozess-ID im Benutzermodus, die den Socket erstellt hat.

Ein Address-Parameter in den eventdata-Informationen wird in einigen Winsock-Ablaufverfolgungsereignissen zurückgegeben. Ein Address-Parameter stellt eine IP-Adresse dar, wird jedoch in der Textdatei angezeigt, die vom **tracerpt.exe-Tool** erstellt wurde, oder in Ereignisanzeige als unformatierte Bytes oder als Zahl. IPv6-Adressen werden hexadezimal angezeigt, sodass sie leichter verständlich sind. IPv4-Adressen werden als große Dezimalzahl angezeigt. Entwickler müssen die unformatierten Bytes einer IPv4-Adresse manuell in die vertrautere IPv4-Punkt-Dezimal-Adressnotation konvertieren, um den Wert besser interpretieren zu können.

Ein Error-Parameter in eventdata wird in einigen Winsock-Ablaufverfolgungsereignissen zurückgegeben. Ein Error-Parameter weist die Form eines NTSTATUS- oder HRESULT-Fehlercodes auf. Dieser Fehlerparameter wird in der Textdatei angezeigt, die vom **tracerpt.exe-Tool** erstellt wurde, oder in Ereignisanzeige als Dezimalzahl. Entwickler müssen die Dezimalzahl manuell in eine hexadezimale Zahl konvertieren, um den Fehlercode in einigen Fällen besser zu interpretieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Details zur Ablaufverfolgung von Winsock-Katalogänderungen](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Details zur Ablaufverfolgung von Winsock-Netzwerkereignissen](winsock-tracing-event-details.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> </dl>

 

 
