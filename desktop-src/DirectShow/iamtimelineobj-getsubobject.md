---
description: Die getsubobject-Methode ruft das diesem Objekt zugeordnete untergeordnete Objekt ab.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Iamtimelineobj:: getsubobject-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367026"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="dc8ea-103">Iamtimelineobj:: getsubobject-Methode</span><span class="sxs-lookup"><span data-stu-id="dc8ea-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="dc8ea-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-104">\[Deprecated.</span></span> <span data-ttu-id="dc8ea-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="dc8ea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc8ea-106">Die- `GetSubObject` Methode ruft das diesem-Objekt zugeordnete untergeordnete Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc8ea-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="dc8ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc8ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc8ea-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dc8ea-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8ea-110">Empfängt einen Zeiger auf die **IUnknown** -Schnittstelle des SubObject.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="dc8ea-111">Wenn das Objekt kein untergeordnetes Objekt hat, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc8ea-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc8ea-112">Return value</span></span>

<span data-ttu-id="dc8ea-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc8ea-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc8ea-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc8ea-115">Remarks</span></span>

<span data-ttu-id="dc8ea-116">Jedes Zeitachsen Objekt kann einen Zeiger auf ein zugeordnetes untergeordnetes Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="dc8ea-117">Wenn der in *PVal* zurückgegebene Wert nicht **null** ist, weist die **IUnknown** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="dc8ea-118">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="dc8ea-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc8ea-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc8ea-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc8ea-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc8ea-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc8ea-122">Requirements</span></span>



| <span data-ttu-id="dc8ea-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc8ea-123">Requirement</span></span> | <span data-ttu-id="dc8ea-124">Wert</span><span class="sxs-lookup"><span data-stu-id="dc8ea-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8ea-125">Header</span><span class="sxs-lookup"><span data-stu-id="dc8ea-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dc8ea-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dc8ea-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc8ea-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc8ea-127">Library</span></span><br/> | <dl> <span data-ttu-id="dc8ea-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="dc8ea-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc8ea-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc8ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8ea-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dc8ea-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="dc8ea-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="dc8ea-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




