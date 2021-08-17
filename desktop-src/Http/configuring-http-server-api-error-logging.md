---
title: Konfigurieren der HTTP-Server-API-Fehlerprotokollierung
description: Die HTTP-Server-API-Fehlerprotokollierung wird durch drei Registrierungswerte unter einem \\ HTTP-Parameterschlüssel gesteuert.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- HTTP-Server-API, Konfigurieren von Fehlerprotokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10479a1b2bd1ebf559213b6cd4b738f6c0b9ea63c142edcce3c10f64f877dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950889"
---
# <a name="configuring-http-server-api-error-logging"></a>Konfigurieren der HTTP-Server-API-Fehlerprotokollierung

Die HTTP-Server-API-Fehlerprotokollierung wird von drei Registrierungswerten unter einem **HTTP-Parameterschlüssel** \\  gesteuert, der sich unter befindet:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> Der Speicherort und die Form der Konfigurationswerte können sich in zukünftigen Versionen des Windows Betriebssystems ändern.

 

Ein Benutzer muss über Administrator-/Lokale Systemberechtigungen verfügen, um die Registrierungswerte zu ändern und die Protokolldateien und den Ordner, in dem sie enthalten sind, anzuzeigen oder zu ändern.

Konfigurationsinformationen in den Registrierungswerten werden gelesen, wenn der HTTP Server-API-Treiber gestartet wird. Wenn die Einstellungen geändert werden, muss der Treiber daher angehalten und neu gestartet werden, um die neuen Werte zu lesen. Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:

**net stop http**

**net start http**

Die Protokolldateien werden mithilfe der folgenden Konvention benannt:

**httperr +** *SequenceNumber* **+ .log**

Beispiel: "httperr4.log".

Protokolldateien werden zyklust, wenn sie die maximale Größe erreichen, die durch den **Registrierungswert ErrorLogFileTruncateSize** angegeben wird, und der Wert darf nicht kleiner als ein Megabyte (MB) sein.

Wenn die Konfiguration der Fehlerprotokollierung ungültig ist oder beim Schreiben in die Protokolldateien ein Fehler auftritt, verwendet die HTTP-Server-API die Ereignisprotokollierung, um Administratoren darüber zu informieren, dass die Fehlerprotokollierung nicht erfolgt ist.

Registrierungskonfigurationswerte werden in der folgenden Tabelle beschrieben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Registrierungswert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Ein <strong>DWORD,</strong> das auf <strong>TRUE</strong> festgelegt werden kann, um die Fehlerprotokollierung zu aktivieren, oder <strong>FALSE,</strong> um es zu deaktivieren. Der Standardwert ist <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td>Ein <strong>DWORD,</strong> das die maximale Größe einer Fehlerprotokolldatei in Bytes angibt. Der Standardwert ist 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
Der angegebene Wert darf nicht kleiner als der Standardwert sein.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td>Eine <strong>Zeichenfolge,</strong> die den Ordner angibt, unter dem die HTTP-Server-API ihre Protokollierungsdateien platziert. <br/> Die HTTP-Server-API erstellt einen Unterordner mit dem Namen &quot; HTTPERR &quot; unter dem angegebenen Ordner, in dem die Protokolldateien abgelegt werden. Dieser Unterordner und die Protokolldateien erhalten die gleichen Berechtigungseinstellungen. Dies bedeutet, dass Administrator- und lokale Systemkonten vollzugriff haben, während andere Benutzer keinen Zugriff haben.<br/> Wenn in der Registrierung kein Ordner angegeben ist, lautet der Standardordner wie folgt:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
Der ErrorLoggingDir-Zeichenfolgenwert muss ein vollqualifizierter Pfad sein, kann jedoch &quot; %SystemRoot% &quot; enthalten.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





