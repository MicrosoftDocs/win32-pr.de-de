---
description: Die setsubobjectguid-Methode gibt die GUID des untergeordneten Objekts an, das diesem Objekt zugeordnet ist.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Iamtimelineobj:: setsubobjectguid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369178"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="8d9e8-103">Iamtimelineobj:: setsubobjectguid-Methode</span><span class="sxs-lookup"><span data-stu-id="8d9e8-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="8d9e8-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-104">\[Deprecated.</span></span> <span data-ttu-id="8d9e8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="8d9e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8d9e8-106">Die- `SetSubObjectGUID` Methode gibt die GUID des untergeordneten Objekts an, das diesem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d9e8-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="8d9e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d9e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9e8-109">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="8d9e8-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8d9e8-110">GUID des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d9e8-111">Return value</span></span>

<span data-ttu-id="8d9e8-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d9e8-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9e8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d9e8-114">Remarks</span></span>

<span data-ttu-id="8d9e8-115">Die Rendering-Engine erstellt nach Bedarf eine Instanz des untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="8d9e8-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8d9e8-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8d9e8-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8d9e8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d9e8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d9e8-119">Requirements</span></span>



| <span data-ttu-id="8d9e8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d9e8-120">Requirement</span></span> | <span data-ttu-id="8d9e8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8d9e8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="8d9e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8d9e8-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8d9e8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d9e8-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8d9e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="8d9e8-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="8d9e8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d9e8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d9e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9e8-127">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8d9e8-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8d9e8-128">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="8d9e8-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




