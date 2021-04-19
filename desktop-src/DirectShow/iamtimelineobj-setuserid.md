---
description: Die setuserid-Methode legt einen von der Anwendung definierten Bezeichner für das-Objekt fest.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'Iamtimelineobj:: setuserid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365707"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="e4b77-103">Iamtimelineobj:: setuserid-Methode</span><span class="sxs-lookup"><span data-stu-id="e4b77-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="e4b77-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e4b77-104">\[Deprecated.</span></span> <span data-ttu-id="e4b77-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e4b77-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e4b77-106">Die `SetUserID` -Methode legt einen von der Anwendung definierten Bezeichner für das-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="e4b77-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b77-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4b77-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e4b77-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4b77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b77-109">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="e4b77-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b77-110">Der-Wert, der den Bezeichner angibt.</span><span class="sxs-lookup"><span data-stu-id="e4b77-110">Value that specifies the identifier.</span></span> <span data-ttu-id="e4b77-111">Dieser Bezeichner wird nur von der Anwendung verwendet und kann ein beliebiger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="e4b77-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b77-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4b77-112">Return value</span></span>

<span data-ttu-id="e4b77-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4b77-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4b77-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4b77-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b77-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4b77-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4b77-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e4b77-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4b77-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e4b77-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e4b77-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e4b77-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4b77-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4b77-119">Requirements</span></span>



| <span data-ttu-id="e4b77-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4b77-120">Requirement</span></span> | <span data-ttu-id="e4b77-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e4b77-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b77-122">Header</span><span class="sxs-lookup"><span data-stu-id="e4b77-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b77-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e4b77-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e4b77-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4b77-124">Library</span></span><br/> | <dl> <span data-ttu-id="e4b77-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e4b77-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b77-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4b77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b77-127">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e4b77-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e4b77-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e4b77-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




