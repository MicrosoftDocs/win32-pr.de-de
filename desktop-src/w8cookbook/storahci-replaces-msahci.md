---
title: Storahci ersetzt msahci
description: Storahci ersetzt msahci
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106341968"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="4e55a-103">Storahci ersetzt msahci</span><span class="sxs-lookup"><span data-stu-id="4e55a-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="4e55a-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="4e55a-104">Platforms</span></span>

<span data-ttu-id="4e55a-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="4e55a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="4e55a-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e55a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="4e55a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e55a-107">Description</span></span>

<span data-ttu-id="4e55a-108">Storahci, ein Storport-Miniport, unterstützt die von SATA (Serial Advanced Technology Attachment) erweiterten Hosts für die Host Controller Schnittstelle (AHCI) in Windows und ersetzt msahci, einen ataport-Miniport.</span><span class="sxs-lookup"><span data-stu-id="4e55a-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4e55a-109">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="4e55a-109">Manifestation</span></span>

<span data-ttu-id="4e55a-110">Es sollte keine Änderung in der Funktionalität oder Leistung vorhanden sein. Dieser Treiber unterstützt alle gleichen Geräte, die von msahci unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4e55a-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="4e55a-111">Diese Änderung ist für den Benutzer transparent.</span><span class="sxs-lookup"><span data-stu-id="4e55a-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4e55a-112">Minderung</span><span class="sxs-lookup"><span data-stu-id="4e55a-112">Mitigation</span></span>

<span data-ttu-id="4e55a-113">Aktualisieren Sie alle Hilfsprogramme und Skripts, die auf ataport-Bindungen beruhen.</span><span class="sxs-lookup"><span data-stu-id="4e55a-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="4e55a-114">Verlassen Sie sich nicht auf den Namen des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="4e55a-114">Do not rely on the drive name.</span></span> <span data-ttu-id="4e55a-115">Verwenden Sie stattdessen die standardmäßige Datenträger Erkennung.</span><span class="sxs-lookup"><span data-stu-id="4e55a-115">Instead use standard disk detection.</span></span>

 

 




