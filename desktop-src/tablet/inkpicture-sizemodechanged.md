---
description: Tritt auf, nachdem die SizeMode-Eigenschaft des InkPicture-Steuer Elements geändert wurde.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture. SizeModeChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348658"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="112cf-103">InkPicture. SizeModeChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="112cf-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="112cf-104">Tritt auf, nachdem die [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="112cf-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="112cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="112cf-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="112cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="112cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112cf-107">*NEWMODE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112cf-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112cf-108">Der neue Zustand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements, basierend auf dem neuen Wert der [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="112cf-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="112cf-109">*Oldmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="112cf-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112cf-110">Der alte Zustand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements, basierend auf dem alten Wert der [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="112cf-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="112cf-111">Return value</span></span>

<span data-ttu-id="112cf-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="112cf-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="112cf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="112cf-113">Remarks</span></span>

<span data-ttu-id="112cf-114">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="112cf-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="112cf-115">Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ iPeer SizeModeChanged".</span><span class="sxs-lookup"><span data-stu-id="112cf-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="112cf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="112cf-116">Requirements</span></span>



| <span data-ttu-id="112cf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="112cf-117">Requirement</span></span> | <span data-ttu-id="112cf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="112cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="112cf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="112cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="112cf-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="112cf-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="112cf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="112cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="112cf-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="112cf-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="112cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="112cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="112cf-124"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="112cf-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="112cf-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="112cf-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="112cf-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="112cf-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="112cf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="112cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112cf-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="112cf-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

