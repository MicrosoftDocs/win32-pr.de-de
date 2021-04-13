---
title: Verwenden von netsh zum Verwalten von Ablauf Verfolgungen
description: In Windows 7 können netsh.exe über eine Eingabeaufforderung zum Aktivieren und Konfigurieren von Netzwerk Ablauf Verfolgungen verwendet werden. In diesem Abschnitt werden einige der netsh.exe Befehle beschrieben, die bei der Behandlung von Problemen bei der Ablauf Verfolgung helfen können, einschließlich der neuen Netsh-Ablauf Verfolgungs Funktion.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1978345da984ac90699b5355b36af18b9b285d5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388378"
---
# <a name="using-netsh-to-manage-traces"></a>Verwenden von netsh zum Verwalten von Ablauf Verfolgungen

In Windows 7 können netsh.exe über eine Eingabeaufforderung zum Aktivieren und Konfigurieren von Netzwerk Ablauf Verfolgungen verwendet werden. In diesem Abschnitt werden einige der netsh.exe Befehle beschrieben, die bei der Behandlung von Problemen bei der Ablauf Verfolgung helfen können, einschließlich der neuen **netsh** -Ablauf Verfolgungs Funktion. Beachten Sie, dass die Netsh-Befehle an einer Eingabeaufforderung mit erhöhten Rechten ausgeführt werden müssen.

## <a name="collecting-traces"></a>Sammeln von Ablauf Verfolgungen

Szenarios sind vordefinierte Sätze von Ablauf Verfolgungs Anbietern, die für die Problembehandlung aktiviert werden können. Zum Anzeigen der Liste der verfügbaren netzwerkbezogenen Szenarios geben Sie **Netsh Trace Show Szenarios** ein (**Netsh Trace Show Providers** listet alle verfügbaren Anbieter auf, einschließlich derjenigen, die für das Netzwerk nicht relevant sind).

Wenn Sie ein Szenario identifiziert haben, das für Ihre Probleme relevant ist, können Sie eine Liste aller in diesem Szenario enthaltenen Anbieter sehen. Wenn Sie z. b. alle Anbieter anzeigen möchten, die im Internet Client Szenario aktiviert sind, geben Sie **Netsh Trace Show Scenario Internet Client deklarieren** ein.

Sie können eine Ablauf Verfolgung für alle Anbieter in einem bestimmten Szenario oder einer Reihe von Szenarien starten. Wenn Sie z. b. eine Ablauf Verfolgung für alle unter dem Internet Client-Szenario aktivierten Anbieter starten möchten, geben Sie **Netsh Trace Start Scenario = Internetclient** ein. Um Anbieter für mehr als ein Szenario zu erfassen, können Sie alle geeigneten Szenarien angeben, z. b. **Netsh Trace Start Scenario = Filesharing Scenario = DirectAccess**. Beachten Sie, dass jeweils nur eine Ablauf Verfolgungs Sitzung aktiviert werden kann. Es ist nicht möglich, Ablauf Verfolgungs Informationen aus unterschiedlichen Sätzen von Anbietern in separaten Dateien gleichzeitig zu erfassen.

Sie können auch eine Ablauf Verfolgung für zusätzliche Anbieter starten, die nicht in diesem speziellen Szenario enthalten sind. Beispielsweise können Sie Ablauf Verfolgungen für alle Anbieter starten, die im WLAN-Szenario aktiviert sind, und auch den DHCP-Anbieter. Geben Sie hierzu **Netsh Trace Start Scenario = WLAN Provider = Microsoft-Windows-DHCP-Client** ein.

Sie können auch weitere Details zu einem bestimmten Anbieter anzeigen, indem Sie **Netsh Trace Show Provider** gefolgt vom Anbieter Namen eingeben.

Wenn Sie alle verfügbaren Optionen und Filter anzeigen möchten, können Sie **Netsh Trace Start/?** eingeben.

Um die Ablauf Verfolgung zu verhindern, geben Sie **Netsh Trace stoppein**.

## <a name="using-the-output-files"></a>Verwenden der Ausgabedateien

Wenn die Ablauf Verfolgung beendet wird, werden standardmäßig zwei Dateien generiert: eine ETL-Datei (Event Trace Log) und eine CAB-Datei.

Ablauf Verfolgungs Ereignisse werden in der ETL-Datei gesammelt, die mithilfe von Tools wie Netzwerkmonitor angezeigt werden kann. Die ETL-Datei erhält standardmäßig den Namen NetTrace. ETL, oder Sie können einen anderen Namen angeben, indem Sie **Tracefile = filename. ETL** beim Starten der Ablauf Verfolgung einschließen.

