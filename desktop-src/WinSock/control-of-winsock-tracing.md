---
description: .
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Kontrolle über die Winsock-Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b15ece4581525fddc25213c630e24d0e49110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356760"
---
# <a name="control-of-winsock-tracing"></a>Kontrolle über die Winsock-Ablauf Verfolgung

Die Winsock-Ablauf Verfolgung kann mit einer der folgenden Methoden gesteuert werden:

-   Befehlszeilentools

    In Windows Vista und Windows Server 2008 sind zwei Befehlszeilen Tools enthalten, mit denen die Ablauf Verfolgung gesteuert und die Binärdatei für die Ablauf Verfolgungs Protokolle in lesbaren Text konvertiert wird.

    Das **logman.exe** Tool wird verwendet, um die Winsock-Ablauf Verfolgung zu starten oder zu starten.

    Das **tracerpt.exe** Tool wird verwendet, um die Binärdatei der Ablauf Verfolgungs Protokolle in eine lesbare Textdatei zu konvertieren.

-   Ereignisanzeige

    Der Ereignisanzeige unter Windows Vista und höher kann auch verwendet werden, um die Winsock-Ablauf Verfolgung zu aktivieren. Der Ereignisanzeige ist unter den Verwaltungs Tools über das Startmenü verfügbar.

## <a name="using-logman-and-tracert"></a>Verwenden von logman und tracert

Die Winsock-Netzwerk Ereignis Ablauf Verfolgung ist unter Windows Vista und höher standardmäßig deaktiviert.

Der folgende Befehl startet die Winsock-Netzwerk Ereignis Ablauf Verfolgung auf einem Computer, legt den Namen der Ereignis Ablauf Verfolgungs Sitzung auf mywinsocksession fest und sendet die Ausgabe an eine binäre Protokolldatei mit dem Namen winsocklogfile. ETL:

**logman start-ETs mywinsocksession-o winsocklogfile. ETL-p Microsoft-Windows-Winsock-AFD**

Protokolldateien werden im aktuellen Verzeichnis mit Dateinamen in der Form winsocklogfile \_ 000001. etl erstellt.

Mit dem folgenden Befehl wird die obige Winsock-Ablauf Verfolgung auf einem Computer für die Sitzung mit dem Namen "mywinsocksession" beendet:

**logman beendet-ETS mywinsocksession**

Eine binäre Protokolldatei wird an den Speicherort geschrieben, der durch den – o-Parameter angegeben wird. Wenn die Binärdatei in eine lesbare Textdatei übersetzt werden soll, wird **tracerpt.exe** verwendet:

**tracerpt.exe <Namen der ETL-Datei> – o winsocktracelog.txt**

Wenn eine Ausgabedatei, die XML anstelle von Klartext enthält, bevorzugt wird, wird der folgende Befehl verwendet:

**tracerpt.exe <Namen der ETL-Datei> – o winsocktracelog.xml – von XML**

Die Änderungs Ablauf Verfolgung für den Winsock-Katalog ist unter Windows Vista und höher standardmäßig aktiviert.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Der folgende Befehl startet die Änderungs Ablauf Verfolgung für den Winsock-Katalog für mehrstufige Dienstanbieter (LSPs) auf einem Computer, legt den Namen der Ereignis Ablauf Verfolgungs Sitzung auf mywinsockcatalogsession fest und sendet die Ausgabe an eine binäre Protokolldatei mit dem Namen winsockcataloglogfile. ETL:

**logman start-ETs mywinsockcatalogsession-o winsockcataloglogfile. ETL-p Microsoft-Windows-Winsock-WS2HELP**

Protokolldateien werden im aktuellen Verzeichnis mit Dateinamen in der Form winsockcataloglogfile \_ 000001. etl erstellt.

Mit dem folgenden Befehl wird die obige Winsock-Ablauf Verfolgung auf einem Computer für die Sitzung mit dem Namen "MySession" beendet:

**logman beendet-ETS mywinsockcatalogsession**

