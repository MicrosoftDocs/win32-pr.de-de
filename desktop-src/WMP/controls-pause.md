---
title: Controls. Pause-Methode
description: Die Pause-Methode hält die Wiedergabe des Medien Elements an. | Controls. Pause-Methode
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- Windows-Media Player für die Methoden Pause
- Pause-Methode, Windows Media Player, Steuerelement Klasse
- Steuerelement-Klasse, Windows-Media Player, anhaltemethode
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371471"
---
# <a name="controlspause-method"></a><span data-ttu-id="20761-107">Controls. Pause-Methode</span><span class="sxs-lookup"><span data-stu-id="20761-107">Controls.pause method</span></span>

<span data-ttu-id="20761-108">Die **Pause** -Methode hält die Wiedergabe des Medien Elements an.</span><span class="sxs-lookup"><span data-stu-id="20761-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="20761-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20761-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="20761-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20761-110">Parameters</span></span>

<span data-ttu-id="20761-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="20761-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20761-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20761-112">Return value</span></span>

<span data-ttu-id="20761-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20761-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20761-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20761-114">Remarks</span></span>

<span data-ttu-id="20761-115">Wenn eine Datei angehalten wird, gibt Windows Media Player keine Systemressourcen, z. b. das Audiogerät, aus.</span><span class="sxs-lookup"><span data-stu-id="20761-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="20761-116">Bestimmte Medientypen können nicht angehalten werden, z. b. Livestreams.</span><span class="sxs-lookup"><span data-stu-id="20761-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="20761-117">Verwenden Sie-Steuer *Elemente*, um zu bestimmen, ob ein bestimmter Medientyp angehalten werden kann. **IsAvailable (' Pause ')**.</span><span class="sxs-lookup"><span data-stu-id="20761-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="20761-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20761-118">Examples</span></span>

<span data-ttu-id="20761-119">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Pause** zum Anhalten der Wiedergabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="20761-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="20761-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="20761-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="20761-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20761-121">Requirements</span></span>



| <span data-ttu-id="20761-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20761-122">Requirement</span></span> | <span data-ttu-id="20761-123">Wert</span><span class="sxs-lookup"><span data-stu-id="20761-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20761-124">Version</span><span class="sxs-lookup"><span data-stu-id="20761-124">Version</span></span><br/> | <span data-ttu-id="20761-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="20761-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="20761-126">DLL</span><span class="sxs-lookup"><span data-stu-id="20761-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="20761-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20761-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20761-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20761-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20761-129">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="20761-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="20761-130">**Controls. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="20761-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





