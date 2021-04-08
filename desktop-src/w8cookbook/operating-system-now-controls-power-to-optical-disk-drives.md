---
title: Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken
description: Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730736"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="19667-103">Betriebssystem steuert jetzt die Stromversorgung auf optischen Laufwerken</span><span class="sxs-lookup"><span data-stu-id="19667-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="19667-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="19667-104">Platforms</span></span>

<span data-ttu-id="19667-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="19667-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="19667-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19667-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="19667-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19667-107">Description</span></span>

<span data-ttu-id="19667-108">In früheren Versionen von Windows wurde die Stromversorgung des optischen Laufwerks nicht verwaltet, als das optische Laufwerk nicht verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="19667-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="19667-109">Wenn auf dem optischen Laufwerk (ungerade) kein Medium vorhanden ist, schaltet das Betriebssystem die Stromversorgung auf dem optischen Laufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="19667-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="19667-110">Diese Funktion wird als Zero Power Odd (zpodd) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="19667-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="19667-111">Diese Funktion gilt nur für optische Laufwerke, die einen Slimline SATA (Serial Advanced Technology Attachment)-Connector verwenden.</span><span class="sxs-lookup"><span data-stu-id="19667-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="19667-112">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="19667-112">Manifestation</span></span>

<span data-ttu-id="19667-113">Wir haben keine negativen Auswirkungen von diesem neuen Verhalten festgestellt. Sie sollten sich jedoch bewusst sein, da dies zu unerwartetem Verhalten von Medien-Schreibsoftware führen kann.</span><span class="sxs-lookup"><span data-stu-id="19667-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="19667-114">Minderung</span><span class="sxs-lookup"><span data-stu-id="19667-114">Mitigation</span></span>

<span data-ttu-id="19667-115">Um den AlwaysOn-Status wiederherzustellen, deaktivieren Sie diese Funktionalität in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="19667-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="19667-116">Der absolute Pfad zum Registrierungs Wert lautet:</span><span class="sxs-lookup"><span data-stu-id="19667-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="19667-117">Der Typ ist "DWORD (32 Bit)", und wenn der Wert 0 ist, wird zpodd deaktiviert. Wenn es sich um einen anderen Wert handelt, ist zpodd aktiviert.</span><span class="sxs-lookup"><span data-stu-id="19667-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="19667-118">Tests</span><span class="sxs-lookup"><span data-stu-id="19667-118">Tests</span></span>

<span data-ttu-id="19667-119">Testen Sie Ihre Medien zum Schreiben von Software auf Anomalien, die aufgrund dieses neuen Features auftreten.</span><span class="sxs-lookup"><span data-stu-id="19667-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="19667-120">[Informieren Sie Microsoft](mailto:OptIssue@microsoft.com) über Probleme, die Sie mit dieser neuen Funktion finden.</span><span class="sxs-lookup"><span data-stu-id="19667-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




