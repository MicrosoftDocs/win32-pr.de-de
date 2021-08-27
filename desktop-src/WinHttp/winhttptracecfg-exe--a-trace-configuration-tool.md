---
description: Das Microsoft Windows HTTP Services -Ablaufverfolgungskonfigurationstool (WinHTTP), WinHttpTraceCfg.exe, wird verwendet, um Ablaufverfolgungsfunktionen für Debug- und Paketsyntiffingzwecke zu konfigurieren.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, ein Tool für die Ablaufverfolgungskonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e292373c0da19be32f48d7f62f558953406e8d1b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622566"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, ein Tool für die Ablaufverfolgungskonfiguration

Das Microsoft Windows HTTP Services -Ablaufverfolgungskonfigurationstool [(WinHTTP),](about-winhttp.md) WinHttpTraceCfg.exe, wird verwendet, um Ablaufverfolgungsfunktionen für Debug- und Paketsyntiffingzwecke zu konfigurieren. Die Möglichkeit, WinHTTP-Funktionen und deren entsprechenden Netzwerkdatenverkehr zu überwachen, ist wichtig. Das Debuggen von Anwendungen, die verschlüsselte Wire Protocols wie Secure Sockets Layer (SSL) verwenden, schließt das Ausspähen von Paketen auf der Netzwerktransportschicht aus und erfordert die Möglichkeit, den Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde. Microsoft Windows HTTP Services (WinHTTP) bietet eine Ablaufverfolgungseinrichtung, die über eine Reihe von Funktionen zum Abfangen des Datenverkehrsstreams zwischen Client und Server verfügt.

Diese Ablaufverfolgungseinrichtung kann ein wertvolles Tool für das Debuggen sein. Sie kann beispielsweise verwendet werden, um Parameter, die an verschiedene Funktionsaufrufe übergeben werden, sowie zum Anzeigen der tatsächlichen Daten, die von einer WinHTTP-Anwendung gesendet und empfangen werden, anzeigen zu können.

