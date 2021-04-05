---
title: Showdefaultcharakteriproperties-Methode
description: Showdefaultcharakteriproperties-Methode
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709912"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="76e9f-103">Showdefaultcharakteriproperties-Methode</span><span class="sxs-lookup"><span data-stu-id="76e9f-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="76e9f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="76e9f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="76e9f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76e9f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="76e9f-106">Zeigt die Eigenschaften des Standard Zeichens an.</span><span class="sxs-lookup"><span data-stu-id="76e9f-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="76e9f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="76e9f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="76e9f-108">\*Agent \* \* *. Showdefaultcharacters-Eigenschaften* \*  \[ *X* , *Y*\]</span><span class="sxs-lookup"><span data-stu-id="76e9f-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="76e9f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="76e9f-109">Part</span></span> | <span data-ttu-id="76e9f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76e9f-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e9f-111">*X*</span><span class="sxs-lookup"><span data-stu-id="76e9f-111">*X*</span></span>  | <span data-ttu-id="76e9f-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="76e9f-112">Optional.</span></span> <span data-ttu-id="76e9f-113">Ein kurzer ganzzahliger Wert, der die horizontale (*X* ) Bildschirm Koordinate angibt, um das Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76e9f-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="76e9f-114">Diese Koordinate muss in Pixel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76e9f-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="76e9f-115">*J*</span><span class="sxs-lookup"><span data-stu-id="76e9f-115">*Y*</span></span>  | <span data-ttu-id="76e9f-116">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="76e9f-116">Optional.</span></span> <span data-ttu-id="76e9f-117">Ein kurzer *ganzzahliger* Wert, der die vertikale Bildschirm Koordinate (Y) angibt, um das Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76e9f-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="76e9f-118">Diese Koordinate muss in Pixel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76e9f-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76e9f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76e9f-119">Remarks</span></span>

<span data-ttu-id="76e9f-120">Beim Aufrufen dieser Methode wird das standardmäßige Zeichen Eigenschaften Fenster (nicht das Eigenschaften Blatt "Microsoft-Agent") angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76e9f-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="76e9f-121">Wenn Sie die X-und Y-Koordinaten nicht angeben, wird das Fenster an der letzten Position angezeigt, an der es angezeigt wurde.</span><span class="sxs-lookup"><span data-stu-id="76e9f-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="76e9f-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76e9f-122">See Also</span></span>

[<span data-ttu-id="76e9f-123">**Defaultcharacters-Änderungs Ereignis**</span><span class="sxs-lookup"><span data-stu-id="76e9f-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




