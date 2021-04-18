---
title: Controls. Play-Methode
description: Die Play-Methode bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder die Wiedergabe eines angehaltenen Elements wird wieder aufgenommen.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Wiedergabemethode Windows Media Player
- Play-Methode, Windows Media Player, Controls-Klasse
- Steuerelement-Klasse, Windows Media Player, Wiedergabemethode
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358696"
---
# <a name="controlsplay-method"></a><span data-ttu-id="413d7-106">Controls. Play-Methode</span><span class="sxs-lookup"><span data-stu-id="413d7-106">Controls.play method</span></span>

<span data-ttu-id="413d7-107">Die **Play** -Methode bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder die Wiedergabe eines angehaltenen Elements wird wieder aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="413d7-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="413d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="413d7-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="413d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="413d7-109">Parameters</span></span>

<span data-ttu-id="413d7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="413d7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="413d7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="413d7-111">Return value</span></span>

<span data-ttu-id="413d7-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="413d7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="413d7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="413d7-113">Remarks</span></span>

<span data-ttu-id="413d7-114">Wenn diese Methode während der schnellen Weiterleitung oder rebuggen aufgerufen wird, der Wert von *Settings*. die **Rate** ist auf 1,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="413d7-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="413d7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="413d7-115">Examples</span></span>

<span data-ttu-id="413d7-116">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Play** zum Wiedergeben des aktuellen Medien Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="413d7-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="413d7-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="413d7-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="413d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="413d7-118">Requirements</span></span>



| <span data-ttu-id="413d7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="413d7-119">Requirement</span></span> | <span data-ttu-id="413d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="413d7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="413d7-121">Version</span><span class="sxs-lookup"><span data-stu-id="413d7-121">Version</span></span><br/> | <span data-ttu-id="413d7-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="413d7-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="413d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="413d7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="413d7-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="413d7-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413d7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="413d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413d7-126">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="413d7-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





