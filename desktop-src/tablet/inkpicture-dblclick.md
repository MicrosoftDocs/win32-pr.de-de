---
description: Tritt auf, wenn auf das InkPicture-Steuerelement Doppel geklickt wird.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture. DblClick-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347888"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="dac19-103">InkPicture. DblClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="dac19-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="dac19-104">Tritt auf, wenn auf das [InkPicture](inkpicture-control-reference.md) -Steuerelement Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="dac19-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dac19-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="dac19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dac19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac19-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dac19-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dac19-108">Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dac19-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac19-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dac19-109">Return value</span></span>

<span data-ttu-id="dac19-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dac19-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac19-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dac19-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dac19-112">Verwenden Sie das [**MouseDown**](inkpicture-mousedown.md) -und das [**MouseUp**](inkpicture-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="dac19-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="dac19-113">Wenn im [**Click**](inkpicture-click.md) -Ereignis Code vorhanden ist, wird das **DblClick** -Ereignis nie auslöst.</span><span class="sxs-lookup"><span data-stu-id="dac19-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="dac19-114">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="dac19-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="dac19-115">Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ipedblclick**.</span><span class="sxs-lookup"><span data-stu-id="dac19-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac19-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dac19-116">Requirements</span></span>



| <span data-ttu-id="dac19-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dac19-117">Requirement</span></span> | <span data-ttu-id="dac19-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dac19-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac19-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dac19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dac19-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dac19-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dac19-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dac19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dac19-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dac19-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dac19-123">Header</span><span class="sxs-lookup"><span data-stu-id="dac19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac19-124"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dac19-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dac19-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dac19-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="dac19-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac19-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dac19-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dac19-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac19-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="dac19-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




