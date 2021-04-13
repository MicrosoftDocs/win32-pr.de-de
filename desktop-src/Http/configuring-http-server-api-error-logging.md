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
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="bf3f4-104">Konfigurieren der Fehler Protokollierung der HTTP Server-API</span><span class="sxs-lookup"><span data-stu-id="bf3f4-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="bf3f4-105">Die Fehler Protokollierung der HTTP-Server-API wird durch drei Registrierungs Werte unter einem **http**- \\ **Parameter** Schlüssel gesteuert, der sich unter befindet:</span><span class="sxs-lookup"><span data-stu-id="bf3f4-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="bf3f4-106">Der Speicherort und die Form der Konfigurationswerte können sich in zukünftigen Versionen des Windows-Betriebssystems ändern.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="bf3f4-107">Ein Benutzer muss über Administrator-/lokale System Berechtigungen verfügen, um die Registrierungs Werte zu ändern und die Protokolldateien und den Ordner, in dem Sie enthalten sind, anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="bf3f4-108">Konfigurationsinformationen in den Registrierungs Werten werden gelesen, wenn der HTTP-Server-API-Treiber gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="bf3f4-109">Wenn die Einstellungen geändert werden, muss der Treiber daher beendet und neu gestartet werden, um die neuen Werte zu lesen.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="bf3f4-110">Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:</span><span class="sxs-lookup"><span data-stu-id="bf3f4-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="bf3f4-111">**NET stopphttp**</span><span class="sxs-lookup"><span data-stu-id="bf3f4-111">**net stop http**</span></span>

<span data-ttu-id="bf3f4-112">**NET Start http**</span><span class="sxs-lookup"><span data-stu-id="bf3f4-112">**net start http**</span></span>

<span data-ttu-id="bf3f4-113">Die Protokolldateien werden mithilfe der folgenden Konvention benannt:</span><span class="sxs-lookup"><span data-stu-id="bf3f4-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="bf3f4-114">**Httperr +** *sequencennummer* **+. log**</span><span class="sxs-lookup"><span data-stu-id="bf3f4-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="bf3f4-115">Beispiel: "httperr4. log".</span><span class="sxs-lookup"><span data-stu-id="bf3f4-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="bf3f4-116">Protokolldateien werden durchlaufen, wenn Sie die maximale Größe erreichen, die durch den Registrierungs Wert **errorlogfiletrunpeesize** festgelegt wird, und der Wert darf nicht kleiner als 1 Megabyte (MB) sein.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="bf3f4-117">Wenn die Konfiguration der Fehler Protokollierung ungültig ist oder beim Schreiben in die Protokolldateien ein Fehler auftritt, wird die Ereignisprotokollierung von der HTTP-Server-API verwendet, um Administratoren zu benachrichtigen, dass die Fehler Protokollierung nicht durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="bf3f4-118">Die Registrierungs Konfigurationswerte werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf3f4-119">Registrierungs Wert</span><span class="sxs-lookup"><span data-stu-id="bf3f4-119">Registry Value</span></span></th>
<th><span data-ttu-id="bf3f4-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf3f4-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf3f4-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>Enableerrorlogging</span><span class="sxs-lookup"><span data-stu-id="bf3f4-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="bf3f4-122">Ein <strong>DWORD</strong> , das auf <strong>true</strong> festgelegt werden kann, um die Fehler Protokollierung zu aktivieren, oder <strong>false</strong> , um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="bf3f4-123">Der Standardwert ist " <strong>true</strong>".</span><span class="sxs-lookup"><span data-stu-id="bf3f4-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3f4-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>Errorlogfiletrunungesize</span><span class="sxs-lookup"><span data-stu-id="bf3f4-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="bf3f4-125">Ein <strong>DWORD</strong> , das die maximale Größe einer Fehlerprotokoll Datei in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="bf3f4-126">Der Standardwert ist 1 MB (0x100000).</span><span class="sxs-lookup"><span data-stu-id="bf3f4-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf3f4-127">Der angegebene Wert darf nicht kleiner als der Standardwert sein.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf3f4-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>Errorloggingdir</span><span class="sxs-lookup"><span data-stu-id="bf3f4-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="bf3f4-129">Eine <strong>Zeichenfolge</strong> , die den Ordner angibt, in dem die Protokolldateien der HTTP-Server-API abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="bf3f4-130">Die HTTP-Server-API erstellt einen Unterordner mit dem Namen " &quot; Httperr" in &quot; dem angegebenen Ordner, in dem die Protokolldateien abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="bf3f4-131">Dieser Unterordner und die Protokolldateien erhalten die gleichen Berechtigungseinstellungen. Dies bedeutet, dass Administrator-und lokale System Konten über Vollzugriff verfügen, während andere Benutzer keinen Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="bf3f4-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="bf3f4-132">Wenn in der Registrierung kein Ordner angegeben ist, lautet der Standardordner wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf3f4-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="bf3f4-133">&quot;%Systemroot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="bf3f4-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf3f4-134">Der Wert der errorloggingdir-Zeichenfolge muss ein voll qualifizierter Pfad sein, kann jedoch &quot; % systemroot% enthalten &quot; .</span><span class="sxs-lookup"><span data-stu-id="bf3f4-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





