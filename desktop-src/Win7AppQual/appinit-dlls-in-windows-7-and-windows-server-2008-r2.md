---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363415"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="8d6ca-103">AppInit \_ -DLLs in Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d6ca-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="8d6ca-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="8d6ca-104">Platform</span></span>

<span data-ttu-id="8d6ca-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d6ca-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="8d6ca-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d6ca-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="8d6ca-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="8d6ca-107">Feature Impact</span></span>

 <span data-ttu-id="8d6ca-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="8d6ca-108">**Severity** - Low</span></span>  
<span data-ttu-id="8d6ca-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="8d6ca-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="8d6ca-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d6ca-110">Description</span></span>

<span data-ttu-id="8d6ca-111">Bei AppInit- \_ DLLs handelt es sich um einen Mechanismus, mit dem eine beliebige Liste von DLLs in jeden Benutzermodusprozess auf dem System geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="8d6ca-112">Microsoft ändert die AppInit-DLLs-Funktion in Windows 7 und Windows Server 2008 R2, um eine neue Code Signatur Anforderung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="8d6ca-113">Dadurch wird die Zuverlässigkeit und Leistung des Systems verbessert, und der Einblick in den Ursprung der Software wird verbessert.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="8d6ca-114">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8d6ca-114">Configuration</span></span>

<span data-ttu-id="8d6ca-115">Werte, die unter der HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key in der Registrierung gespeichert sind, bestimmen das Verhalten der AppInit- \_ DLLs-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="8d6ca-116">In der folgenden Tabelle werden diese Registrierungs Werte beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8d6ca-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8d6ca-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8d6ca-117">Value</span></span></th>
<th><span data-ttu-id="8d6ca-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d6ca-118">Description</span></span></th>
<th><span data-ttu-id="8d6ca-119">Beispielwerte</span><span class="sxs-lookup"><span data-stu-id="8d6ca-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="8d6ca-120">LoadAppInit_DLLs (REG_DWORD) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8d6ca-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="8d6ca-121">Hiermit werden AppInit_DLLs. $ {Remove} $ global aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8d6ca-122">0x0 – AppInit_DLLs sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d6ca-123">0x1 – AppInit_DLLs aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="8d6ca-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="8d6ca-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="8d6ca-125">Durch Trennzeichen getrennte Liste der zu ladenden DLLs.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="8d6ca-126">Der gesamte Pfad zur DLL sollte mithilfe von Kurznamen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="8d6ca-127">C:\ PROGRA ~ 1 \ WID288 ~ 1 \ Micros ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="8d6ca-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="8d6ca-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8d6ca-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="8d6ca-129">Nur Code signierte DLLs laden. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="8d6ca-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="8d6ca-130">0x0 – laden Sie alle DLLs.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d6ca-131">0x1 – nur Code signierte DLLs laden.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="8d6ca-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="8d6ca-132">**Windows 7**</span></span>

<span data-ttu-id="8d6ca-133">Alle DLLs, die von der AppInit- \_ DLLs-Infrastruktur geladen werden, sollten Code signiert sein.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="8d6ca-134">Im Interesse der Anwendungs Kompatibilität lädt das Windows 7-Betriebs System alle AppInit-DLLs.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="8d6ca-135">Microsoft empfiehlt jedoch, dass alle Anwendungsentwickler ihre DLLs Code signieren, um die Zuverlässigkeit von Windows zu verbessern und die Code Signatur in zukünftigen Versionen von Windows vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="8d6ca-136">Der Registrierungsschlüssel "Requirements signetdappinit \_ DLLs" steuert dieses Verhalten, und sein Wert unter Windows 7 ist standardmäßig auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="8d6ca-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d6ca-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="8d6ca-138">Alle DLLs, die von der AppInit- \_ DLLs-Infrastruktur geladen werden, müssen Code signiert sein.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="8d6ca-139">Der Registrierungsschlüssel "Requirements signetdappinit \_ DLLs" steuert dieses Verhalten, und sein Wert unter Windows Server 2008 R2 ist standardmäßig auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d6ca-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8d6ca-140">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d6ca-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="8d6ca-141">AppInit-DLLs in Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d6ca-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
