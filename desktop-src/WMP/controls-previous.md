---
title: Controls. Previous-Methode
description: Die vorherige Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- vorherige Methode, Windows Media Player
- vorherige Methode, Windows Media Player, Steuerelement Klasse
- Steuerelement-Klasse, Windows Media Player, vorherige Methode
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372147"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="0d63d-106">Controls. Previous-Methode</span><span class="sxs-lookup"><span data-stu-id="0d63d-106">Controls.previous method</span></span>

<span data-ttu-id="0d63d-107">Die **vorherige** Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.</span><span class="sxs-lookup"><span data-stu-id="0d63d-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d63d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d63d-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="0d63d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d63d-109">Parameters</span></span>

<span data-ttu-id="0d63d-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0d63d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d63d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d63d-111">Return value</span></span>

<span data-ttu-id="0d63d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0d63d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d63d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d63d-113">Remarks</span></span>

<span data-ttu-id="0d63d-114">Wenn sich die Wiedergabeliste auf dem ersten Eintrag befindet, wenn **Previous** aufgerufen wird, wird der letzte Eintrag in der Wiedergabeliste zum aktuellen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="0d63d-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="0d63d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d63d-115">Examples</span></span>

<span data-ttu-id="0d63d-116">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **zurück verwendet, um zum** vorherigen Element in der aktuellen Wiedergabeliste zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="0d63d-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="0d63d-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d63d-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="0d63d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d63d-118">Requirements</span></span>



| <span data-ttu-id="0d63d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d63d-119">Requirement</span></span> | <span data-ttu-id="0d63d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0d63d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d63d-121">Version</span><span class="sxs-lookup"><span data-stu-id="0d63d-121">Version</span></span><br/> | <span data-ttu-id="0d63d-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0d63d-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0d63d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0d63d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d63d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d63d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d63d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d63d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d63d-126">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0d63d-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0d63d-127">**Steuerelemente. Next**</span><span class="sxs-lookup"><span data-stu-id="0d63d-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="0d63d-128">**Controls. Pause**</span><span class="sxs-lookup"><span data-stu-id="0d63d-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





