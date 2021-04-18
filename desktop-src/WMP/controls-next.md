---
title: Controls. Next-Methode
description: Die Next-Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- nächste Methode, Windows Media Player
- Next Method Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, nächste Methode
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371790"
---
# <a name="controlsnext-method"></a><span data-ttu-id="ce721-106">Controls. Next-Methode</span><span class="sxs-lookup"><span data-stu-id="ce721-106">Controls.next method</span></span>

<span data-ttu-id="ce721-107">Die **Next** -Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.</span><span class="sxs-lookup"><span data-stu-id="ce721-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce721-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce721-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="ce721-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce721-109">Parameters</span></span>

<span data-ttu-id="ce721-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce721-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce721-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce721-111">Return value</span></span>

<span data-ttu-id="ce721-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce721-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce721-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce721-113">Remarks</span></span>

<span data-ttu-id="ce721-114">Wenn sich die Wiedergabeliste auf dem letzten Eintrag befindet, wenn **Next** aufgerufen wird, wird der erste Eintrag in der Wiedergabeliste zum aktuellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="ce721-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="ce721-115">Bei serverseitigen Wiedergabelisten springt diese Methode zum nächsten Element in der serverseitigen Wiedergabeliste, nicht zur Client Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="ce721-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="ce721-116">Beim Abspielen einer DVD überspringt diese Methode das nächste logische Kapitel in der Wiedergabe Sequenz, das möglicherweise nicht das nächste Kapitel in der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="ce721-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="ce721-117">Bei der Wiedergabe von DVD-Stills springt diese Methode zum nächsten weiter.</span><span class="sxs-lookup"><span data-stu-id="ce721-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="ce721-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce721-118">Examples</span></span>

<span data-ttu-id="ce721-119">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Next** verwendet, um zum nächsten Element in der aktuellen Wiedergabeliste zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="ce721-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="ce721-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce721-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="ce721-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce721-121">Requirements</span></span>



| <span data-ttu-id="ce721-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce721-122">Requirement</span></span> | <span data-ttu-id="ce721-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ce721-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce721-124">Version</span><span class="sxs-lookup"><span data-stu-id="ce721-124">Version</span></span><br/> | <span data-ttu-id="ce721-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ce721-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ce721-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ce721-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce721-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce721-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce721-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce721-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce721-129">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ce721-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="ce721-130">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="ce721-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="ce721-131">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="ce721-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





