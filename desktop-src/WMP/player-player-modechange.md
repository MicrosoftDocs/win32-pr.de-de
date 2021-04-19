---
title: Player. modechange-Ereignis
description: Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird. | Player. modechange-Ereignis
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Modechange-Ereignisfenster Media Player
- Modechange-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, modechange-Ereignis
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366931"
---
# <a name="playermodechange-event"></a><span data-ttu-id="52cbb-107">Player. modechange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="52cbb-107">Player.ModeChange event</span></span>

<span data-ttu-id="52cbb-108">Das **modechange** -Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="52cbb-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="52cbb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52cbb-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="52cbb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52cbb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52cbb-111">*"Name"*</span><span class="sxs-lookup"><span data-stu-id="52cbb-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="52cbb-112">**Zeichenfolge** , die den Modus angibt, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="52cbb-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="52cbb-113">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="52cbb-113">Contains one of the following values.</span></span>



| <span data-ttu-id="52cbb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="52cbb-114">Value</span></span>   | <span data-ttu-id="52cbb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52cbb-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="52cbb-116">Shuffle</span><span class="sxs-lookup"><span data-stu-id="52cbb-116">shuffle</span></span> | <span data-ttu-id="52cbb-117">Spuren werden in zufälliger Reihenfolge wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="52cbb-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="52cbb-118">loop</span><span class="sxs-lookup"><span data-stu-id="52cbb-118">loop</span></span>    | <span data-ttu-id="52cbb-119">Die gesamte Sequenz von Spuren wird wiederholt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="52cbb-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="52cbb-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="52cbb-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="52cbb-121">**Boolescher** Wert, der den neuen Zustand des angegebenen Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="52cbb-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52cbb-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52cbb-122">Return value</span></span>

<span data-ttu-id="52cbb-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="52cbb-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52cbb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52cbb-124">Remarks</span></span>

<span data-ttu-id="52cbb-125">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="52cbb-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="52cbb-126">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="52cbb-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="52cbb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52cbb-127">Requirements</span></span>



| <span data-ttu-id="52cbb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52cbb-128">Requirement</span></span> | <span data-ttu-id="52cbb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="52cbb-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52cbb-130">Version</span><span class="sxs-lookup"><span data-stu-id="52cbb-130">Version</span></span><br/> | <span data-ttu-id="52cbb-131">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="52cbb-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="52cbb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="52cbb-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="52cbb-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52cbb-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52cbb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52cbb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cbb-135">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="52cbb-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="52cbb-136">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="52cbb-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="52cbb-137">**Settings. setmode**</span><span class="sxs-lookup"><span data-stu-id="52cbb-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





