---
description: Die transitionsenabled-Methode bestimmt, ob Übergänge aktiviert sind.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Iamtimeline:: transitionsenabled-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360923"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="2509a-103">Iamtimeline:: transitionsenabled-Methode</span><span class="sxs-lookup"><span data-stu-id="2509a-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="2509a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2509a-104">\[Deprecated.</span></span> <span data-ttu-id="2509a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2509a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2509a-106">Die **transitionsenabled** -Methode bestimmt, ob Übergänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="2509a-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="2509a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2509a-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="2509a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2509a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2509a-109">*pfaktivierte*</span><span class="sxs-lookup"><span data-stu-id="2509a-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="2509a-110">Empfängt einen booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="2509a-110">Receives a Boolean value.</span></span> <span data-ttu-id="2509a-111">**True** gibt an, dass Übergänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="2509a-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="2509a-112">Andernfalls sind Übergänge deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2509a-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2509a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2509a-113">Return value</span></span>

<span data-ttu-id="2509a-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2509a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2509a-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2509a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2509a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2509a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2509a-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2509a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2509a-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="2509a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2509a-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2509a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2509a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2509a-120">Requirements</span></span>



| <span data-ttu-id="2509a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2509a-121">Requirement</span></span> | <span data-ttu-id="2509a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2509a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2509a-123">Header</span><span class="sxs-lookup"><span data-stu-id="2509a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2509a-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2509a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2509a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2509a-125">Library</span></span><br/> | <dl> <span data-ttu-id="2509a-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="2509a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2509a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2509a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2509a-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2509a-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="2509a-129">**Iamtimeline:: enabletransitions**</span><span class="sxs-lookup"><span data-stu-id="2509a-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="2509a-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="2509a-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




