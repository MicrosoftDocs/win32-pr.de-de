---
description: Das Microsoft Windows HTTP-Dienste (WinHTTP) Trace Configuration Tool (WinHttpTraceCfg.exe) wird verwendet, um Ablauf Verfolgungs Funktionen für das Debuggen und das paketsniffing zu konfigurieren.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, ein Konfigurations Tool für die Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349004"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, ein Konfigurations Tool für die Ablauf Verfolgung

Das [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md) Trace Configuration Tool (WinHttpTraceCfg.exe) wird verwendet, um Ablauf Verfolgungs Funktionen für das Debuggen und das paketsniffing zu konfigurieren. Die Fähigkeit zum Überwachen von WinHTTP-Funktionen und des entsprechenden Netzwerk Datenverkehrs ist wichtig. Das Debuggen von Anwendungen, die verschlüsselte Übertragungsprotokolle nutzen, wie z. b. Secure Sockets Layer (SSL), schließt das Auslagern von Paketen auf der Netzwerk Transport Ebene aus und erfordert die Möglichkeit, den Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde. Die Microsoft Windows HTTP-Dienste (WinHTTP) stellen eine Ablauf Verfolgungs Funktion bereit, die über eine Reihe von Funktionen für das Abfangen des Datenverkehrs zwischen dem Client und dem Server verfügt.

Diese Ablauf Verfolgungs Funktion kann ein wertvolles Tool für das Debuggen sein. Sie kann z. b. verwendet werden, um Parameter anzuzeigen, die an verschiedene Funktionsaufrufe übermittelt werden, sowie um tatsächliche, von einer WinHTTP-Anwendung gesendete und empfangene Daten anzuzeigen.

