---
description: Die setdefaulttransition-Methode legt den Standard Übergang fest. Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'Iamtimeline:: setdefaulttransition-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362124"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="afe49-104">Iamtimeline:: setdefaulttransition-Methode</span><span class="sxs-lookup"><span data-stu-id="afe49-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="afe49-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="afe49-105">\[Deprecated.</span></span> <span data-ttu-id="afe49-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="afe49-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="afe49-107">Die- `SetDefaultTransition` Methode legt den Standard Übergang fest.</span><span class="sxs-lookup"><span data-stu-id="afe49-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="afe49-108">Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang</span><span class="sxs-lookup"><span data-stu-id="afe49-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe49-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="afe49-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="afe49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afe49-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe49-111">*pguid*</span><span class="sxs-lookup"><span data-stu-id="afe49-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="afe49-112">Ein Zeiger auf eine Variable, die die GUID des Standard Übergangs enthält.</span><span class="sxs-lookup"><span data-stu-id="afe49-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe49-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afe49-113">Return value</span></span>

<span data-ttu-id="afe49-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="afe49-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="afe49-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="afe49-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="afe49-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afe49-116">Remarks</span></span>

<span data-ttu-id="afe49-117">Wenn Sie keinen Standard Übergang festlegen oder wenn der von Ihnen als Standard angegebene Übergang einen Fehler verursacht, verwendet des einen eigenen Standard Übergang.</span><span class="sxs-lookup"><span data-stu-id="afe49-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="afe49-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="afe49-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="afe49-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="afe49-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="afe49-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="afe49-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="afe49-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afe49-121">Requirements</span></span>



| <span data-ttu-id="afe49-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afe49-122">Requirement</span></span> | <span data-ttu-id="afe49-123">Wert</span><span class="sxs-lookup"><span data-stu-id="afe49-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afe49-124">Header</span><span class="sxs-lookup"><span data-stu-id="afe49-124">Header</span></span><br/>  | <dl> <span data-ttu-id="afe49-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="afe49-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="afe49-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afe49-126">Library</span></span><br/> | <dl> <span data-ttu-id="afe49-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="afe49-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe49-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afe49-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe49-129">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="afe49-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="afe49-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="afe49-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




