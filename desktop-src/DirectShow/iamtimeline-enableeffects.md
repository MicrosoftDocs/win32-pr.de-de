---
description: Die enableeffects-Methode aktiviert oder deaktiviert alle Effekte in der Zeitachse. Wenn Effekte deaktiviert sind, verbleiben Sie in der Zeitachse, werden jedoch nicht gerendert.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'Iamtimeline:: enableeffects-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358025"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="cea09-104">Iamtimeline:: enableeffects-Methode</span><span class="sxs-lookup"><span data-stu-id="cea09-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="cea09-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cea09-105">\[Deprecated.</span></span> <span data-ttu-id="cea09-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cea09-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cea09-107">Die- `EnableEffects` Methode aktiviert oder deaktiviert alle Effekte in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="cea09-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="cea09-108">Wenn Effekte deaktiviert sind, verbleiben Sie in der Zeitachse, werden jedoch nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="cea09-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea09-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cea09-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cea09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea09-111">*fenabled*</span><span class="sxs-lookup"><span data-stu-id="cea09-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="cea09-112">Boolescher Wert, der angibt, ob Effekte aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cea09-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="cea09-113">**True** gibt an, dass Effekte aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="cea09-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="cea09-114">**False** gibt an, dass Effekte deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="cea09-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea09-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cea09-115">Return value</span></span>

<span data-ttu-id="cea09-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cea09-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cea09-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cea09-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea09-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cea09-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cea09-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cea09-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cea09-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="cea09-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cea09-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cea09-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cea09-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea09-122">Requirements</span></span>



| <span data-ttu-id="cea09-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cea09-123">Requirement</span></span> | <span data-ttu-id="cea09-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cea09-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea09-125">Header</span><span class="sxs-lookup"><span data-stu-id="cea09-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cea09-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cea09-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cea09-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cea09-127">Library</span></span><br/> | <dl> <span data-ttu-id="cea09-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="cea09-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea09-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cea09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea09-130">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cea09-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="cea09-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="cea09-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