-   [Verwenden der Ablauf Verfolgungs Funktion](#using-the-trace-facility)
-   [Interpretieren von Ablauf Verfolgungs Daten](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Verwenden der Ablauf Verfolgungs Funktion

WinHTTP ruft Ablauf Verfolgungs Steuerungsparameter aus der Registrierung ab. Diese Steuerelement Parameter beeinflussen, wie WinHTTP eine Ablauf Verfolgungs Ausgabe erzeugt und wie diese Ausgabe formatiert wird. Alle Anwendungen, die WinHTTP verwenden, verwenden die gleichen Einstellungen.

Ein Konfigurationstool für die Ablauf Verfolgungs Einrichtung (WinHttpTraceCfg.exe) ist als Download auf der [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) -Website verfügbar. Das-Konfigurationstool legt die Registrierungs Einstellungen für die Ablauf Verfolgungs Einrichtung basierend auf den angegebenen Befehlszeilen Parametern fest oder ruft Sie ab.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

In der folgenden Tabelle sind die möglichen Parameter für das-Konfigurationstool aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Zeigt Syntax Daten an.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Gibt an, ob die Ablauf Verfolgungs Funktion aktiviert oder deaktiviert ist. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Standardeinstellung. Deaktiviert die Ablauf Verfolgung.</td>
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
<td><p>Gibt ein Präfix für die Protokolldatei an. Das Präfix kann einen Pfad enthalten. Die Protokolldatei wird in das aktuelle Verzeichnis oder das im Präfix angegebene Verzeichnis geschrieben und weist das folgende Format auf.</p>
<p><<em>Präfix</em> > -< <em>Anwendungsname</em> > . <<em>time</em> > . log</p>
<p>Wenn kein Präfix angegeben ist, wird eine leere Zeichenfolge verwendet. Gibt &quot; * &quot; an, dass ein vorhandenes Präfix gelöscht wird.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Gibt an, ob die Ausgabe der Ablauf Verfolgung in einem Debugger angezeigt oder in eine Datei geschrieben wird.</p>

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
<td><p>Gibt an, wie Netzwerk Datenverkehr (Anforderungen und Antworten) angezeigt wird.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Zeigt nur HTTP-Header an.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Standardeinstellung. Zeigt den Netzwerk Datenverkehr im American National Standards Institute (ANSI)-Format an.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Zeigt den Netzwerk Datenverkehr im Hexadezimal Format an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-t</td>
<td><p>Gibt an, ob Funktionsaufrufe der obersten Ebene in der Ablauf Verfolgung aufgezeichnet werden.</p>

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
<td><p>Gibt die maximale Größe (in Bytes) einer Protokolldatei an, die von der Ablauf Verfolgungs Funktion generiert wird. Wenn diese Option ohne Größe angegeben wird, beträgt der Mindestwert 65.535 bytes. Wenn eine Protokolldatei die maximale Größe erreicht, wird der Inhalt der Datei gelöscht. Ablauf Verfolgungs Daten werden weiterhin in die Protokolldatei geschrieben.</p></td>
</tr>
</tbody>
</table>



 

Wenn Sie das Konfigurationstool für die Ablauf Verfolgungs Einrichtung ausführen und keine Parameter angeben, werden die aktuellen Registrierungs Einstellungen abgerufen und angezeigt.

> [!Note]  
> Protokolldateien werden schnell vergrößert und beeinträchtigen die Anwendungsleistung. Stellen Sie sicher, dass der erforderliche Festplattenspeicher verfügbar ist, bevor Sie die Ablauf Verfolgungs Funktion aktivieren.

 

## <a name="interpreting-trace-data"></a>Interpretieren von Ablauf Verfolgungs Daten

Der Datenstrom der Ablauf Verfolgungs Einrichtung reflektiert die in der Anwendung aufgerufenen WinHTTP-Funktionen und alle gesendeten oder empfangenen HTTP-Daten. In einigen Fällen werden auch Funktionen angezeigt, die intern von WinHTTP aufgerufen werden.

Die folgende Abbildung zeigt einen Teil einer Protokolldatei, die von der Ablauf Verfolgungs Funktion generiert wurde. Mehrere Elemente werden hervorgehoben und bezeichnet.

![Beispiel Ablauf Verfolgung](images/ss-tracer-wco.png)

Jede Zeile der Ablauf Verfolgungs Ausgabe enthält Informationen in drei Spalten. Die erste Spalte zeigt das Datum und die Uhrzeit der Aufzeichnung des Eintrags an. In der zweiten Spalte wird eine Anforderungs Kennung (ID) angezeigt, die zur Unterscheidung zwischen mehreren Anforderungen verwendet werden kann. Wenn der Protokolleintrag nicht mit einer bestimmten Anforderung übereinstimmt, \* \* wird in dieser Spalte "Session" angezeigt. Es kann nützlich sein, die Protokolldatei auf Grundlage dieser ID zu sortieren, um nur Ereignisse anzuzeigen, die für eine einzelne Anforderung auftreten. Das folgende Beispiel zeigt einen Befehl, den Sie zum Sortieren der Protokolldatei verwenden können.

**findstr 00000001 Logfile. log**

Die dritte Spalte zeigt einen Funktions-und HTTP-Datenverkehr oder eine Statusmeldung, die zur Interpretation der Ablauf Verfolgung enthalten ist.

Wenn ein Protokolleintrag einem Funktions aufzurufen entspricht, werden die Parameter der Funktion ebenfalls aufgezeichnet. Speicheradressen werden als hexadezimal angezeigt, während alle anderen Werte als ASCII-Zeichenfolge angezeigt werden. Die Ablauf Verfolgungs Funktion zeichnet auch die Rückgabezeit und den Wert für jede Funktion auf.

Das Format der HTTP-Daten hängt von den Registrierungs Einstellungen ab, die mit dem Konfigurationstool für die Ablauf Verfolgungs Einrichtung angegeben werden Wenn HTTP-Daten verschlüsselt werden, werden die entschlüsselten Daten auch in der Ausgabe der Ablauf Verfolgung angezeigt.

 

 




