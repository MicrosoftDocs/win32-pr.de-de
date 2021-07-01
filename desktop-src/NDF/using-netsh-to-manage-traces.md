---
title: Verwenden von Netsh zum Verwalten von Ablaufverfolgungen
description: In Windows 7 können netsh.exe über eine Eingabeaufforderung verwendet werden, um Netzwerkablaufverfolgungen zu aktivieren und zu konfigurieren. In diesem Abschnitt werden einige der netsh.exe Befehle beschrieben, die bei der Behandlung von Ablaufverfolgungsproblemen hilfreich sein können, einschließlich der neuen Netsh-Ablaufverfolgungsfunktionen.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119025"
---
# <a name="using-netsh-to-manage-traces"></a>Verwenden von Netsh zum Verwalten von Ablaufverfolgungen

In Windows 7 können netsh.exe über eine Eingabeaufforderung verwendet werden, um Netzwerkablaufverfolgungen zu aktivieren und zu konfigurieren. In diesem Abschnitt werden einige der netsh.exe Befehle beschrieben, die bei der Behandlung von Ablaufverfolgungsproblemen hilfreich sein können, einschließlich der neuen **Netsh-Ablaufverfolgungsfunktionen.** Beachten Sie, dass die netsh-Befehle über eine Eingabeaufforderung mit erhöhten Rechten ausgeführt werden müssen.

## <a name="collecting-traces"></a>Erfassen von Ablaufverfolgungen

Szenarien sind vordefinierte Sätze von Ablaufverfolgungsanbietern, die für die Problembehandlung aktiviert werden können. Um die Liste der verfügbaren netzwerkbezogenen Szenarien anzuzeigen, geben Sie **netsh trace show scenarios** ein (**netsh trace show providers** lists every one of the available providers, including one that are not relevant to networking).

Wenn Sie ein Szenario identifiziert haben, das für Ihre Probleme relevant ist, sehen Sie eine Liste aller Anbieter, die in diesem Szenario enthalten sind. Um beispielsweise alle Anbieter anzuzeigen, die im InternetClient-Szenario aktiviert sind, geben Sie **netsh trace show scenario internetclient** ein.

Sie können eine Ablaufverfolgung für alle Anbieter in einem bestimmten Szenario oder einer Reihe von Szenarien starten. Um beispielsweise eine Ablaufverfolgung für alle Anbieter zu starten, die im InternetClient-Szenario aktiviert sind, geben Sie **netsh trace start scenario=internetclient** ein. Um Anbieter für mehr als ein Szenario zu erfassen, können Sie alle geeigneten Szenarien angeben, z. **B. netsh trace start scenario=FileSharing scenario=DirectAccess**. Beachten Sie, dass jeweils nur eine Ablaufverfolgungssitzung aktiviert werden kann. Es ist nicht möglich, Ablaufverfolgungsinformationen aus verschiedenen Sätzen von Anbietern gleichzeitig in separaten Dateien zu erfassen.

Sie können auch eine Ablaufverfolgung für zusätzliche Anbieter starten, die nicht in diesem bestimmten Szenario enthalten sind. Beispielsweise können Sie Ablaufverfolgungen für alle Anbieter starten, die im WLAN-Szenario aktiviert sind, sowie für den DHCP-Anbieter. Geben Sie hierzu **netsh trace start scenario=wlan provider=Microsoft-Windows-Dhcp-Client** ein.

Sie können auch weitere Details zu einem bestimmten Anbieter anzeigen, indem Sie **netsh trace show provider** gefolgt vom Anbieternamen eingeben.

Um alle verfügbaren Optionen und Filter anzuzeigen, können Sie **netsh trace start /?** eingeben.

Geben Sie **netsh trace stop** ein, um die Ablaufverfolgung zu beenden.

## <a name="using-the-output-files"></a>Verwenden der Ausgabedateien

Wenn die Ablaufverfolgung beendet wird, werden standardmäßig zwei Dateien generiert: eine ETL-Datei (Event Trace Log) und eine .cab Datei.

Ablaufverfolgungsereignisse werden in der ETL-Datei gesammelt, die mit Tools wie Netzwerkmonitor angezeigt werden kann. Die ETL-Datei erhält standardmäßig den Namen nettrace.etl, oder Sie können einen anderen Namen angeben, indem Sie **tracefile=filename.etl** beim Starten der Ablaufverfolgung einschließen.

