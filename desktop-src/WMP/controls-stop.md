---
title: Controls. stoppt-Methode
description: Die Methode "beenden" beendet die Wiedergabe des Medien Elements. | Controls. stoppt-Methode
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- Windows-Media Player "Methode"
- Methode "Methode Media Player", Steuerelement Klasse
- Steuerelement-Klasse, Windows Media Player, Methode "Ende"
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369667"
---
# <a name="controlsstop-method"></a><span data-ttu-id="c179d-107">Controls. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="c179d-107">Controls.stop method</span></span>

<span data-ttu-id="c179d-108">Die Methode " **Beenden** " beendet die Wiedergabe des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="c179d-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c179d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c179d-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="c179d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c179d-110">Parameters</span></span>

<span data-ttu-id="c179d-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c179d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c179d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c179d-112">Return value</span></span>

<span data-ttu-id="c179d-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c179d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c179d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c179d-114">Remarks</span></span>

<span data-ttu-id="c179d-115">Diese Methode bewirkt, dass Windows Media Player alle verwendeten Systemressourcen, z. b. das Audiogerät, freigibt.</span><span class="sxs-lookup"><span data-stu-id="c179d-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="c179d-116">Das aktuelle Medien Element wird jedoch nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c179d-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="c179d-117">Wenn der Spieler angehalten wird, wird die Nachverfolgung an den Anfang zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c179d-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="c179d-118">Der Aufruf von **Play** beginnt dann, den Clip von Anfang an wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c179d-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="c179d-119">Verwenden Sie die **Pause** -Methode, um einen Wiedergabe Vorgang anzuhalten, ohne die aktuelle Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c179d-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="c179d-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c179d-120">Examples</span></span>

<span data-ttu-id="c179d-121">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Beenden** zum Beenden der Wiedergabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c179d-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="c179d-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c179d-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="c179d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c179d-123">Requirements</span></span>



| <span data-ttu-id="c179d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c179d-124">Requirement</span></span> | <span data-ttu-id="c179d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c179d-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c179d-126">Version</span><span class="sxs-lookup"><span data-stu-id="c179d-126">Version</span></span><br/> | <span data-ttu-id="c179d-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c179d-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c179d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c179d-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c179d-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c179d-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c179d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c179d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c179d-131">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c179d-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c179d-132">**Steuerelemente. Next**</span><span class="sxs-lookup"><span data-stu-id="c179d-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="c179d-133">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="c179d-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="c179d-134">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="c179d-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





