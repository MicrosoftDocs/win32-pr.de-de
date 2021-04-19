---
description: Die gettimelinetype-Methode ruft den Typ des Objekts ab.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'Iamtimelineobj:: gettimelinetype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353785"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="a21f4-103">Iamtimelineobj:: gettimelinetype-Methode</span><span class="sxs-lookup"><span data-stu-id="a21f4-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="a21f4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a21f4-104">\[Deprecated.</span></span> <span data-ttu-id="a21f4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a21f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a21f4-106">Die `GetTimelineType` -Methode ruft den Typ des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="a21f4-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21f4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21f4-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a21f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21f4-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a21f4-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a21f4-110">Empfängt einen Member des enumerierten Typs der Zeitachse, der den Objekttyp angibt. [**\_ \_**](timeline-major-type.md)</span><span class="sxs-lookup"><span data-stu-id="a21f4-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21f4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a21f4-111">Return value</span></span>

<span data-ttu-id="a21f4-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a21f4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a21f4-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a21f4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a21f4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a21f4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a21f4-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a21f4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a21f4-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="a21f4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a21f4-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a21f4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a21f4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a21f4-118">Requirements</span></span>



| <span data-ttu-id="a21f4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a21f4-119">Requirement</span></span> | <span data-ttu-id="a21f4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a21f4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a21f4-121">Header</span><span class="sxs-lookup"><span data-stu-id="a21f4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a21f4-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a21f4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a21f4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a21f4-123">Library</span></span><br/> | <dl> <span data-ttu-id="a21f4-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="a21f4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21f4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a21f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21f4-126">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a21f4-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="a21f4-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="a21f4-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




