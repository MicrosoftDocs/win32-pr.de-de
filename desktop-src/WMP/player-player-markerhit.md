---
title: Player. markerhit-Ereignis
description: Das markerhit-Ereignis tritt auf, wenn ein Marker erreicht wird. | Player. markerhit-Ereignis
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player "markerhit-Ereignisfenster"
- Markerhit-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, markerhit-Ereignis
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372307"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="58db5-107">Player. markerhit-Ereignis</span><span class="sxs-lookup"><span data-stu-id="58db5-107">Player.MarkerHit event</span></span>

<span data-ttu-id="58db5-108">Das **markerhit** -Ereignis tritt auf, wenn ein Marker erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="58db5-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="58db5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58db5-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="58db5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="58db5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58db5-111">*Markernum*</span><span class="sxs-lookup"><span data-stu-id="58db5-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="58db5-112">**Zahl** (**Long**), die die Nummer der Markierung angibt, die getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="58db5-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58db5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58db5-113">Return value</span></span>

<span data-ttu-id="58db5-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="58db5-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58db5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58db5-115">Remarks</span></span>

<span data-ttu-id="58db5-116">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="58db5-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="58db5-117">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="58db5-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="58db5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58db5-118">Requirements</span></span>



| <span data-ttu-id="58db5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58db5-119">Requirement</span></span> | <span data-ttu-id="58db5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="58db5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58db5-121">Version</span><span class="sxs-lookup"><span data-stu-id="58db5-121">Version</span></span><br/> | <span data-ttu-id="58db5-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="58db5-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="58db5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58db5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="58db5-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58db5-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58db5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58db5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58db5-126">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="58db5-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





