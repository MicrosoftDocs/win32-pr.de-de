---
description: 'IAMTimelineObj::GetTimelineNoRef-Methode: Nicht unterstützt.'
ms.assetid: be7721e4-ba43-47c1-b955-e97afc5caac4
title: IAMTimelineObj::GetTimelineNoRef-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineNoRef
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f36918f7e2bc52fb8cb2898930ff1971ad33b74b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098531"
---
# <a name="iamtimelineobjgettimelinenoref-method"></a><span data-ttu-id="482ef-103">IAMTimelineObj::GetTimelineNoRef-Methode</span><span class="sxs-lookup"><span data-stu-id="482ef-103">IAMTimelineObj::GetTimelineNoRef method</span></span>

> [!Note]  
> <span data-ttu-id="482ef-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="482ef-104">\[Deprecated.</span></span> <span data-ttu-id="482ef-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="482ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="482ef-106">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="482ef-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="482ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="482ef-107">Syntax</span></span>


```C++
HRESULT GetTimelineNoRef(
   IAMTimeline **ppResult
);
```



## <a name="parameters"></a><span data-ttu-id="482ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="482ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482ef-109">*ppResult*</span><span class="sxs-lookup"><span data-stu-id="482ef-109">*ppResult*</span></span> 
</dt> <dd>

<span data-ttu-id="482ef-110">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="482ef-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="482ef-111">Return value</span></span>

<span data-ttu-id="482ef-112">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="482ef-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="482ef-113">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="482ef-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="482ef-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="482ef-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="482ef-115">Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="482ef-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="482ef-116">Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und .NET Framework [3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="482ef-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="482ef-117">Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="482ef-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="482ef-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="482ef-118">Requirements</span></span>



| <span data-ttu-id="482ef-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="482ef-119">Requirement</span></span> | <span data-ttu-id="482ef-120">Wert</span><span class="sxs-lookup"><span data-stu-id="482ef-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="482ef-121">Header</span><span class="sxs-lookup"><span data-stu-id="482ef-121">Header</span></span><br/>  | <dl> <span data-ttu-id="482ef-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="482ef-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="482ef-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="482ef-123">Library</span></span><br/> | <dl> <span data-ttu-id="482ef-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="482ef-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="482ef-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="482ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482ef-126">**IAMTimelineObj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="482ef-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




