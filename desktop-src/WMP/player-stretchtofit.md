---
title: Player. stretchdefit
description: Mit der Eigenschaft stretchdefit wird ein Wert angegeben oder abgerufen, der angibt, ob das Video, das von der Windows-Media Player Steuerung angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds ist.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchdefit-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368291"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="1a976-104">Player. stretchdefit</span><span class="sxs-lookup"><span data-stu-id="1a976-104">Player.stretchToFit</span></span>

<span data-ttu-id="1a976-105">Mit der Eigenschaft **stretchdefit** wird ein Wert angegeben oder abgerufen, der angibt, ob das Video, das von der Windows-Media Player Steuerung angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds ist.</span><span class="sxs-lookup"><span data-stu-id="1a976-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a976-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a976-106">Syntax</span></span>

<span data-ttu-id="1a976-107">*Player*. **stretchdefit**</span><span class="sxs-lookup"><span data-stu-id="1a976-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1a976-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1a976-108">Possible Values</span></span>

<span data-ttu-id="1a976-109">Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1a976-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1a976-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1a976-110">Value</span></span> | <span data-ttu-id="1a976-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a976-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="1a976-112">true</span><span class="sxs-lookup"><span data-stu-id="1a976-112">true</span></span>  | <span data-ttu-id="1a976-113">Das Video wird so gestreckt, dass es an das Fenster angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="1a976-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="1a976-114">false</span><span class="sxs-lookup"><span data-stu-id="1a976-114">false</span></span> | <span data-ttu-id="1a976-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="1a976-115">Default.</span></span> <span data-ttu-id="1a976-116">Das Video wird nicht so gestreckt, dass es an das Fenster angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="1a976-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a976-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a976-117">Remarks</span></span>

<span data-ttu-id="1a976-118">Wenn **stretchdefit** auf true festgelegt ist, wird das ursprüngliche Seitenverhältnis des Videos vom Windows Media Player-Steuerelement beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1a976-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="1a976-119">Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters identisch ist, können schwarze Masken Bereiche entweder am oberen und unteren Rand des Video Bilds angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1a976-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="1a976-120">Diese Eigenschaft gilt nur für das Windows Media Player-Steuerelement, wenn Sie in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="1a976-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="1a976-121">**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a976-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a976-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a976-122">Requirements</span></span>



| <span data-ttu-id="1a976-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a976-123">Requirement</span></span> | <span data-ttu-id="1a976-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1a976-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a976-125">Version</span><span class="sxs-lookup"><span data-stu-id="1a976-125">Version</span></span><br/> | <span data-ttu-id="1a976-126">Windows Media Player Version 7,1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1a976-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="1a976-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1a976-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a976-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a976-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a976-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a976-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a976-130">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1a976-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





