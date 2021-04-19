---
description: Die getgenid-Methode ruft den generierten Bezeichner des Objekts ab. Der Bezeichner ist eine reservierte Zahl. Anwendungen sollten Sie nicht verwenden.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Iamtimelineobj:: getgenid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366833"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="21569-104">Iamtimelineobj:: getgenid-Methode</span><span class="sxs-lookup"><span data-stu-id="21569-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="21569-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21569-105">\[Deprecated.</span></span> <span data-ttu-id="21569-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="21569-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21569-107">Die `GetGenID` -Methode ruft den generierten Bezeichner des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="21569-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="21569-108">Der Bezeichner ist eine reservierte Zahl. Anwendungen sollten Sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="21569-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="21569-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="21569-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="21569-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="21569-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21569-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="21569-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="21569-112">Empfängt den generierten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="21569-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21569-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21569-113">Return value</span></span>

<span data-ttu-id="21569-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="21569-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21569-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21569-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21569-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21569-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21569-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="21569-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21569-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="21569-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21569-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21569-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21569-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21569-120">Requirements</span></span>



| <span data-ttu-id="21569-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21569-121">Requirement</span></span> | <span data-ttu-id="21569-122">Wert</span><span class="sxs-lookup"><span data-stu-id="21569-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21569-123">Header</span><span class="sxs-lookup"><span data-stu-id="21569-123">Header</span></span><br/>  | <dl> <span data-ttu-id="21569-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21569-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21569-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21569-125">Library</span></span><br/> | <dl> <span data-ttu-id="21569-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="21569-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21569-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21569-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21569-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="21569-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="21569-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="21569-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




