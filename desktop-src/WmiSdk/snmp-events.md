---
description: Der SNMP-Anbieter unterstützt das Schreiben in Protokolldateien und in den Debugger.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: SNMP-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925ce6bb5eca0a3c067470255296ba6c9f66c0183b2b74aa6cfa4a25824446d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816646"
---
# <a name="snmp-events"></a>SNMP-Ereignisse

Der SNMP-Anbieter unterstützt das Schreiben in Protokolldateien und in den Debugger.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Eine Reihe von Registrierungsschlüsseln und -werten definiert die Ebene und den Typ der aktuell generierten Protokollierung:

-   Debuggen

    Der Registrierungsschlüssel **HKEY \_ LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM \\ PROVIDERS \\ LOGGING** enthält den Protokollierungswert, der angibt, ob Informationen in den Debugger geschrieben werden können. Der Protokollierungswert wird entweder auf 0 festgelegt, um die Debugausgabe zu deaktivieren, oder auf 1, um ihn zu aktivieren. Die Protokollierung ist ein REG \_ DWORD-Wert.

-   Protokollierung

    Der **Registrierungsschlüssel HKEY \_ LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM \\ PROVIDERS LOGGING \\ \\ WBEMSNMP** enthält alle Protokollierungsinformationen, die für den SNMP-Anbieter spezifisch sind. In der folgenden Tabelle sind die diesem Schlüssel zugeordneten Werte aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Typ</td>
<td><strong>REG_SZ</strong><br/> Übernimmt einen der folgenden Werte:<br/> &quot;File &quot; = (Standard) Sendet die Debugausgabe an eine Datei.<br/> &quot;Debugger &quot; = Sendet die Debugausgabe an den Debugger.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Akzeptiert ganzzahlige Werte von 1024 bis 2^32-1. Der Wert ist die maximal zulässige Größe in Bytes für die Protokolldatei. Wenn der Wert kleiner als 1024 ist, verwendet der Protokollierungsmechanismus den Wert 1024. Für diesen Wert wird eine Mindestgröße von 8 KB empfohlen. Wenn die Datei die von MaxFileSize angegebene Größe erreicht, wird dem Dateinamen ein ~-Zeichen voran gestellt, und eine neue Datei wird erstellt. Daher ist der maximale Speicherplatz, der für die Protokollierung erforderlich ist, doppelt so hoch wie dieser Wert.<br/></td>
</tr>
<tr class="odd">
<td>Datei</td>
<td><strong>REG_SZ</strong><br/> Definiert den Namen der Datei, an die die Debugausgabe gesendet wird, wenn der Protokollierungstyp auf "File" festgelegt ist. Der Standardwert ist <WBEMLOGS> "\wbemsnmp.log". Wenn das <WBEMLOGS> Verzeichnis nicht über den WMI-Registrierungsabschnitt bestimmt werden kann, wird standardmäßig der Wert "c:\wbemsnmp.log" verwendet. Wenn eine Freigabe verwendet wird, z. B. \\ computer\share\wbemsnmp.log oder M:\wbemsnmp.log, wobei M: \\ computer\share ist, muss das lokale SYSTEM-Konto, unter dem WMI ausgeführt wird, über Lese-/Schreibzugriffsrechte für den \\ Computer\die Freigabe verfügen.<br/></td>
</tr>
<tr class="even">
<td>Ebene</td>
<td><strong>REG_DWORD</strong><br/> Akzeptiert ganzzahlige Werte von 0 bis 2^32-1. Der Wert ist eine logische Maske, die aus 32 Bits besteht. Die folgenden Bitmasken werden kombiniert, um den Typ der generierten Debugausgabe zu definieren:<br/>
<ul>
<li>0: Aufrufe der <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices-Methode</strong></a> des SNMP-Klassenanbieters</li>
<li>1: Implementierung des SNMP-Klassenanbieters</li>
<li>2: Aufrufe der <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices-Methode</strong></a> des SNMP-Instanzanbieters</li>
<li>3: Implementierung des SNMP-Instanzanbieters</li>
<li>4: SNMP-Klassenbibliothek</li>
<li>5: SNMP SMIR</li>
<li>6: SNMP-Korrelator</li>
<li>7: SNMP-Typzuordnungscode</li>
<li>8: SNMP-Threadingcode</li>
<li>9: Schnittstellen und Implementierung von SNMP-Ereignisanbietern</li>
</ul>
Legen Sie Level für Vorgänge, die Aufrufe der <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices-Methoden</strong></a> des SNMP-Klassenanbieters und Vorgänge mit SNMP-Threadingcode betreffen, auf (2^0 + 2^8=) 257 fest.<br/></td>
</tr>
</tbody>
</table>



 

 

 




