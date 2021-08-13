---
description: Das Microsoft Windows HTTP Services(WinHTTP)-Ablaufverfolgungskonfigurationstool WinHttpTraceCfg.exe wird verwendet, um Ablaufverfolgungsfunktionen für Debug- und Paketsuchzwecke zu konfigurieren.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, ein Tool für die Ablaufverfolgungskonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7747e0b2fe023ab3c2c86d19a722059482aed19062cf2a450b8d0f237a8b3a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562413"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, ein Tool für die Ablaufverfolgungskonfiguration

Das [Microsoft Windows HTTP Services(WinHTTP)-Ablaufverfolgungskonfigurationstool](about-winhttp.md) WinHttpTraceCfg.exe wird verwendet, um Ablaufverfolgungsfunktionen für Debug- und Paketsuchzwecke zu konfigurieren. Die Fähigkeit, WinHTTP-Funktionen und den entsprechenden Netzwerkdatenverkehr zu überwachen, ist wichtig. Debuggen von Anwendungen, die verschlüsselte Wire Protocols verwenden, z. B. Secure Sockets Layer (SSL), schließen die Ermittlung von Paketen auf der Netzwerktransportebene aus und erfordern die Fähigkeit, Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde. Microsoft Windows HTTP Services (WinHTTP) bietet eine Ablaufverfolgungsfunktion, die über eine Reihe von Funktionen zum Abfangen des Datenverkehrsstroms zwischen Client und Server verfügt.

Diese Ablaufverfolgungsfunktion kann ein wertvolles Tool für das Debuggen sein. Sie kann z. B. zum Anzeigen von Parametern verwendet werden, die an verschiedene Funktionsaufrufe übergeben werden, sowie zum Anzeigen der tatsächlichen Daten, die von einer WinHTTP-Anwendung gesendet und empfangen werden.

-   [Verwenden der Ablaufverfolgungsfunktion](#using-the-trace-facility)
-   [Interpretieren von Ablaufverfolgungsdaten](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Verwenden der Ablaufverfolgungsfunktion

WinHTTP ruft Ablaufverfolgungssteuerungsparameter aus der Registrierung ab. Diese Steuerelementparameter beeinflussen, wie WinHTTP eine Ablaufverfolgungsausgabe erzeugt und wie diese Ausgabe formatiert wird. Alle Anwendungen, die WinHTTP verwenden, verwenden die gleichen Einstellungen.

Ein Konfigurationstool für die Ablaufverfolgungseinrichtung WinHttpTraceCfg.exe steht als Download auf der Website [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) zur Verfügung. Das Konfigurationstool legt die Registrierungseinstellungen der Ablaufverfolgungseinrichtung basierend auf den angegebenen Befehlszeilenparametern fest oder ruft sie ab.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

In der folgenden Tabelle sind mögliche Parameter für das Konfigurationstool aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Gibt an, ob die Ablaufverfolgungsfunktion aktiviert oder deaktiviert ist. <br/> 
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
<td><p>Gibt ein Präfix für die Protokolldatei an. Das Präfix kann einen Pfad enthalten. Die Protokolldatei wird in das aktuelle Verzeichnis oder das im Präfix angegebene Verzeichnis geschrieben und weist das folgende Format auf.</p>
<p><<em>Präfix</em> > -< <em>Anwendungsname</em> > . <em><.log-Zeit</em> ></p>
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
<td>Standardeinstellung. Zeigt Netzwerkdatenverkehr im ansi-Format (American National Standards Institute) an.</td>
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
<td><p>Gibt die maximale Größe einer Protokolldatei in Byte an, die von der Ablaufverfolgungsfunktion generiert wird. Wenn diese Option ohne Größe angegeben wird, beträgt der Mindestwert 65.535 Bytes. Wenn eine Protokolldatei die maximale Größe erreicht, wird der Inhalt der Datei gelöscht. Ablaufverfolgungsdaten werden weiterhin in die Protokolldatei geschrieben.</p></td>
</tr>
</tbody>
</table>



 

Wenn Sie das Konfigurationstool für die Ablaufverfolgungseinrichtung ausführen und keine Parameter angeben, werden die aktuellen Registrierungseinstellungen abgerufen und angezeigt.

> [!Note]  
> Protokolldateien wachsen schnell und beeinträchtigen die Anwendungsleistung. Stellen Sie sicher, dass der erforderliche Festplattenspeicher verfügbar ist, bevor Sie die Ablaufverfolgungsfunktion aktivieren.

 

## <a name="interpreting-trace-data"></a>Interpretieren von Ablaufverfolgungsdaten

Der Datenstrom der Ablaufverfolgungsfunktion spiegelt winHTTP-Funktionen wider, die in der Anwendung aufgerufen werden, sowie alle gesendeten oder empfangenen HTTP-Daten. In einigen Fällen werden auch Intern von WinHTTP aufgerufene Funktionen angezeigt.

Die folgende Abbildung zeigt einen Teil einer Protokolldatei, die von der Ablaufverfolgungsfunktion generiert wurde. Mehrere Elemente sind hervorgehoben und gekennzeichnet.

![Beispielablaufverfolgung](images/ss-tracer-wco.png)

Jede Zeile der Ablaufverfolgungsausgabe enthält Informationen in drei Spalten. Die erste Spalte zeigt das Datum und die Uhrzeit der Aufzeichnung des Eintrags an. Die zweite Spalte zeigt einen Anforderungsbezeichner (ID), der verwendet werden kann, um zwischen mehreren Anforderungen zu unterscheiden. Wenn der Protokolleintrag keiner bestimmten Anforderung entspricht, \* wird " Sitzung " in dieser Spalte \* angezeigt. Es kann hilfreich sein, die Protokolldatei basierend auf dieser ID zu sortieren, um nur Ereignisse anzuzeigen, die für eine einzelne Anforderung auftreten. Das folgende Beispiel zeigt einen Befehl, den Sie zum Sortieren der Protokolldatei verwenden können.

**findstr 00000001 LogFile.log**

Die dritte Spalte zeigt einen Funktionsaufruf, HTTP-Datenverkehr oder eine enthaltene Statusmeldung, um die Ablaufverfolgung zu interpretieren.

Wenn ein Protokolleintrag einem Funktionsaufruf entspricht, werden auch die Parameter der Funktion aufgezeichnet. Speicheradressen werden hexadezimal angezeigt, während alle anderen Werte als ASCII-Zeichenfolge angezeigt werden. Die Ablaufverfolgungsfunktion zeichnet auch die Rückgabezeit und den Wert für jede Funktion auf.

Das Format der HTTP-Daten hängt von den Registrierungseinstellungen ab, die mit dem Konfigurationstool für die Ablaufverfolgungsfunktion angegeben wurden. Wenn HTTP-Daten verschlüsselt werden, werden die entschlüsselten Daten auch in der Ablaufverfolgungsausgabe angezeigt.

 

 




