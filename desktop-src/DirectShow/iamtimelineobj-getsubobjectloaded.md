---
description: Die getsubobjectloaded-Methode bestimmt, ob der untergeordnete Zeiger festgelegt wurde.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'Iamtimelineobj:: getsubobjectloaded-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359297"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="22870-103">Iamtimelineobj:: getsubobjectloaded-Methode</span><span class="sxs-lookup"><span data-stu-id="22870-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="22870-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22870-104">\[Deprecated.</span></span> <span data-ttu-id="22870-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="22870-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22870-106">Die- `GetSubObjectLoaded` Methode bestimmt, ob der untergeordnete Zeiger festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="22870-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="22870-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22870-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="22870-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22870-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22870-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="22870-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="22870-110">Empfängt einen booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="22870-110">Receives a Boolean value.</span></span> <span data-ttu-id="22870-111">Wenn der Wert **true** ist, wurde der untergeordnete Zeiger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22870-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="22870-112">**False** gibt an, dass der Zeiger nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="22870-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22870-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22870-113">Return value</span></span>

<span data-ttu-id="22870-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="22870-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22870-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22870-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22870-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22870-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22870-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="22870-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22870-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="22870-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22870-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22870-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22870-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22870-120">Requirements</span></span>



| <span data-ttu-id="22870-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22870-121">Requirement</span></span> | <span data-ttu-id="22870-122">Wert</span><span class="sxs-lookup"><span data-stu-id="22870-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22870-123">Header</span><span class="sxs-lookup"><span data-stu-id="22870-123">Header</span></span><br/>  | <dl> <span data-ttu-id="22870-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="22870-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22870-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22870-125">Library</span></span><br/> | <dl> <span data-ttu-id="22870-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="22870-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22870-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22870-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22870-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="22870-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="22870-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="22870-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




