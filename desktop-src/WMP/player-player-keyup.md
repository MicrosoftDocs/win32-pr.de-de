---
title: Player. KeyUp-Ereignis
description: Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird. | Player. KeyUp-Ereignis
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- KeyUp-Ereignisfenster Media Player
- KeyUp-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, KeyUp-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373679"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="46773-107">Player. KeyUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="46773-107">Player.KeyUp event</span></span>

<span data-ttu-id="46773-108">Das **KeyUp** -Ereignis tritt auf, wenn eine Taste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="46773-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="46773-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46773-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="46773-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46773-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46773-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="46773-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="46773-112">**Number** (**int**), der angibt, welcher physische Schlüssel gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="46773-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="46773-113">Mögliche Werte finden Sie unter " [Player. KeyDown](player-player-keydown.md)"-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="46773-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="46773-114">*nshiftstate*</span><span class="sxs-lookup"><span data-stu-id="46773-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="46773-115">**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="46773-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="46773-116">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="46773-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="46773-117">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="46773-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="46773-118">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="46773-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46773-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46773-119">Return value</span></span>

<span data-ttu-id="46773-120">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="46773-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46773-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46773-121">Remarks</span></span>

<span data-ttu-id="46773-122">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="46773-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="46773-123">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="46773-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="46773-124">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46773-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="46773-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46773-125">Requirements</span></span>



| <span data-ttu-id="46773-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46773-126">Requirement</span></span> | <span data-ttu-id="46773-127">Wert</span><span class="sxs-lookup"><span data-stu-id="46773-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46773-128">Version</span><span class="sxs-lookup"><span data-stu-id="46773-128">Version</span></span><br/> | <span data-ttu-id="46773-129">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="46773-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="46773-130">DLL</span><span class="sxs-lookup"><span data-stu-id="46773-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="46773-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46773-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46773-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46773-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46773-133">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="46773-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





