---
title: Konfigurieren der Fehler Protokollierung der HTTP Server-API
description: Die Fehler Protokollierung der HTTP-Server-API wird durch drei Registrierungs Werte unter einem HTTP- \\ Parameter Schlüssel gesteuert.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- HTTP-Server-API, Konfigurieren von Fehlerprotokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388283"
---
# <a name="configuring-http-server-api-error-logging"></a>Konfigurieren der Fehler Protokollierung der HTTP Server-API

Die Fehler Protokollierung der HTTP-Server-API wird durch drei Registrierungs Werte unter einem **http**- \\ **Parameter** Schlüssel gesteuert, der sich unter befindet:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> Der Speicherort und die Form der Konfigurationswerte können sich in zukünftigen Versionen des Windows-Betriebssystems ändern.

 

Ein Benutzer muss über Administrator-/lokale System Berechtigungen verfügen, um die Registrierungs Werte zu ändern und die Protokolldateien und den Ordner, in dem Sie enthalten sind, anzuzeigen oder zu ändern.

Konfigurationsinformationen in den Registrierungs Werten werden gelesen, wenn der HTTP-Server-API-Treiber gestartet wird. Wenn die Einstellungen geändert werden, muss der Treiber daher beendet und neu gestartet werden, um die neuen Werte zu lesen. Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:

**NET stopphttp**

**NET Start http**

Die Protokolldateien werden mithilfe der folgenden Konvention benannt:

**Httperr +** *sequencennummer* **+. log**

Beispiel: "httperr4. log".

Protokolldateien werden durchlaufen, wenn Sie die maximale Größe erreichen, die durch den Registrierungs Wert **errorlogfiletrunpeesize** festgelegt wird, und der Wert darf nicht kleiner als 1 Megabyte (MB) sein.

Wenn die Konfiguration der Fehler Protokollierung ungültig ist oder beim Schreiben in die Protokolldateien ein Fehler auftritt, wird die Ereignisprotokollierung von der HTTP-Server-API verwendet, um Administratoren zu benachrichtigen, dass die Fehler Protokollierung nicht durchgeführt wurde.

Die Registrierungs Konfigurationswerte werden in der folgenden Tabelle beschrieben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registrierungs Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>Enableerrorlogging<br/></td>
<td>Ein <strong>DWORD</strong> , das auf <strong>true</strong> festgelegt werden kann, um die Fehler Protokollierung zu aktivieren, oder <strong>false</strong> , um es zu deaktivieren. Der Standardwert ist " <strong>true</strong>".<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>Errorlogfiletrunungesize<br/></td>
<td>Ein <strong>DWORD</strong> , das die maximale Größe einer Fehlerprotokoll Datei in Bytes angibt. Der Standardwert ist 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
Der angegebene Wert darf nicht kleiner als der Standardwert sein.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>Errorloggingdir<br/></td>
<td>Eine <strong>Zeichenfolge</strong> , die den Ordner angibt, in dem die Protokolldateien der HTTP-Server-API abgelegt werden. <br/> Die HTTP-Server-API erstellt einen Unterordner mit dem Namen " &quot; Httperr" in &quot; dem angegebenen Ordner, in dem die Protokolldateien abgelegt werden. Dieser Unterordner und die Protokolldateien erhalten die gleichen Berechtigungseinstellungen. Dies bedeutet, dass Administrator-und lokale System Konten über Vollzugriff verfügen, während andere Benutzer keinen Zugriff haben.<br/> Wenn in der Registrierung kein Ordner angegeben ist, lautet der Standardordner wie folgt:<br/> &quot;%Systemroot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
Der Wert der errorloggingdir-Zeichenfolge muss ein voll qualifizierter Pfad sein, kann jedoch &quot; % systemroot% enthalten &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





