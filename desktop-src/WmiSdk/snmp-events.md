---
description: Der SNMP-Anbieter unterstützt das Schreiben in Protokolldateien und den Debugger.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: SNMP-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348887"
---
# <a name="snmp-events"></a>SNMP-Ereignisse

Der SNMP-Anbieter unterstützt das Schreiben in Protokolldateien und den Debugger.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Eine Reihe von Registrierungs Schlüsseln und-Werten definiert die Ebene und den Typ der aktuell generierten Protokollierung:

-   Debuggen

    Der Registrierungsschlüssel " **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ Providers \\ Logging** " enthält den Protokollierungs Wert, der angibt, ob Informationen in den Debugger geschrieben werden können. Der Protokollierungs Wert wird entweder auf 0 festgelegt, um die Debugausgabe zu deaktivieren Die Protokollierung ist ein reg \_ DWORD-Wert.

-   Protokollierung

    Der Registrierungsschlüssel " **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ Providers \\ Logging \\ Wbemsnmp** " enthält alle Protokollierungs Informationen, die für den SNMP-Anbieter spezifisch sind. In der folgenden Tabelle sind die Werte aufgelistet, die diesem Schlüssel zugeordnet sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td><strong>REG_SZ</strong><br/> Nimmt einen der folgenden Werte an:<br/> &quot;File &quot; = (Standard) sendet eine Debugausgabe an eine Datei.<br/> &quot;Debugger &quot; = sendet debuggingausgaben an den Debugger.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Nimmt ganzzahlige Werte zwischen 1024 und 2 ^ 32-1. Der Wert ist die maximal zulässige Größe in Byte für die Protokolldatei. Wenn dieser Wert kleiner als 1024 ist, verwendet der Protokollierungs Mechanismus den Wert 1024. Für diesen Wert wird eine Mindestgröße von 8 KB empfohlen. Wenn die Datei die durch MaxFileSize angegebene Größe erreicht, wird dem Dateinamen das Zeichen "~" vorangestellt, und eine neue Datei wird erstellt. Daher ist der für die Protokollierung maximal erforderliche Speicherplatz doppelt so groß wie dieser Wert.<br/></td>
</tr>
<tr class="odd">
<td>File</td>
<td><strong>REG_SZ</strong><br/> Definiert den Namen der Datei, an die die Debugausgabe gesendet wird, wenn der Protokollierungstyp auf ' file ' festgelegt ist. Der Standardwert ist ' <WBEMLOGS> \wbemsnmp.log. '. Wenn das <WBEMLOGS> Verzeichnis nicht aus dem WMI-Registrierungs Abschnitt ermittelt werden kann, lautet der Standardwert "c:\wbemsnmp.log". Wenn eine Freigabe verwendet wird, z. b. \\ machine\share\wbemsnmp.log oder m:\wbemsnmp.log, wobei M: \\ machine\share ist, muss das lokale System Konto, auf dem WMI ausgeführt wird, über Lese-/Schreibzugriffsrechte für \\ machine\shareverfügen.<br/></td>
</tr>
<tr class="even">
<td>Ebene</td>
<td><strong>REG_DWORD</strong><br/> Nimmt ganzzahlige Werte von 0 bis 2 ^ 32-1 an. Der Wert ist eine logische Maske, die aus 32 Bits besteht. Die folgenden Bitmasken werden kombiniert, um den Typ der generierten Debugausgabe zu definieren:<br/>
<ul>
<li>0: Aufrufen von <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> -Methoden Aufrufen des SNMP-Klassen Anbieters</li>
<li>1: Implementierung des SNMP-Klassen Anbieters</li>
<li>2: <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>snbemservices</strong></a> -Methodenaufrufe des SNMP-Instanzanbieters</li>
<li>3: Implementierung des SNMP-Instanzanbieters</li>
<li>4: SNMP-Klassenbibliothek</li>
<li>5: SNMP SMIR</li>
<li>6: SNMP-Korrelator</li>
<li>7: SNMP-Typmapping-Code</li>
<li>8: SNMP-Threading Code</li>
<li>9: SNMP-Ereignis Anbieter Schnittstellen und-Implementierung</li>
</ul>
Legen Sie die Ebene auf (2 ^ 0 + 2 ^ 8 =) 257 für Vorgänge mit Aufrufen an die Methoden des SNMP-Klassen Anbieters <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> und Vorgänge mit SNMP-Threading Code fest.<br/></td>
</tr>
</tbody>
</table>



 

 

 




