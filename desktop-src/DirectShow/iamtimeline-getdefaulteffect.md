---
description: Die getdefaulteffect-Methode ruft den Standardeffekt ab. Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'Iamtimeline:: getdefaulteffect-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354707"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="01a81-104">Iamtimeline:: getdefaulteffect-Methode</span><span class="sxs-lookup"><span data-stu-id="01a81-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="01a81-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="01a81-105">\[Deprecated.</span></span> <span data-ttu-id="01a81-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="01a81-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01a81-107">Die- `GetDefaultEffect` Methode ruft den Standardeffekt ab.</span><span class="sxs-lookup"><span data-stu-id="01a81-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="01a81-108">Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt</span><span class="sxs-lookup"><span data-stu-id="01a81-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a81-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="01a81-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="01a81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01a81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a81-111">*pguid*</span><span class="sxs-lookup"><span data-stu-id="01a81-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="01a81-112">Empfängt die Globally Unique Identifier (GUID) des Standard Effekts.</span><span class="sxs-lookup"><span data-stu-id="01a81-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a81-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01a81-113">Return value</span></span>

<span data-ttu-id="01a81-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="01a81-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01a81-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01a81-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a81-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01a81-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="01a81-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="01a81-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01a81-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="01a81-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01a81-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="01a81-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01a81-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01a81-120">Requirements</span></span>



| <span data-ttu-id="01a81-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01a81-121">Requirement</span></span> | <span data-ttu-id="01a81-122">Wert</span><span class="sxs-lookup"><span data-stu-id="01a81-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a81-123">Header</span><span class="sxs-lookup"><span data-stu-id="01a81-123">Header</span></span><br/>  | <dl> <span data-ttu-id="01a81-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="01a81-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01a81-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01a81-125">Library</span></span><br/> | <dl> <span data-ttu-id="01a81-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="01a81-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a81-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01a81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a81-128">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="01a81-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="01a81-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="01a81-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




