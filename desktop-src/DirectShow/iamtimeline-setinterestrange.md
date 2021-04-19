---
description: Nicht implementiert.
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'Iamtimeline:: setinterestrange-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a3c92848380bb71bcdca0e6f6de1069d6eb998a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369705"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="ab678-103">Iamtimeline:: setinterestrange-Methode</span><span class="sxs-lookup"><span data-stu-id="ab678-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="ab678-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ab678-104">\[Deprecated.</span></span> <span data-ttu-id="ab678-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ab678-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ab678-106">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ab678-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab678-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab678-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="ab678-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab678-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab678-109">*Starten*</span><span class="sxs-lookup"><span data-stu-id="ab678-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="ab678-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ab678-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ab678-111">*Beenden*</span><span class="sxs-lookup"><span data-stu-id="ab678-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="ab678-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="ab678-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab678-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab678-113">Return value</span></span>

<span data-ttu-id="ab678-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ab678-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab678-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab678-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab678-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab678-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ab678-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ab678-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ab678-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ab678-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ab678-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab678-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab678-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab678-120">Requirements</span></span>



| <span data-ttu-id="ab678-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab678-121">Requirement</span></span> | <span data-ttu-id="ab678-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ab678-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab678-123">Header</span><span class="sxs-lookup"><span data-stu-id="ab678-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ab678-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ab678-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab678-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab678-125">Library</span></span><br/> | <dl> <span data-ttu-id="ab678-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ab678-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab678-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab678-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab678-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ab678-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