Die .cab-Datei enthält umfassende Informationen zur Software und Hardware auf dem System, z. B. Adapterinformationen, Build, Betriebssystem und Drahtloseinstellungen. Die .cab Datei wird standardmäßig nettrace.cab benannt, es sei denn, ein anderer Name wurde wie oben angegeben angegeben.

Diese .cab Datei enthält zwei Dateien, die immer den gleichen Namen haben. Report.etl ist eine weitere Kopie der gleichen Informationen, die in nettrace.etl enthalten sind. Die datei report.html enthält zusätzliche Informationen zu den Ablaufverfolgungsereignissen und den anderen gesammelten Informationen. Um die meisten verfügbaren Details zu erhalten, schließen Sie beim Starten einer Ablaufverfolgung den Befehl **report = yes** ein.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Verwenden von Filtern zum Reduzieren der Datenmenge in der ETL-Ablaufverfolgungsdatei

Wenn Erfassungen über einen längeren Zeitraum erfolgen, kann die ETL-Ablaufverfolgungsdatei sehr groß werden. In Szenarien, in denen mehrere Anbieter aktiviert sind, was zu hohem Datenverkehr führt, können ETW-Puffereinschränkungen dazu führen, dass einige Ablaufverfolgungen gelöscht werden. Abgesehen von diesem Aspekt kann die Reduzierung der Datenmenge in der ETL-Ablaufverfolgungsdatei dazu beitragen, die Problembehandlung zu vereinfachen, indem die Menge der zu überprüfenden Daten reduziert wird.

Netsh-Ablaufverfolgungsfilter können verwendet werden, um die Größe der ETL-Ablaufverfolgungsdatei zu reduzieren. Diese Ablaufverfolgungsfilter sind ETW-Ebenen und Schlüsselwörter, die auf einzelne Anbieter angewendet werden können.

Geben Sie **netsh trace start /?** ein, um eine Liste der Filter anzuzeigen, die angewendet werden können.

Ein Beispiel für einen Filter ist **netsh trace start InternetClient provider=Microsoft-Windows-TCPIP level=5 keywords=ut:ReceivePath,ut:SendPath**.

In diesem Beispiel ist die Ebene auf 5 festgelegt, was bedeutet, dass die maximale Anzahl von Ereignissen angezeigt wird. In der folgenden Tabelle sind die verfügbaren Einstellungen aufgeführt:



| Level      | Einstellung              | Beschreibung                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Kritisch      | Nur kritische Ereignisse werden angezeigt.                                        |
| 2     | Errors        | Kritische Ereignisse und Fehler werden angezeigt.                                  |
| 3     | Warnungen      | Kritische Ereignisse, Fehler und Warnungen werden angezeigt.                       |
| 4     | Informational | Kritische Ereignisse, Fehler, Warnungen und Informationsereignisse werden angezeigt. |
| 5     | Ausführlich       | Alle Ereignisse werden angezeigt.                                                  |



 

Die Schlüsselwörter **ut:ReceivePath** und **ut:SentPath** filtern die Ereignisse so, dass nur die Ereignisse angezeigt werden, die im Empfangs- oder Sendepfad nachverfolgt werden. Eine vollständige Liste der Schlüsselwörter für einen bestimmten Anbieter finden Sie, indem Sie **netsh trace show provider** gefolgt vom Anbieternamen eingeben. Wenn Sie beispielsweise **netsh trace show provider Microsoft-Windows-TCPIP** eingeben, werden Informationen zum Microsoft-Windows-TCPIP-Anbieter angezeigt, einschließlich einer Liste von Schlüsselwörtern.

Netsh unterstützt auch die Paketfilterungsfunktion (ähnlich wie Netzwerkmonitor), wenn die Paketerfassung aktiviert ist (durch Festlegen von **capture = yes**). Die Paketfilterung kann verwendet werden, um eine begrenzte Anzahl von Paketen in einer Ablaufverfolgungsdatei zu erfassen. Beispielsweise erfasst **netsh trace start capture = yes ipv4.address == x.x.x.x** , wobei x.x.x.x die IP-Adresse ist, nur Pakete mit ipv4-Datenverkehr mit dieser bestimmten Quell- oder Zieladresse.

Um weitere Informationen zur Verwendung der Paketfilterung zu erhalten, können Sie **netsh trace show capturefilterHelp** eingeben.

 

 




