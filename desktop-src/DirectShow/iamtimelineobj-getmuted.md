---
description: Die getgedämpf-Methode ruft den gedämpften Zustand des Objekts ab.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'Iamtimelineobj:: getgedämpf-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359713"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="0e599-103">Iamtimelineobj:: getgedämpf-Methode</span><span class="sxs-lookup"><span data-stu-id="0e599-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="0e599-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0e599-104">\[Deprecated.</span></span> <span data-ttu-id="0e599-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0e599-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0e599-106">Die `GetMuted` -Methode ruft den gedämpften Zustand des-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="0e599-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e599-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e599-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0e599-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e599-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="0e599-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0e599-110">Empfängt einen Wert, der den Status "stumm" angibt.</span><span class="sxs-lookup"><span data-stu-id="0e599-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="0e599-111">Wenn der Wert **true** ist, werden das-Objekt und seine untergeordneten Elemente stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="0e599-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e599-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e599-112">Return value</span></span>

<span data-ttu-id="0e599-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e599-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e599-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e599-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e599-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e599-115">Remarks</span></span>

<span data-ttu-id="0e599-116">Wenn das übergeordnete Element eines Objekts stumm geschaltet wird, wird das Objekt unabhängig von seinem gedämpften Zustand stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="0e599-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="0e599-117">Wenn das übergeordnete Element nicht mehr stumm geschaltet wird, wird der vorherige stumm Zustand des Objekts wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="0e599-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="0e599-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0e599-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e599-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0e599-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0e599-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e599-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e599-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e599-121">Requirements</span></span>



| <span data-ttu-id="0e599-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e599-122">Requirement</span></span> | <span data-ttu-id="0e599-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0e599-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e599-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e599-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e599-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0e599-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0e599-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e599-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e599-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0e599-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e599-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e599-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e599-129">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0e599-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="0e599-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="0e599-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




