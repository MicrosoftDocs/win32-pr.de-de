---
title: Settings. getMode-Methode
description: Die getMode-Methode bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- getMode-Methode, Windows-Media Player
- getMode-Methode, Windows Media Player, Einstellungs Klasse
- Settings-Klasse, Windows Media Player, getMode-Methode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352957"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="2b1ab-106">Settings. getMode-Methode</span><span class="sxs-lookup"><span data-stu-id="2b1ab-106">Settings.getMode method</span></span>

<span data-ttu-id="2b1ab-107">Die **getMode** -Methode bestimmt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b1ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b1ab-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="2b1ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b1ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b1ab-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="2b1ab-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b1ab-111">Eine **Zeichenfolge** , die den Namen des fraglichen Modus angibt, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="2b1ab-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b1ab-112">String</span></span>     | <span data-ttu-id="2b1ab-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b1ab-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1ab-114">autorewind</span><span class="sxs-lookup"><span data-stu-id="2b1ab-114">autoRewind</span></span> | <span data-ttu-id="2b1ab-115">Nach der Wiedergabe am Ende werden nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="2b1ab-116">loop</span><span class="sxs-lookup"><span data-stu-id="2b1ab-116">loop</span></span>       | <span data-ttu-id="2b1ab-117">Die Reihenfolge der Spuren wird wiederholt.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="2b1ab-118">showframe</span><span class="sxs-lookup"><span data-stu-id="2b1ab-118">showFrame</span></span>  | <span data-ttu-id="2b1ab-119">Der nächste Keyframe wird an der aktuellen Position angezeigt, wenn er nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="2b1ab-120">Dieser Modus ist für Audiospuren nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="2b1ab-121">Shuffle</span><span class="sxs-lookup"><span data-stu-id="2b1ab-121">shuffle</span></span>    | <span data-ttu-id="2b1ab-122">Spuren werden in zufälliger Reihenfolge wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b1ab-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b1ab-123">Return value</span></span>

<span data-ttu-id="2b1ab-124">Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob der angegebene Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b1ab-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b1ab-125">Requirements</span></span>



| <span data-ttu-id="2b1ab-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b1ab-126">Requirement</span></span> | <span data-ttu-id="2b1ab-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2b1ab-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1ab-128">Version</span><span class="sxs-lookup"><span data-stu-id="2b1ab-128">Version</span></span><br/> | <span data-ttu-id="2b1ab-129">Für Schleifen-und Shuffle-Modi ist Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="2b1ab-130">Für den Modus "autorewind" und "showframe", Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="2b1ab-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b1ab-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b1ab-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b1ab-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="2b1ab-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b1ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b1ab-134">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="2b1ab-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="2b1ab-135">**Settings. setmode**</span><span class="sxs-lookup"><span data-stu-id="2b1ab-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