-   [Verwenden der Ablaufverfolgungseinrichtung](#using-the-trace-facility)
-   [Interpretieren von Ablaufverfolgungsdaten](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Verwenden der Ablaufverfolgungseinrichtung

WinHTTP erhält Ablaufverfolgungssteuerungsparameter aus der Registrierung. Diese Steuerungsparameter beeinflussen, wie WinHTTP ablaufverfolgungsausgabe erzeugt und wie diese Ausgabe formatiert wird. Alle Anwendungen, die WinHTTP verwenden, verwenden dieselben Einstellungen.

Ein Tool zur Konfiguration der Ablaufverfolgungseinrichtung, WinHttpTraceCfg.exe, steht als Download auf der Windows [Server 2003 Resource Kit Tools-Website zur](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) Verfügung. Das Konfigurationstool legt die Registrierungseinstellungen der Ablaufverfolgungseinrichtung basierend auf den angegebenen Befehlszeilenparametern fest oder ruft sie ab.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

In der folgenden Tabelle sind mögliche Parameter für das Konfigurationstool aufgeführt.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Zeigt Syntaxdaten an.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Gibt an, ob die Ablaufverfolgungseinrichtung aktiviert oder deaktiviert ist. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Standardeinstellung. Deaktiviert die Ablaufverfolgung.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Aktiviert die Ablaufverfolgung</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>Gibt ein Präfix für die Protokolldatei an. Das Präfix kann einen Pfad enthalten. Die Protokolldatei wird in das aktuelle Verzeichnis oder das im Präfix angegebene Verzeichnis geschrieben und hat das folgende Format.</p>
<p><<em></em> > Präfix -< <em>Anwendungsname</em> > . <<em>time</em> > .log</p>
<p>Wenn kein Präfix angegeben wird, wird eine leere Zeichenfolge verwendet. Geben Sie &quot; * &quot; an, um ein vorhandenes Präfix zu löschen.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Gibt an, ob die Ablaufverfolgungsausgabe in einem Debugger angezeigt oder in eine Datei geschrieben wird.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Standardeinstellung. Schreibt in die Protokolldatei.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Wird in einem Debugger angezeigt.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>Gibt an, wie Netzwerkdatenverkehr (Anforderungen und Antworten) angezeigt wird.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Zeigt nur HTTP-Header an.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Standardeinstellung. Zeigt Netzwerkdatenverkehr im American National Standards Institute(ANSI)-Format an.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Zeigt Netzwerkdatenverkehr im Hexadezimalformat an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-t</td>
<td><p>Gibt an, ob Funktionsaufrufe der obersten Ebene in der Ablaufverfolgung aufgezeichnet werden.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Standardeinstellung. Funktionsaufrufe werden nicht aufgezeichnet.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Funktionsaufrufe der obersten Ebene werden aufgezeichnet.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>Gibt die maximale Größe einer Protokolldatei in Byte an, die von der Ablaufverfolgungseinrichtung generiert wird. Wenn diese Option ohne Größe angegeben wird, beträgt der Mindestwert 65.535 Bytes. Wenn eine Protokolldatei die maximale Größe erreicht, wird der Inhalt der Datei gelöscht. Ablaufverfolgungsdaten werden weiterhin in die Protokolldatei geschrieben.</p></td>
</tr>
</tbody>
</table>



 

Wenn Sie das Konfigurationstool für die Ablaufverfolgungseinrichtung ausführen und keine Parameter angeben, werden die aktuellen Registrierungseinstellungen abgerufen und angezeigt.

> [!Note]  
> Protokolldateien wachsen schnell und beeinträchtigen die Anwendungsleistung. Stellen Sie sicher, dass der erforderliche Festplattenspeicher verfügbar ist, bevor Sie die Ablaufverfolgungseinrichtung aktivieren.

 

## <a name="interpreting-trace-data"></a>Interpretieren von Ablaufverfolgungsdaten

Der Datenstrom der Ablaufverfolgungsfunktion spiegelt WinHTTP-Funktionen wider, die in der Anwendung aufgerufen werden, sowie alle gesendeten oder empfangenen HTTP-Daten. In einigen Fällen werden auch Funktionen angezeigt, die intern von WinHTTP aufgerufen werden.

Die folgende Abbildung zeigt einen Teil einer Protokolldatei, die von der Ablaufverfolgungseinrichtung generiert wurde. Mehrere Elemente sind hervorgehoben und gekennzeichnet.

![Beispiel-Ablaufverfolgung](images/ss-tracer-wco.png)

Jede Zeile der Ablaufverfolgungsausgabe enthält Informationen in drei Spalten. Die erste Spalte zeigt das Datum und die Uhrzeit der Aufzeichnung des Eintrags an. Die zweite Spalte zeigt einen Anforderungsbezeichner (ID), der verwendet werden kann, um zwischen mehreren Anforderungen zu unterscheiden. Wenn der Protokolleintrag nicht einer bestimmten Anforderung entspricht, wird \* \* "Sitzung" in dieser Spalte angezeigt. Es kann hilfreich sein, die Protokolldatei basierend auf dieser ID zu sortieren, um nur Ereignisse zu sehen, die für eine einzelne Anforderung auftreten. Das folgende Beispiel zeigt einen Befehl, den Sie zum Sortieren der Protokolldatei verwenden können.

**findstr 00000001 LogFile.log**

Die dritte Spalte zeigt einen Funktionsaufruf, HTTP-Datenverkehr oder eine Statusmeldung, die enthalten ist, um die Interpretation der Ablaufverfolgung zu unterstützen.

Wenn ein Protokolleintrag einem Funktionsaufruf entspricht, werden auch die Parameter der Funktion aufgezeichnet. Speicheradressen werden hexadezimal angezeigt, während alle anderen Werte als ASCII-Zeichenfolge angezeigt werden. Die Ablaufverfolgungsfunktion zeichnet auch die Rückgabezeit und den Wert für jede Funktion auf.

Das Format der HTTP-Daten hängt von den Registrierungseinstellungen ab, die mit dem Tool für die Konfiguration der Ablaufverfolgungseinrichtung angegeben werden. Wenn HTTP-Daten verschlüsselt werden, werden die entschlüsselten Daten auch in der Ablaufverfolgungsausgabe angezeigt.

 

 




