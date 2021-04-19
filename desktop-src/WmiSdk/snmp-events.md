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
# <a name="snmp-events"></a><span data-ttu-id="36d72-103">SNMP-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="36d72-103">SNMP Events</span></span>

<span data-ttu-id="36d72-104">Der SNMP-Anbieter unterstützt das Schreiben in Protokolldateien und den Debugger.</span><span class="sxs-lookup"><span data-stu-id="36d72-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="36d72-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="36d72-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="36d72-106">Eine Reihe von Registrierungs Schlüsseln und-Werten definiert die Ebene und den Typ der aktuell generierten Protokollierung:</span><span class="sxs-lookup"><span data-stu-id="36d72-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="36d72-107">Debuggen</span><span class="sxs-lookup"><span data-stu-id="36d72-107">Debugging</span></span>

    <span data-ttu-id="36d72-108">Der Registrierungsschlüssel " **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ Providers \\ Logging** " enthält den Protokollierungs Wert, der angibt, ob Informationen in den Debugger geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="36d72-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="36d72-109">Der Protokollierungs Wert wird entweder auf 0 festgelegt, um die Debugausgabe zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="36d72-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="36d72-110">Die Protokollierung ist ein reg \_ DWORD-Wert.</span><span class="sxs-lookup"><span data-stu-id="36d72-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="36d72-111">Protokollierung</span><span class="sxs-lookup"><span data-stu-id="36d72-111">Logging</span></span>

    <span data-ttu-id="36d72-112">Der Registrierungsschlüssel " **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ Providers \\ Logging \\ Wbemsnmp** " enthält alle Protokollierungs Informationen, die für den SNMP-Anbieter spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="36d72-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="36d72-113">In der folgenden Tabelle sind die Werte aufgelistet, die diesem Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="36d72-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36d72-114">Wert</span><span class="sxs-lookup"><span data-stu-id="36d72-114">Value</span></span></th>
<th><span data-ttu-id="36d72-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36d72-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36d72-116">type</span><span class="sxs-lookup"><span data-stu-id="36d72-116">Type</span></span></td>
<td><span data-ttu-id="36d72-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="36d72-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="36d72-118">Nimmt einen der folgenden Werte an:</span><span class="sxs-lookup"><span data-stu-id="36d72-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="36d72-119">&quot;File &quot; = (Standard) sendet eine Debugausgabe an eine Datei.</span><span class="sxs-lookup"><span data-stu-id="36d72-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="36d72-120">&quot;Debugger &quot; = sendet debuggingausgaben an den Debugger.</span><span class="sxs-lookup"><span data-stu-id="36d72-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36d72-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="36d72-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="36d72-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="36d72-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="36d72-123">Nimmt ganzzahlige Werte zwischen 1024 und 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="36d72-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="36d72-124">Der Wert ist die maximal zulässige Größe in Byte für die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="36d72-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="36d72-125">Wenn dieser Wert kleiner als 1024 ist, verwendet der Protokollierungs Mechanismus den Wert 1024.</span><span class="sxs-lookup"><span data-stu-id="36d72-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="36d72-126">Für diesen Wert wird eine Mindestgröße von 8 KB empfohlen.</span><span class="sxs-lookup"><span data-stu-id="36d72-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="36d72-127">Wenn die Datei die durch MaxFileSize angegebene Größe erreicht, wird dem Dateinamen das Zeichen "~" vorangestellt, und eine neue Datei wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="36d72-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="36d72-128">Daher ist der für die Protokollierung maximal erforderliche Speicherplatz doppelt so groß wie dieser Wert.</span><span class="sxs-lookup"><span data-stu-id="36d72-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36d72-129">File</span><span class="sxs-lookup"><span data-stu-id="36d72-129">File</span></span></td>
<td><span data-ttu-id="36d72-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="36d72-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="36d72-131">Definiert den Namen der Datei, an die die Debugausgabe gesendet wird, wenn der Protokollierungstyp auf ' file ' festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36d72-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="36d72-132">Der Standardwert ist ' <WBEMLOGS> \wbemsnmp.log. '.</span><span class="sxs-lookup"><span data-stu-id="36d72-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="36d72-133">Wenn das <WBEMLOGS> Verzeichnis nicht aus dem WMI-Registrierungs Abschnitt ermittelt werden kann, lautet der Standardwert "c:\wbemsnmp.log".</span><span class="sxs-lookup"><span data-stu-id="36d72-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="36d72-134">Wenn eine Freigabe verwendet wird, z. b. \\ machine\share\wbemsnmp.log oder m:\wbemsnmp.log, wobei M: \\ machine\share ist, muss das lokale System Konto, auf dem WMI ausgeführt wird, über Lese-/Schreibzugriffsrechte für \\ machine\shareverfügen.</span><span class="sxs-lookup"><span data-stu-id="36d72-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36d72-135">Ebene</span><span class="sxs-lookup"><span data-stu-id="36d72-135">Level</span></span></td>
<td><span data-ttu-id="36d72-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="36d72-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="36d72-137">Nimmt ganzzahlige Werte von 0 bis 2 ^ 32-1 an.</span><span class="sxs-lookup"><span data-stu-id="36d72-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="36d72-138">Der Wert ist eine logische Maske, die aus 32 Bits besteht.</span><span class="sxs-lookup"><span data-stu-id="36d72-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="36d72-139">Die folgenden Bitmasken werden kombiniert, um den Typ der generierten Debugausgabe zu definieren:</span><span class="sxs-lookup"><span data-stu-id="36d72-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="36d72-140">0: Aufrufen von <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> -Methoden Aufrufen des SNMP-Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="36d72-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="36d72-141">1: Implementierung des SNMP-Klassen Anbieters</span><span class="sxs-lookup"><span data-stu-id="36d72-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="36d72-142">2: <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>snbemservices</strong></a> -Methodenaufrufe des SNMP-Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="36d72-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="36d72-143">3: Implementierung des SNMP-Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="36d72-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="36d72-144">4: SNMP-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="36d72-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="36d72-145">5: SNMP SMIR</span><span class="sxs-lookup"><span data-stu-id="36d72-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="36d72-146">6: SNMP-Korrelator</span><span class="sxs-lookup"><span data-stu-id="36d72-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="36d72-147">7: SNMP-Typmapping-Code</span><span class="sxs-lookup"><span data-stu-id="36d72-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="36d72-148">8: SNMP-Threading Code</span><span class="sxs-lookup"><span data-stu-id="36d72-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="36d72-149">9: SNMP-Ereignis Anbieter Schnittstellen und-Implementierung</span><span class="sxs-lookup"><span data-stu-id="36d72-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="36d72-150">Legen Sie die Ebene auf (2 ^ 0 + 2 ^ 8 =) 257 für Vorgänge mit Aufrufen an die Methoden des SNMP-Klassen Anbieters <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> und Vorgänge mit SNMP-Threading Code fest.</span><span class="sxs-lookup"><span data-stu-id="36d72-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