Die CAB-Datei enthält umfangreiche Informationen über die Software und Hardware im System, z. b. die Adapter Informationen, Build-, Betriebssystem-und drahtlos Einstellungen. Die CAB-Datei wird standardmäßig nettrace.cab benannt, es sei denn, wie oben angegeben, wurde ein anderer Name angegeben.

Diese CAB-Datei enthält zwei Dateien, die immer denselben Namen haben. "Report. ETL" ist eine weitere Kopie derselben Informationen, die in "NetTrace. ETL" enthalten sind. Die report.html-Datei enthält zusätzliche Informationen zu den Ablauf Verfolgungs Ereignissen und den anderen gesammelten Informationen. Um die verfügbaren Details zu erhalten, schließen Sie den Befehl **Report = Yes** ein, wenn Sie eine Ablauf Verfolgung starten.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Verwenden von Filtern, um die Datenmenge in der ETL-Ablauf Verfolgungs Datei zu reduzieren

Wenn Aufzeichnungen über einen längeren Zeitraum hinweg erfolgen, kann die ETL-Ablauf Verfolgungs Datei sehr groß werden. In Szenarien, in denen mehrere Anbieter aktiviert sind, was zu hohem Datenverkehr führt, können etw-Puffer Einschränkungen dazu führen, dass einige Ablauf Verfolgungen gelöscht werden. Abgesehen von dieser Überlegung kann das Verringern der Datenmenge in der ETL-Ablauf Verfolgungs Datei helfen, die Problembehandlung zu vereinfachen, indem die zu überprüfende Datenmenge reduziert wird.

Netsh-Ablauf Verfolgungs Filter können verwendet werden, um die Größe der ETL-Ablauf Verfolgungs Datei zu verringern. Diese Ablauf Verfolgungs Filter sind etw-Ebenen und-Schlüsselwörter, die auf einzelne Anbieter angewendet werden können.

Geben Sie **Netsh Trace Start/?** ein, um eine Liste der Filter anzuzeigen, die angewendet werden können.

Ein Beispiel für einen Filter ist **Netsh Trace Start Internetclient Provider = Microsoft-Windows-tcpip Level = 5 Keywords = UT: receivepath, UT: sendpath**.

In diesem Beispiel ist die Ebene auf 5 festgelegt, was bedeutet, dass die maximale Anzahl von Ereignissen angezeigt wird. In der folgenden Tabelle sind die verfügbaren Einstellungen aufgeführt:



|       |               |                                                                            |
|-------|---------------|----------------------------------------------------------------------------|
| Ebene | Einstellung       | BESCHREIBUNG                                                                |
| 1     | Kritisch      | Es werden nur kritische Ereignisse angezeigt.                                        |
| 2     | Errors        | Kritische Ereignisse und Fehler werden angezeigt.                                  |
| 3     | Warnungen      | Wichtige Ereignisse, Fehler und Warnungen werden angezeigt.                       |
| 4     | Informational | Wichtige Ereignisse, Fehler, Warnungen und Informations Ereignisse werden angezeigt. |
| 5     | Ausführlich       | Alle Ereignisse werden angezeigt.                                                  |



 

Mit den Schlüsselwörtern **UT: receivepath** und **UT: sentpath** werden die Ereignisse gefiltert, sodass nur die Ereignisse angezeigt werden, die auf dem Empfangs-oder sende Pfad verfolgt werden. Eine umfassende Liste mit Schlüsselwörtern für einen bestimmten Anbieter finden Sie unter " **Netsh Trace Show Provider** " gefolgt vom Anbieter Namen. Wenn Sie z. **b. Netsh Trace Show Provider Microsoft-Windows-tcpip** eingeben, werden Informationen zum Microsoft-Windows-tcpip-Anbieter angezeigt, einschließlich einer Liste von Schlüsselwörtern.

Netsh unterstützt auch die Funktion zum Filtern von Paketen (ähnlich wie bei Netzwerkmonitor), wenn die Paket Erfassung aktiviert ist (durch Festlegen von **Capture = Yes**). Die Paketfilterung kann verwendet werden, um eine begrenzte Anzahl von Paketen in einer Ablauf Verfolgungs Datei aufzuzeichnen. Beispiel: **Netsh Trace Start Capture = Yes IPv4. Address = = x. x. x. x** , wobei x. x. x. x die IP-Adresse ist, erfasst nur Pakete mit IPv4-Datenverkehr mit dieser bestimmten Quell-oder Zieladresse.

Weitere Informationen zur Verwendung der Paketfilterung erhalten Sie, wenn Sie **Netsh Trace Show capturefilterhelp** eingeben.

 

 