Eine binäre Protokolldatei wird an den Speicherort geschrieben, der durch den – o-Parameter angegeben wird. Wenn die Binärdatei in eine lesbare Textdatei übersetzt werden soll, wird **tracerpt.exe** verwendet:

**tracerpt.exe <Namen der ETL-Datei> – o winsockcatalogtracelog.txt**

Wenn eine Ausgabedatei, die XML anstelle von Klartext enthält, bevorzugt wird, wird der folgende Befehl verwendet:

**tracerpt.exe <Namen der ETL-Datei> – o winsockcatalogtracelog.xml – von XML**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Verwenden von Ereignisanzeige zum Starten der Winsock-Netzwerk Ereignis Ablauf Verfolgung

Wenn Sie Ereignisanzeige öffnen, enthält der linke Bereich die Liste der Ereignisse. Öffnen Sie **Anwendungs-und Dienst Protokolle** , und navigieren Sie zum **Microsoft \\ Windows \\ Winsock-Netzwerk Ereignis** als Quelle, und wählen Sie **Operational** aus.

Wählen Sie im Aktionsbereich die Option **Protokoll Eigenschaften** aus, und aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren** . Wenn die Protokollierung aktiviert ist, können Sie auch die Größe der Protokolldatei ändern, wenn dies erforderlich ist.

Die Winsock-Netzwerk Ereignis Ablauf Verfolgung ist nun aktiviert, und Sie müssen nur noch die Aktualisierungs Aktion ausführen, um die Liste der protokollierten Ereignisse zu aktualisieren. Deaktivieren Sie einfach das Optionsfeld, um die Protokollierung zu deaktivieren.

