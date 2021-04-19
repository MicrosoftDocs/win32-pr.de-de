---
title: Controls. Step-Methode
description: Die Step-Methode bewirkt, dass das aktuelle Video Medien Element die Wiedergabe für den nächsten Frame oder den vorherigen Frame fixiert.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Step-Methode (Windows Media Player)
- Step-Methode, Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, Step-Methode
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366044"
---
# <a name="controlsstep-method"></a><span data-ttu-id="83903-106">Controls. Step-Methode</span><span class="sxs-lookup"><span data-stu-id="83903-106">Controls.step method</span></span>

<span data-ttu-id="83903-107">Die **Step** -Methode bewirkt, dass das aktuelle Video Medien Element die Wiedergabe für den nächsten Frame oder den vorherigen Frame fixiert.</span><span class="sxs-lookup"><span data-stu-id="83903-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="83903-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="83903-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="83903-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="83903-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83903-110">*FrameCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83903-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83903-111">**Zahl** (**Long**), die angibt, wie viele Frames vor dem Einfrieren durchlaufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83903-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="83903-112">Muss derzeit auf 1 oder-1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="83903-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83903-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83903-113">Return value</span></span>

<span data-ttu-id="83903-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="83903-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83903-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83903-115">Remarks</span></span>

<span data-ttu-id="83903-116">Diese Methode unterstützt derzeit nur die Parameter 1 oder-1, sodass Sie nur einen Frame gleichzeitig ausführen können.</span><span class="sxs-lookup"><span data-stu-id="83903-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="83903-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83903-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="83903-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83903-118">Requirements</span></span>



| <span data-ttu-id="83903-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83903-119">Requirement</span></span> | <span data-ttu-id="83903-120">Wert</span><span class="sxs-lookup"><span data-stu-id="83903-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83903-121">Version</span><span class="sxs-lookup"><span data-stu-id="83903-121">Version</span></span><br/> | <span data-ttu-id="83903-122">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="83903-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="83903-123">DLL</span><span class="sxs-lookup"><span data-stu-id="83903-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="83903-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83903-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83903-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83903-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83903-126">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="83903-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="83903-127">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="83903-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





