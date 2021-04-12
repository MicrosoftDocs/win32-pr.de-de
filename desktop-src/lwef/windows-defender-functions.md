---
title: Windows Defender-Funktionen
description: Funktionen, die von apps aufgerufen werden, um Scans, Signatur Updates oder Informationen von Windows Defender anzufordern.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389792"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="493ea-103">Windows Defender-Funktionen</span><span class="sxs-lookup"><span data-stu-id="493ea-103">Windows Defender Functions</span></span>

<span data-ttu-id="493ea-104">Funktionen, die von apps aufgerufen werden, um Scans, Signatur Updates oder Informationen von Windows Defender anzufordern.</span><span class="sxs-lookup"><span data-stu-id="493ea-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="493ea-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="493ea-105">Function</span></span></th>
<th><span data-ttu-id="493ea-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="493ea-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="493ea-107"><a href="mperrormessageformat.md"><strong>Mperrormessageformat</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="493ea-108">Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-109"><a href="mpfreememory.md"><strong>Mpfrememory</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="493ea-110">Gibt Arbeitsspeicher für den Malware Schutz-Manager frei.</span><span class="sxs-lookup"><span data-stu-id="493ea-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-111"><a href="mphandleclose.md"><strong>Mplenker schließen</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="493ea-112">Schließt das von <a href="mpmanageropen.md"><strong>mpmanageropen</strong></a>, <a href="mpscanstart.md"><strong>mpscanstart</strong></a>, <a href="mpthreatopen.md"><strong>mporial Open</strong></a>oder <a href="mpupdatestart.md"><strong>mpupdatestart</strong></a>zurückgegebene Handle.</span><span class="sxs-lookup"><span data-stu-id="493ea-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-113"><a href="mpmanageropen.md"><strong>Mpmanageropen</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="493ea-114">Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.</span><span class="sxs-lookup"><span data-stu-id="493ea-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-115"><a href="mpmanagerstatusquery.md"><strong>Mpmanagerstatus Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="493ea-116"><strong>Nicht unterstützt.</strong></span><span class="sxs-lookup"><span data-stu-id="493ea-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="493ea-117">Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-118"><a href="mpmanagerstatusqueryex.md"><strong>Mpmanagerstatus-QUERYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="493ea-119">Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-120"><a href="mpmanagerversionquery.md"><strong>Mpmanagerversionquery</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="493ea-121">Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-122"><a href="mpscancontrol.md"><strong>Mpscancontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="493ea-123">Ermöglicht das Steuern einer Überprüfung, die asynchron über <a href="mpscanstart.md"><strong>mpscanstart</strong></a>initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="493ea-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-124"><a href="mpscanstart.md"><strong>Mpscanstart</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="493ea-125">Startet einen Scanvorgang.</span><span class="sxs-lookup"><span data-stu-id="493ea-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-126"><a href="mpthreatenumerate.md"><strong>Mpzerenumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="493ea-127">Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="493ea-128">Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="493ea-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-129"><a href="mpthreatopen.md"><strong>Mpbedrohlich öffnen</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="493ea-130">Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="493ea-131">Diese Funktion kann verwendet werden, um von einer bestimmten Überprüfung erkannte Bedrohungen, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder alle Bedrohungen in der Signaturdatenbank zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="493ea-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-132"><a href="mpthreatquery.md"><strong>Mpbedrohlich Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="493ea-133">Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.</span><span class="sxs-lookup"><span data-stu-id="493ea-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-134"><a href="mpupdatecontrol.md"><strong>Mpupdatecontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="493ea-135">Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über <a href="mpupdatestart.md"><strong>mpupdatestart</strong></a>initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="493ea-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-136"><a href="mpupdatestart.md"><strong>Mpupdatestart</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="493ea-137">Startet einen Signatur Aktualisierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="493ea-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="493ea-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>Wdenable</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="493ea-139">Ändert den Windows Defender-Status in ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="493ea-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="493ea-140">Ab Windows 10, Version 1607 und Windows Server 2016, gibt die <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>wdenable</strong></a> -Funktion immer <strong>E_NOTIMPL</strong>zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="493ea-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>Wdstatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="493ea-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="493ea-142">Gibt den aktuellen Status von Windows Defender zurück.</span><span class="sxs-lookup"><span data-stu-id="493ea-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





