---
description: Steuerung der Winsock-Ablaufverfolgung
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Steuerung der Winsock-Ablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f256c4e3927672bc13b14bfb72ca3b02c22bde
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110548"
---
# <a name="control-of-winsock-tracing"></a>Steuerung der Winsock-Ablaufverfolgung

Die Winsock-Ablaufverfolgung kann mit einer der folgenden Methoden gesteuert werden:

-   Befehlszeilentools

    In Windows Vista und Windows Server 2008 sind zwei Befehlszeilentools enthalten, mit denen die Ablaufverfolgung kontrolliert und die binäre Ablaufverfolgungsprotokolldatei in lesbaren Text konvertiert wird.

    Das **logman.exe** Tool wird verwendet, um die Winsock-Ablaufverfolgung zu starten oder zu beenden.

    Das **tracerpt.exe** Tool wird verwendet, um die binäre Ablaufverfolgungsprotokolldatei in eine lesbare Textdatei zu konvertieren.

-   Ereignisanzeige

    Die Ereignisanzeige unter Windows Vista und höher kann auch verwendet werden, um die Winsock-Ablaufverfolgung zu aktivieren. Der Ereignisanzeige ist über die Verwaltungstools über die Startmenü.

## <a name="using-logman-and-tracert"></a>Verwenden von logman und tracert

Die Winsock-Netzwerkereignisablaufverfolgung ist unter Windows Vista und höher standardmäßig deaktiviert.

Der folgende Befehl startet die Winsock-Netzwerkereignisablaufverfolgung auf einem Computer, legt den Namen der Ereignisablaufverfolgungssitzung auf mywinsocksession fest und sendet die Ausgabe an eine binäre Protokolldatei namens winsocklogfile.etl:

**logman start -ets mywinsocksession -o winsocklogfile.etl -p Microsoft-Windows-Winsock-AFD**

Protokolldateien werden im aktuellen Verzeichnis mit Dateinamen im Format winsocklogfile \_ 000001.etl erstellt.

Der folgende Befehl beendet die oben genannte Winsock-Ablaufverfolgung auf einem Computer für die Sitzung namens mywinsocksession:

**logman stop -ets mywinsocksession**

Eine binäre Protokolldatei wird an den vom -o-Parameter angegebenen Speicherort geschrieben. Um die Binärdatei in eine lesbare Textdatei zu **übersetzen,** tracerpt.exeverwendet:

**tracerpt.exe <Namen der ETL-Datei> -o winsocktracelog.txt**

Wenn eine Ausgabedatei bevorzugt wird, die xml anstelle von Nur-Text enthält, wird der folgende Befehl verwendet:

**tracerpt.exe <Name der ETL-Datei> –o winsocktracelog.xml –von xml**

