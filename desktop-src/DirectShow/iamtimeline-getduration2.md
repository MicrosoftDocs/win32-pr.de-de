---
description: 'Die GetDuration2-Methode ruft die Dauer der Zeitachse ab. Diese Methode entspricht iamtimeline:: getduration, aber nimmt einen Parameter vom Typ Double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'Iamtimeline:: GetDuration2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359412"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="c0478-104">Iamtimeline:: GetDuration2-Methode</span><span class="sxs-lookup"><span data-stu-id="c0478-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="c0478-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c0478-105">\[Deprecated.</span></span> <span data-ttu-id="c0478-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c0478-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c0478-107">Die- `GetDuration2` Methode ruft die Dauer der Zeitachse ab.</span><span class="sxs-lookup"><span data-stu-id="c0478-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="c0478-108">Diese Methode entspricht [**iamtimeline:: getduration**](iamtimeline-getduration.md), aber nimmt einen Parameter vom Typ **Double**.</span><span class="sxs-lookup"><span data-stu-id="c0478-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0478-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0478-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="c0478-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0478-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0478-111">*pduration*</span><span class="sxs-lookup"><span data-stu-id="c0478-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="c0478-112">Empfängt die Dauer der Zeitachse in Sekundenbruchteilen.</span><span class="sxs-lookup"><span data-stu-id="c0478-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0478-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0478-113">Return value</span></span>

<span data-ttu-id="c0478-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c0478-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0478-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0478-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0478-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0478-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0478-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c0478-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c0478-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c0478-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c0478-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c0478-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0478-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0478-120">Requirements</span></span>



| <span data-ttu-id="c0478-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0478-121">Requirement</span></span> | <span data-ttu-id="c0478-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c0478-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0478-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0478-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c0478-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c0478-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c0478-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0478-125">Library</span></span><br/> | <dl> <span data-ttu-id="c0478-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c0478-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0478-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0478-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0478-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c0478-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c0478-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c0478-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




