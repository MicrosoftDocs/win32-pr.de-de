---
title: Ereignis verschieben
description: Ereignis verschieben
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856208"
---
# <a name="move-event"></a><span data-ttu-id="18a3c-103">Ereignis verschieben</span><span class="sxs-lookup"><span data-stu-id="18a3c-103">Move Event</span></span>

<span data-ttu-id="18a3c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="18a3c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="18a3c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18a3c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="18a3c-106">Tritt ein, wenn ein Zeichen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="18a3c-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="18a3c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="18a3c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="18a3c-108">**Sub-** *Agent*- \_ **Verschiebung (ByVal** - *Kenn zeichenkennung*, **ByVal** *X*, **ByVal** *Y*, **ByVal** - *Ursache \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="18a3c-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="18a3c-109">Teil</span><span class="sxs-lookup"><span data-stu-id="18a3c-109">Part</span></span>          | <span data-ttu-id="18a3c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18a3c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a3c-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="18a3c-111">*CharacterID*</span></span> | <span data-ttu-id="18a3c-112">Gibt die ID des Zeichens zurück, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="18a3c-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="18a3c-113">*X*</span><span class="sxs-lookup"><span data-stu-id="18a3c-113">*X*</span></span>           | <span data-ttu-id="18a3c-114">Gibt die x-Koordinate (in Pixel) des oberen Rands der neuen Position des Zeichen Rahmens als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="18a3c-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="18a3c-115">*J*</span><span class="sxs-lookup"><span data-stu-id="18a3c-115">*Y*</span></span>           | <span data-ttu-id="18a3c-116">Gibt die y-Koordinate (in Pixel) des linken Rands der neuen Position des Zeichen Rahmens als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="18a3c-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="18a3c-117">*Ursache*</span><span class="sxs-lookup"><span data-stu-id="18a3c-117">*Cause*</span></span>       | <span data-ttu-id="18a3c-118">Gibt einen Wert zurück, der angibt, wodurch das Zeichen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="18a3c-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="18a3c-119">1 der Benutzer hat das Zeichen gezogen.</span><span class="sxs-lookup"><span data-stu-id="18a3c-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="18a3c-120">2 Ihre Client Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="18a3c-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="18a3c-121">3 eine andere Client Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="18a3c-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="18a3c-122">4 der Agent-Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="18a3c-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="18a3c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18a3c-123">Remarks</span></span>

<span data-ttu-id="18a3c-124">Dieses Ereignis tritt auf, wenn der Benutzer oder eine Anwendung die Position des Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="18a3c-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="18a3c-125">Die Koordinaten sind in der oberen linken Ecke des Bildschirms relevant.</span><span class="sxs-lookup"><span data-stu-id="18a3c-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="18a3c-126">Dieses Ereignis wird nur an die Clients des Zeichens gesendet (Anwendungen, die das Zeichen geladen haben).</span><span class="sxs-lookup"><span data-stu-id="18a3c-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="18a3c-127">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="18a3c-127">**See Also**</span></span>

<span data-ttu-id="18a3c-128">[**Eigenschaft "muvecause**](movecause-property.md)", [ **Größen Ereignis**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="18a3c-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





