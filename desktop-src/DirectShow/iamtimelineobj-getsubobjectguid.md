---
description: Die getsubobjectguid-Methode ruft die GUID des untergeordneten Objekts ab, das diesem Zeitachsen Objekt zugeordnet ist.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: 'Iamtimelineobj:: getsubobjectguid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1c787bdbca8bbd255ccc78c3756fd0071d22f30d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364969"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a><span data-ttu-id="c22da-103">Iamtimelineobj:: getsubobjectguid-Methode</span><span class="sxs-lookup"><span data-stu-id="c22da-103">IAMTimelineObj::GetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="c22da-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c22da-104">\[Deprecated.</span></span> <span data-ttu-id="c22da-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c22da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c22da-106">Die- `GetSubObjectGUID` Methode ruft die GUID des untergeordneten Objekts ab, das diesem Zeitachsen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c22da-106">The `GetSubObjectGUID` method retrieves the GUID of the subobject associated with this timeline object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c22da-107">Syntax</span></span>


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c22da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c22da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22da-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="c22da-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c22da-110">Empfängt die GUID des unter Objekts oder GUID \_ NULL, wenn das Objekt nicht über ein untergeordnetes Objekt verfügt.</span><span class="sxs-lookup"><span data-stu-id="c22da-110">Receives the GUID of the subobject, or GUID\_NULL if the object does not have a subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22da-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c22da-111">Return value</span></span>

<span data-ttu-id="c22da-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c22da-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c22da-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c22da-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c22da-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c22da-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c22da-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c22da-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c22da-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c22da-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c22da-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c22da-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c22da-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c22da-118">Requirements</span></span>



| <span data-ttu-id="c22da-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c22da-119">Requirement</span></span> | <span data-ttu-id="c22da-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c22da-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c22da-121">Header</span><span class="sxs-lookup"><span data-stu-id="c22da-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c22da-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c22da-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c22da-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c22da-123">Library</span></span><br/> | <dl> <span data-ttu-id="c22da-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c22da-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22da-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c22da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22da-126">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c22da-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c22da-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c22da-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




