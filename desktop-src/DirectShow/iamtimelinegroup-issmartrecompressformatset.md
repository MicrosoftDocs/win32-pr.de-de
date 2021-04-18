---
description: Die issmartrecompressformatset-Methode bestimmt, ob ein intelligentes neukomprimierungs Format für die Gruppe festgelegt wurde.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'Iamtimelinegroup:: issmartrecompressformatset-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357699"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="a4d3a-103">Iamtimelinegroup:: issmartrecompressformatset-Methode</span><span class="sxs-lookup"><span data-stu-id="a4d3a-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="a4d3a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-104">\[Deprecated.</span></span> <span data-ttu-id="a4d3a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a4d3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a4d3a-106">Die- `IsSmartRecompressFormatSet` Methode bestimmt, ob ein intelligentes Recompression-Format für die Gruppe festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d3a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4d3a-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a4d3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4d3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d3a-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a4d3a-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a4d3a-110">Empfängt einen booleschen Wert, der angibt, ob ein Komprimierungs Format festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="a4d3a-111">**True** gibt an, dass ein Komprimierungs Format festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d3a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4d3a-112">Return value</span></span>

<span data-ttu-id="a4d3a-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4d3a-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4d3a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4d3a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4d3a-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4d3a-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a4d3a-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a4d3a-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4d3a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4d3a-119">Requirements</span></span>



| <span data-ttu-id="a4d3a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4d3a-120">Requirement</span></span> | <span data-ttu-id="a4d3a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a4d3a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d3a-122">Header</span><span class="sxs-lookup"><span data-stu-id="a4d3a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a4d3a-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a4d3a-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a4d3a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4d3a-124">Library</span></span><br/> | <dl> <span data-ttu-id="a4d3a-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a4d3a-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4d3a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4d3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d3a-127">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a4d3a-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="a4d3a-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a4d3a-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




