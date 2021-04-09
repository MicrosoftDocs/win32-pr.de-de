---
description: Das showmenu-Ereignis wird gesendet, wenn der Disc die Anzeige eines Menüs aktiviert oder deaktiviert.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: Showmenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957961"
---
# <a name="showmenu"></a><span data-ttu-id="eafaf-103">Showmenu</span><span class="sxs-lookup"><span data-stu-id="eafaf-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="eafaf-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eafaf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eafaf-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="eafaf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eafaf-106">Das `ShowMenu` Ereignis wird gesendet, wenn der Disc die Anzeige eines Menüs aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eafaf-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="eafaf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eafaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafaf-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*Dvdmenuidconstants*</span><span class="sxs-lookup"><span data-stu-id="eafaf-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="eafaf-109">Gibt an, welches Menü als Zahlenwert aktiviert oder deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="eafaf-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="eafaf-110">Wert</span><span class="sxs-lookup"><span data-stu-id="eafaf-110">Value</span></span> | <span data-ttu-id="eafaf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eafaf-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="eafaf-112">2</span><span class="sxs-lookup"><span data-stu-id="eafaf-112">2</span></span>     | <span data-ttu-id="eafaf-113">Titel</span><span class="sxs-lookup"><span data-stu-id="eafaf-113">Title</span></span>       |
| <span data-ttu-id="eafaf-114">3</span><span class="sxs-lookup"><span data-stu-id="eafaf-114">3</span></span>     | <span data-ttu-id="eafaf-115">Root</span><span class="sxs-lookup"><span data-stu-id="eafaf-115">Root</span></span>        |
| <span data-ttu-id="eafaf-116">4</span><span class="sxs-lookup"><span data-stu-id="eafaf-116">4</span></span>     | <span data-ttu-id="eafaf-117">Untertitel</span><span class="sxs-lookup"><span data-stu-id="eafaf-117">Subpicture</span></span>  |
| <span data-ttu-id="eafaf-118">5</span><span class="sxs-lookup"><span data-stu-id="eafaf-118">5</span></span>     | <span data-ttu-id="eafaf-119">Audio</span><span class="sxs-lookup"><span data-stu-id="eafaf-119">Audio</span></span>       |
| <span data-ttu-id="eafaf-120">6</span><span class="sxs-lookup"><span data-stu-id="eafaf-120">6</span></span>     | <span data-ttu-id="eafaf-121">Angle</span><span class="sxs-lookup"><span data-stu-id="eafaf-121">Angle</span></span>       |
| <span data-ttu-id="eafaf-122">7</span><span class="sxs-lookup"><span data-stu-id="eafaf-122">7</span></span>     | <span data-ttu-id="eafaf-123">Kapitel</span><span class="sxs-lookup"><span data-stu-id="eafaf-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="eafaf-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*</span><span class="sxs-lookup"><span data-stu-id="eafaf-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="eafaf-125">Gibt an, ob der Vorgang als boolescher Wert aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eafaf-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



