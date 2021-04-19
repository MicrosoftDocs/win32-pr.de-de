---
title: Player. positionChange-Ereignis
description: Das Positions Change-Ereignis tritt auf, wenn die aktuelle Position des Medien Elements geändert wurde.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Positions Change-Ereignisfenster Media Player
- Positions Change-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, positionChange-Ereignis
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360422"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="1103c-106">Player. positionChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1103c-106">Player.PositionChange event</span></span>

<span data-ttu-id="1103c-107">Das **Positions Change** -Ereignis tritt auf, wenn die aktuelle Position des Medien Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1103c-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1103c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1103c-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="1103c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1103c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1103c-110">*oldposition*</span><span class="sxs-lookup"><span data-stu-id="1103c-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="1103c-111">Number (**Double**), das die alte Position angibt.</span><span class="sxs-lookup"><span data-stu-id="1103c-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="1103c-112">*neuposition*</span><span class="sxs-lookup"><span data-stu-id="1103c-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="1103c-113">**Number** (**Double**), das die neue Position angibt.</span><span class="sxs-lookup"><span data-stu-id="1103c-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1103c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1103c-114">Return value</span></span>

<span data-ttu-id="1103c-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1103c-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1103c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1103c-116">Remarks</span></span>

<span data-ttu-id="1103c-117">Dieses Ereignis wird während der Wiedergabe nicht routinemäßig ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1103c-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="1103c-118">Sie tritt nur dann auf, wenn die aktuelle Position des Wiedergabe-Medien Elements aktiv geändert wird, z. b. wenn der Benutzer das Such handle oder den Code verschiebt, der einen Wert für Steuer *Elemente* angibt. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="1103c-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="1103c-119">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="1103c-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1103c-120">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="1103c-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1103c-121">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1103c-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1103c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1103c-122">Requirements</span></span>



| <span data-ttu-id="1103c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1103c-123">Requirement</span></span> | <span data-ttu-id="1103c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1103c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1103c-125">Version</span><span class="sxs-lookup"><span data-stu-id="1103c-125">Version</span></span><br/> | <span data-ttu-id="1103c-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1103c-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1103c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1103c-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="1103c-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1103c-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1103c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1103c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1103c-130">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1103c-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