Abhängig von der Anzahl der Ereignisse, die Sie anzeigen möchten, müssen Sie möglicherweise die Größe des Protokolls erhöhen. Ein Nachteil bei der Verwendung des Ereignisanzeige für die Winsock-Ablauf Verfolgung besteht darin, dass nicht alle Zeichen folgen Ressourcen geladen werden, sodass die Nachrichten, die im Beschreibungsfeld angezeigt werden (nachdem Sie ein Ereignis ausgewählt haben), manchmal schwer lesbar sind (ein Argument, das als Hex formatiert werden sollte, wird beispielsweise in Dezimalform angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignis Beschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel leichter zu verstehen ist.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Verwenden von Ereignisanzeige zum Starten der Ablauf Verfolgung der Winsock-Katalog Änderung

Wenn Sie Ereignisanzeige öffnen, enthält der linke Bereich die Liste der Ereignisse. Öffnen Sie **Anwendungs-und Dienst Protokolle** , und navigieren Sie zu **Microsoft \\ Windows \\ Winsock Catalog Change** als Quelle, und wählen Sie **Operational** aus.

Wählen Sie im Aktionsbereich die Option **Protokoll Eigenschaften** aus, und aktivieren Sie das Kontrollkästchen **Protokollierung aktivieren** . Wenn die Protokollierung aktiviert ist, können Sie auch die Größe der Protokolldatei ändern, wenn dies erforderlich ist.

Die Änderungs Ablauf Verfolgung für den Winsock-Katalog ist jetzt aktiviert, und Sie müssen nur noch die Aktualisierungs Aktion ausführen, um die Liste der protokollierten Ereignisse zu aktualisieren. Deaktivieren Sie einfach das Optionsfeld, um die Protokollierung zu deaktivieren.

Abhängig von der Anzahl der Ereignisse, die Sie anzeigen möchten, müssen Sie möglicherweise die Größe des Protokolls erhöhen. Ein Nachteil bei der Verwendung des Ereignisanzeige für die Winsock-Ablauf Verfolgung besteht darin, dass nicht alle Zeichen folgen Ressourcen geladen werden, sodass die Nachrichten, die im Beschreibungsfeld angezeigt werden (nachdem Sie ein Ereignis ausgewählt haben), manchmal schwer lesbar sind (ein Argument, das als Hex formatiert werden sollte, wird beispielsweise in Dezimalform angezeigt). Sie können jedoch die Registerkarte **Details** in der Ereignis Beschreibung auswählen, die den unformatierten XML-Protokolleintrag anzeigt, der in der Regel leichter zu verstehen ist.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretieren von Winsock-Ablauf Verfolgungs Protokollen

Alle Winsock-Ablauf Verfolgungs Ereignisse in einem Protokoll enthalten zwei Arten von Informationen:

-   System
-   EventData

Die Systeminformationen enthalten den Protokolliergrad, den Zeitpunkt, zu dem der Protokolleintrag erstellt wurde, die Ereignis-ID, die den Ereignistyp, die Ausführungsprozess-ID, die Ausführungs Thread-ID und andere Systeminformationen darstellt. Die Protokollebene 4 in der Winsock-Ablauf Verfolgung stellt die Protokollierung von Informations Ereignissen dar. Die Protokollebene 5 in der Winsock-Ablauf Verfolgung stellt die Protokollierung ausführlicher Ereignisse dar.

Die Ausführungsprozess-ID und die Thread-ID in den Systeminformationen gibt den Prozess und den Thread an, der ausgeführt wurde, als das Ereignis aufgetreten ist. In vielen Fällen stellt dies einen Kernel-oder Arbeits Thread und-Prozess dar, nicht einen benutzermoduscothread und oder den Prozess der Anwendung. Dieses Feld ist daher normalerweise nicht sehr nützlich.

Jeder Winsock-Ablaufverfolgungs-Ereignistyp weist eine eindeutige Ereignis-ID im Abschnitt "System" der protokollierten Daten auf. Diese Ereignis-IDs können problemlos verwendet werden, um eine Protokolldatei nach bestimmten Winsock-Ablauf Verfolgungs Ereignissen zu filtern.

EVENTDATA enthält Informationen, die für den Ereignistyp spezifisch sind.

Der Process-Parameter in den EVENTDATA-Informationen ist die Kernel-EPROCESS-Struktur Adresse für den Prozess, nicht die tatsächliche PID. Wenn Sie ein Ereignis mit der benutzermoduspid vergleichen möchten, verwenden Sie den Wert Process aus den EVENTDATA-Informationen von einem beliebigen Protokolleintrag, und suchen Sie im Protokoll nach einem socketerstellungs-Ereignis mit dem Wert verarbeiten. Nachdem eine Entsprechung gefunden wurde, ist der letzte Parameter in den socketerstellungs-Ereignisdaten die Benutzermodusprozess-ID, die den Socket erstellt hat.

In einigen Winsock-Ablauf Verfolgungs Ereignissen wird ein Adress Parameter in den EVENTDATA-Informationen zurückgegeben. Ein Adress Parameter stellt eine IP-Adresse dar, wird jedoch in der Textdatei angezeigt, die vom **tracerpt.exe** Tool erstellt wurde, oder in Ereignisanzeige als Rohbytes oder als Zahl. IPv6-Adressen werden als hexadezimal angezeigt, sodass Sie leichter verständlich sind. IPv4-Adressen werden als große Dezimalzahl angezeigt. Entwickler müssen die Rohdaten Bytes einer IPv4-Adresse manuell in die vertraute IPv4-punktierte Adress Notation konvertieren, damit der Wert besser interpretiert werden kann.

In einigen Winsock-Ablauf Verfolgungs Ereignissen wird ein Fehler Parameter in EVENTDATA zurückgegeben. Ein Fehler Parameter hat die Form eines NTSTATUS-oder HRESULT-Fehlercodes. Dieser Fehler Parameter wird in der Textdatei angezeigt, die vom **tracerpt.exe** Tool erstellt wurde, oder in Ereignisanzeige als Dezimalzahl. Entwickler müssen die Dezimalzahl manuell in eine hexadezimale Zahl konvertieren, damit der Fehlercode in einigen Fällen besser interpretiert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung](winsock-tracing-event-details.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> </dl>

 

 
