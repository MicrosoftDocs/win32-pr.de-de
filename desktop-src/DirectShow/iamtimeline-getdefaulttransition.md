---
description: Die getdefaulttransition-Methode ruft den Standard Übergang ab. Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Iamtimeline:: getdefaulttransition-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367736"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="f2ba2-104">Iamtimeline:: getdefaulttransition-Methode</span><span class="sxs-lookup"><span data-stu-id="f2ba2-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="f2ba2-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-105">\[Deprecated.</span></span> <span data-ttu-id="f2ba2-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f2ba2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f2ba2-107">Die- `GetDefaultTransition` Methode ruft den Standard Übergang ab.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="f2ba2-108">Wenn die Rendering-Engine einen Übergang nicht Renderingmodul renderten kann, ersetzt Sie den Standard Übergang</span><span class="sxs-lookup"><span data-stu-id="f2ba2-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ba2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2ba2-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="f2ba2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2ba2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ba2-111">*pguid*</span><span class="sxs-lookup"><span data-stu-id="f2ba2-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ba2-112">Empfängt die GUID des Standard Übergangs.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ba2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2ba2-113">Return value</span></span>

<span data-ttu-id="f2ba2-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2ba2-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ba2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2ba2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2ba2-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f2ba2-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f2ba2-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2ba2-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2ba2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2ba2-120">Requirements</span></span>



| <span data-ttu-id="f2ba2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2ba2-121">Requirement</span></span> | <span data-ttu-id="f2ba2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f2ba2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ba2-123">Header</span><span class="sxs-lookup"><span data-stu-id="f2ba2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f2ba2-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f2ba2-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f2ba2-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2ba2-125">Library</span></span><br/> | <dl> <span data-ttu-id="f2ba2-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f2ba2-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ba2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2ba2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ba2-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f2ba2-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="f2ba2-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f2ba2-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




