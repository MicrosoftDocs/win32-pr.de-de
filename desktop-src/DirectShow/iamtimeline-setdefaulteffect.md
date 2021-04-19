---
description: Die setdefaulteffect-Methode legt den Standardeffekt fest. Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'Iamtimeline:: setdefaulteffect-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366013"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="152f2-104">Iamtimeline:: setdefaulteffect-Methode</span><span class="sxs-lookup"><span data-stu-id="152f2-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="152f2-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="152f2-105">\[Deprecated.</span></span> <span data-ttu-id="152f2-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="152f2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="152f2-107">Die- `SetDefaultEffect` Methode legt den Standardeffekt fest.</span><span class="sxs-lookup"><span data-stu-id="152f2-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="152f2-108">Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt</span><span class="sxs-lookup"><span data-stu-id="152f2-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="152f2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="152f2-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="152f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="152f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152f2-111">*pguid*</span><span class="sxs-lookup"><span data-stu-id="152f2-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="152f2-112">Ein Zeiger auf die GUID des Standard Effekts.</span><span class="sxs-lookup"><span data-stu-id="152f2-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="152f2-113">Return value</span></span>

<span data-ttu-id="152f2-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="152f2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="152f2-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="152f2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="152f2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="152f2-116">Remarks</span></span>

<span data-ttu-id="152f2-117">Wenn Sie keinen Standardeffekt festlegen oder wenn der als Standard angegebene Effekt einen Fehler verursacht, verwendet des einen eigenen Standardeffekt.</span><span class="sxs-lookup"><span data-stu-id="152f2-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="152f2-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="152f2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="152f2-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="152f2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="152f2-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="152f2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="152f2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="152f2-121">Requirements</span></span>



| <span data-ttu-id="152f2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="152f2-122">Requirement</span></span> | <span data-ttu-id="152f2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="152f2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="152f2-124">Header</span><span class="sxs-lookup"><span data-stu-id="152f2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="152f2-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="152f2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="152f2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="152f2-126">Library</span></span><br/> | <dl> <span data-ttu-id="152f2-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="152f2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152f2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="152f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152f2-129">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="152f2-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="152f2-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="152f2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




