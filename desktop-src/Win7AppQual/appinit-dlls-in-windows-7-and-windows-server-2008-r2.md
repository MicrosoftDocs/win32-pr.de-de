---
description: AppInit_DLLs in Windows 7 und Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs unter Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088708"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="50017-103">\_AppInit-DLLs in Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50017-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="50017-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="50017-104">Platform</span></span>

<span data-ttu-id="50017-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="50017-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="50017-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50017-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="50017-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="50017-107">Feature Impact</span></span>

 <span data-ttu-id="50017-108">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="50017-108">**Severity** - Low</span></span>  
<span data-ttu-id="50017-109">**Häufigkeit** – Niedrig</span><span class="sxs-lookup"><span data-stu-id="50017-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="50017-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50017-110">Description</span></span>

<span data-ttu-id="50017-111">AppInit-DLLs sind ein Mechanismus, mit dem eine beliebige Liste von DLLs in jeden Benutzermodusprozess im \_ System geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="50017-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="50017-112">Microsoft ändert die AppInit-DLLs in Windows 7 und Windows Server 2008 R2, um eine neue Codesignaturanforderung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="50017-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="50017-113">Dies hilft, die Zuverlässigkeit und Leistung des Systems zu verbessern und den Einblick in den Ursprung der Software zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="50017-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="50017-114">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="50017-114">Configuration</span></span>

<span data-ttu-id="50017-115">Werte, die unter dem Windows-Schlüssel HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT CurrentVersion In der Registrierung gespeichert sind, bestimmen das Verhalten der \_ \_ \\ \\ \\ \\ \\ AppInit-DLLs-Infrastruktur. \_</span><span class="sxs-lookup"><span data-stu-id="50017-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="50017-116">In der folgenden Tabelle werden diese Registrierungswerte beschrieben:</span><span class="sxs-lookup"><span data-stu-id="50017-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="50017-117">Wert</span><span class="sxs-lookup"><span data-stu-id="50017-117">Value</span></span></th>
<th><span data-ttu-id="50017-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50017-118">Description</span></span></th>
<th><span data-ttu-id="50017-119">Beispielwerte</span><span class="sxs-lookup"><span data-stu-id="50017-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="50017-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="50017-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="50017-121">Aktiviert oder deaktiviert global AppInit_DLLs.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="50017-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="50017-122">0x0 : AppInit_DLLs sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="50017-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50017-123">0x1 : AppInit_DLLs sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="50017-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="50017-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="50017-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="50017-125">Durch Leerzeichen oder Kommas getrennte Liste der zu ladenden DLLs.</span><span class="sxs-lookup"><span data-stu-id="50017-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="50017-126">Der vollständige Pfad zur DLL sollte mithilfe von Kurznamen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50017-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="50017-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span><span class="sxs-lookup"><span data-stu-id="50017-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="50017-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="50017-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="50017-129">Nur mit Code signierte DLLs laden.${REMOVE}$</span><span class="sxs-lookup"><span data-stu-id="50017-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="50017-130">0x0: Alle DLLs werden geladen.</span><span class="sxs-lookup"><span data-stu-id="50017-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50017-131">0x1: Lädt nur mit Code signierte DLLs.</span><span class="sxs-lookup"><span data-stu-id="50017-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="50017-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="50017-132">**Windows 7**</span></span>

<span data-ttu-id="50017-133">Alle DLLs, die von der \_ AppInit-DLLs-Infrastruktur geladen werden, sollten mit Code signiert sein.</span><span class="sxs-lookup"><span data-stu-id="50017-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="50017-134">Aus Gründen der Anwendungskompatibilität lädt das Windows 7-Betriebssystem alle AppInit-DLLs.</span><span class="sxs-lookup"><span data-stu-id="50017-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="50017-135">Microsoft empfiehlt jedoch, dass alle Anwendungsentwickler ihre DLLs codesignieren, um die Zuverlässigkeit von Windows zu verbessern und die Codesignaturerzwingung in zukünftigen Versionen von Windows vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="50017-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="50017-136">Der Registrierungsschlüssel RequireSignedAppInit \_ DLLs steuert dieses Verhalten, und sein Wert unter Windows 7 ist standardmäßig auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50017-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="50017-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="50017-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="50017-138">Alle DLLs, die von der \_ AppInit-DLLs-Infrastruktur geladen werden, müssen mit Code signiert sein.</span><span class="sxs-lookup"><span data-stu-id="50017-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="50017-139">Der Registrierungsschlüssel RequireSignedAppInit \_ DLLs steuert dieses Verhalten, und sein Wert unter Windows Server 2008 R2 ist standardmäßig auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50017-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="50017-140">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="50017-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="50017-141">AppInit-DLLs unter Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50017-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
