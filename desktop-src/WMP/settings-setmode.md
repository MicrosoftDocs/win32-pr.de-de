---
title: Settings. setmode-Methode
description: Die setmode-Methode legt verschiedene Modi auf aktiv oder inaktiv fest.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setmode-Methode, Windows-Media Player
- setmode-Methode, Windows Media Player, Einstellungs Klasse
- Einstellungs Klasse, Windows Media Player, setmode-Methode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356444"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="4f59a-106">Settings. setmode-Methode</span><span class="sxs-lookup"><span data-stu-id="4f59a-106">Settings.setMode method</span></span>

<span data-ttu-id="4f59a-107">Die **setmode** -Methode legt verschiedene Modi auf aktiv oder inaktiv fest.</span><span class="sxs-lookup"><span data-stu-id="4f59a-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f59a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f59a-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="4f59a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f59a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f59a-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="4f59a-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f59a-111">Eine **Zeichenfolge** , die den Namen des geänderten Modus angibt, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="4f59a-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="4f59a-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4f59a-112">String</span></span>     | <span data-ttu-id="4f59a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f59a-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f59a-114">autorewind</span><span class="sxs-lookup"><span data-stu-id="4f59a-114">autoRewind</span></span> | <span data-ttu-id="4f59a-115">Der Modus, der angibt, ob die Nachverfolgung an den Anfang nach dem Ende wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="4f59a-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="4f59a-116">Der Standardstatus ist "true".</span><span class="sxs-lookup"><span data-stu-id="4f59a-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="4f59a-117">loop</span><span class="sxs-lookup"><span data-stu-id="4f59a-117">loop</span></span>       | <span data-ttu-id="4f59a-118">Der Modus, der angibt, ob sich die Reihenfolge der Spuren wiederholt</span><span class="sxs-lookup"><span data-stu-id="4f59a-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="4f59a-119">Der Standardstatus ist false.</span><span class="sxs-lookup"><span data-stu-id="4f59a-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="4f59a-120">showframe</span><span class="sxs-lookup"><span data-stu-id="4f59a-120">showFrame</span></span>  | <span data-ttu-id="4f59a-121">Modus, der angibt, ob der nächste Video Keyframe an der aktuellen Position angezeigt wird, wenn er nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f59a-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="4f59a-122">Der Standardstatus ist false.</span><span class="sxs-lookup"><span data-stu-id="4f59a-122">Default state is false.</span></span> <span data-ttu-id="4f59a-123">Hat keine Auswirkung auf Audiospuren.</span><span class="sxs-lookup"><span data-stu-id="4f59a-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="4f59a-124">Shuffle</span><span class="sxs-lookup"><span data-stu-id="4f59a-124">shuffle</span></span>    | <span data-ttu-id="4f59a-125">Modus, der angibt, ob die Spuren in zufälliger Reihenfolge wiedergegeben werden</span><span class="sxs-lookup"><span data-stu-id="4f59a-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="4f59a-126">Der Standardstatus ist false.</span><span class="sxs-lookup"><span data-stu-id="4f59a-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="4f59a-127">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f59a-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f59a-128">**Boolescher** Wert, der angibt, ob der neue angegebene Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4f59a-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f59a-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f59a-129">Return value</span></span>

<span data-ttu-id="4f59a-130">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4f59a-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f59a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f59a-131">Remarks</span></span>

<span data-ttu-id="4f59a-132">Wenn der showframe-Modus aktiv ist, muss der Spieler auf den Inhalt des Titels zugreifen, um den Videoframe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4f59a-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="4f59a-133">Aufgrund von Bandbreiten Überlegungen sollten Sie diesen Modus bei der Wiedergabe nicht lokaler Inhalte vorsichtig verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f59a-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f59a-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f59a-134">Requirements</span></span>



| <span data-ttu-id="4f59a-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f59a-135">Requirement</span></span> | <span data-ttu-id="4f59a-136">Wert</span><span class="sxs-lookup"><span data-stu-id="4f59a-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f59a-137">Version</span><span class="sxs-lookup"><span data-stu-id="4f59a-137">Version</span></span><br/> | <span data-ttu-id="4f59a-138">Für Schleifen-und Shuffle-Modi ist Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4f59a-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="4f59a-139">Für den Modus "autorewind" und "showframe", Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4f59a-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="4f59a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4f59a-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f59a-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f59a-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="4f59a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f59a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f59a-143">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="4f59a-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="4f59a-144">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="4f59a-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