Die Ablaufverfolgung für Winsock-Katalogänderungen ist unter Windows Vista und höher standardmäßig aktiviert.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 und Windows Server 2012 [die Windows-Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Der folgende Befehl startet die Ablaufverfolgung für Winsock Catalog Change für mehrstufige Dienstanbieter (LSPs) auf einem Computer, legt den Namen der Ereignisablaufverfolgungssitzung auf mywinsockcatalogsession fest und sendet die Ausgabe an eine binäre Protokolldatei namens winsockcataloglogfile.etl:

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

Die Winsock-Netzwerkereignisablaufverfolgung ist jetzt aktiviert, und Sie müssen lediglich die Aktion Aktualisieren drücken, um die Liste der protokollierten Ereignisse zu aktualisieren. Deaktivieren Sie einfach das gleiche Optionsfeld, um die Protokollierung zu beenden.

Möglicherweise müssen Sie die Protokollgröße erhöhen, je nachdem, wie viele Ereignisse Sie anzeigen möchten. Ein Nachteil der Verwendung des Ereignisanzeige für die Winsock-Ablaufverfolgung besteht darin, dass nicht alle Zeichenfolgenressourcen geladen werden, sodass die im Feld Beschreibung angezeigten Meldungen (nachdem Sie ein Ereignis ausgewählt haben) manchmal schwer zu lesen sind (ein Argument, das als hexadezimal formatiert werden soll, wird z. B. als Dezimalzahl angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignisbeschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel einfacher zu verstehende Argumente enthält.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Verwenden von Ereignisanzeige zum Starten der Winsock-Katalogänderungsablaufverfolgung

Wenn Sie Ereignisanzeige öffnen, enthält der linke Bereich die Liste der Ereignisse. Öffnen Sie **Anwendungs- und Dienstprotokolle,** navigieren Sie zu **Microsoft Windows \\ Winsock Catalog Change (Microsoft Windows \\ Winsock-Katalogänderung)** als Quelle, und wählen Sie **Operational (Betriebsbereit)** aus.

Wählen Sie im Bereich Aktion die Option **Protokolleigenschaften** aus, und aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren.** Sobald die Protokollierung aktiviert ist, können Sie bei Bedarf auch die Größe der Protokolldatei ändern.

Die Ablaufverfolgung für Winsock-Katalogänderungen ist jetzt aktiviert, und Sie müssen lediglich die Aktion Aktualisieren ausführen, um die Liste der protokollierten Ereignisse zu aktualisieren. Deaktivieren Sie einfach das gleiche Optionsfeld, um die Protokollierung zu beenden.

Möglicherweise müssen Sie die Protokollgröße erhöhen, je nachdem, wie viele Ereignisse Sie anzeigen möchten. Ein Nachteil der Verwendung des Ereignisanzeige für die Winsock-Ablaufverfolgung besteht darin, dass nicht alle Zeichenfolgenressourcen geladen werden, sodass die im Feld Beschreibung angezeigten Meldungen (nachdem Sie ein Ereignis ausgewählt haben) manchmal schwer zu lesen sind (ein Argument, das als hexadezimal formatiert werden soll, wird z. B. als Dezimalzahl angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignisbeschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel einfacher zu verstehende Argumente enthält.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretieren von Winsock-Ablaufverfolgungsprotokollen

Alle Winsock-Ablaufverfolgungsereignisse in einem Protokoll enthalten zwei Arten von Informationen:

-   System
-   EventData

Die Systeminformationen enthalten den Protokollierstand, die Zeit, zu der der Protokolleintrag erstellt wurde, die Ereignis-ID, die den Ereignistyp darstellt, die Ausführungsprozess-ID, die Ausführungsthread-ID und andere Systeminformationen. Die Protokollebene 4 in der Winsock-Ablaufverfolgung stellt die Protokollierung von Informationsereignis dar. Die Protokollebene 5 in der Winsock-Ablaufverfolgung stellt eine ausführliche Ereignisprotokollierung dar.

Die Ausführungsprozess-ID und thread-ID in den Systeminformationen geben den Prozess und thread an, der beim Ereignis ausgeführt wurde. In vielen Fällen stellt dies einen Kernel- oder Workerthread und -prozess dar, keinen Benutzermodusthread und oder den Prozess der Anwendung. Daher ist dieses Feld normalerweise nicht sehr nützlich.

Jeder Winsock-Ablaufverfolgungsereignistyp verfügt über eine eindeutige Ereignis-ID im Systemabschnitt der protokollierten Daten. Diese Ereignis-IDs können problemlos verwendet werden, um eine Protokolldatei nach bestimmten Winsock-Ablaufverfolgungsereignissen zu filtern.

Die eventdata-Daten enthalten spezifische Informationen für den Ereignistyp.

Der Process-Parameter in den eventdata-Informationen ist die Kernel-EPROCESS-Strukturadresse für den Prozess, nicht die tatsächliche PID. Um ein Ereignis mit der Benutzermodus-PID zu übereinstimmen, verwenden Sie den Wert Verarbeiten aus den eventdata-Informationen eines beliebigen Protokolleintrags, und suchen Sie weiter oben im Protokoll nach einem Socketerstellungsereignis mit dem Wert Verarbeiten. Sobald eine Übereinstimmung gefunden wird, ist der letzte Parameter in den Socketerstellungsereignisdaten die Prozess-ID im Benutzermodus, die den Socket erstellt hat.

Ein Address-Parameter in den eventdata-Informationen wird in einigen Winsock-Ablaufverfolgungsereignissen zurückgegeben. Ein Address-Parameter stellt eine IP-Adresse dar, wird jedoch in der Textdatei angezeigt, die vom **tracerpt.exe-Tool** erstellt wurde, oder in Ereignisanzeige als unformatierte Bytes oder als Zahl. IPv6-Adressen werden hexadezimal angezeigt, sodass sie leichter verständlich sind. IPv4-Adressen werden als große Dezimalzahl angezeigt. Entwickler müssen die unformatierten Bytes einer IPv4-Adresse manuell in die vertrautere IPv4-Punkt-Dezimal-Adressschreibung konvertieren, um den Wert besser interpretieren zu können.

Ein Error-Parameter in eventdata wird in einigen Winsock-Ablaufverfolgungsereignissen zurückgegeben. Ein Error-Parameter weist die Form eines NTSTATUS- oder HRESULT-Fehlercodes auf. Dieser Fehlerparameter wird in der Textdatei angezeigt, die vom **tracerpt.exe** Tool erstellt wurde, oder in Ereignisanzeige als Dezimalzahl. Entwickler müssen die Dezimalzahl manuell in eine hexadezimale Zahl konvertieren, um den Fehlercode in einigen Fällen besser zu interpretieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Ablaufverfolgungsdetails für Winsock-Katalogänderungen](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Details zur Ablaufverfolgung von Winsock-Netzwerkereignissen](winsock-tracing-event-details.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> </dl>

 

 
