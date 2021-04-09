---
title: DragStart-Ereignis
description: DragStart-Ereignis
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036939"
---
# <a name="dragstart-event"></a><span data-ttu-id="1fa0b-103">DragStart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1fa0b-103">DragStart Event</span></span>

<span data-ttu-id="1fa0b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1fa0b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1fa0b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fa0b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1fa0b-106">Tritt ein, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-106">Occurs when the user begins dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="1fa0b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1fa0b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1fa0b-108">**Sub** *Agent \* \* \* \_ DragStart* \*  **(ByVal-** *Kenn zeichenkennung*, **(ByVal** *-Schaltfläche*, **(** ByVal *Shift*, **(** ByVal *X*, **ByVal** *Y \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="1fa0b-108">**Sub** *agent\*\*\*\_DragStart*\* **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="1fa0b-109">Teil</span><span class="sxs-lookup"><span data-stu-id="1fa0b-109">Part</span></span>          | <span data-ttu-id="1fa0b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fa0b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa0b-111">*Merkmal-ID*</span><span class="sxs-lookup"><span data-stu-id="1fa0b-111">*CharacterID*</span></span> | <span data-ttu-id="1fa0b-112">Gibt die ID des angeklickten Zeichens als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1fa0b-113">*Schaltfläche*</span><span class="sxs-lookup"><span data-stu-id="1fa0b-113">*Button*</span></span>      | <span data-ttu-id="1fa0b-114">Gibt eine ganze Zahl zurück, die die Schaltfläche angibt, die zum Auslösen des Ereignisses gedrückt und freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="1fa0b-115">Das Schaltflächen Argument ist ein Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="1fa0b-116">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1fa0b-117">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1fa0b-118">*Shift*</span><span class="sxs-lookup"><span data-stu-id="1fa0b-118">*Shift*</span></span>       | <span data-ttu-id="1fa0b-119">Gibt eine ganze Zahl zurück, die dem Zustand der UMSCHALTTASTE, der STRG-Taste und der Alt-Taste entspricht, wenn die im Schaltflächen Argument angegebene Schaltfläche gedrückt oder freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="1fa0b-120">Ein Bit ist festgelegt, wenn der Schlüssel nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-120">A bit is set if the key is down.</span></span> <span data-ttu-id="1fa0b-121">Beim Shift-Argument handelt es sich um ein Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="1fa0b-122">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1fa0b-123">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="1fa0b-124">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="1fa0b-125">Wenn z. b. STRG und Alt gedrückt wurden, ist der Wert von Shift 6.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="1fa0b-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="1fa0b-126">*X,Y*</span></span>         | <span data-ttu-id="1fa0b-127">Gibt eine ganze Zahl zurück, die die aktuelle Position des Mauszeigers angibt.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="1fa0b-128">Die X-und Y-Werte werden in Relation zur oberen linken Ecke des Bildschirms immer in Pixel ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="1fa0b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fa0b-129">Remarks</span></span>

<span data-ttu-id="1fa0b-130">Dieses Ereignis wird nur an den Eingabe aktiven Client eines Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="1fa0b-131">Wenn der Benutzer ein Zeichen ohne Eingabe aktiven Client zieht, legt der Server den letzten Eingabe aktiven Client als aktuellen Eingabe aktiven Client fest, sendet das [**activateinput**](activateinput-event.md) -Ereignis an diesen Client und sendet dann das **DragStart** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1fa0b-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **DragStart** event.</span></span>

### <a name="see-also"></a><span data-ttu-id="1fa0b-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1fa0b-132">See Also</span></span>

[<span data-ttu-id="1fa0b-133">**Dragcomplete-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1fa0b-133">**DragComplete event**</span></span>](dragcomplete-event.md)


 

 




