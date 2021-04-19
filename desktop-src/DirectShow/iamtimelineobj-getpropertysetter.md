---
description: Die getpropertysetter-Methode ruft den Eigenschaften Setter des Objekts ab. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Iamtimelineobj:: getpropertysetter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373923"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="097f4-104">Iamtimelineobj:: getpropertysetter-Methode</span><span class="sxs-lookup"><span data-stu-id="097f4-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="097f4-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="097f4-105">\[Deprecated.</span></span> <span data-ttu-id="097f4-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="097f4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="097f4-107">Die `GetPropertySetter` -Methode ruft den Eigenschaften Setter des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="097f4-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="097f4-108">Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet.</span><span class="sxs-lookup"><span data-stu-id="097f4-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="097f4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="097f4-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="097f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="097f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097f4-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="097f4-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="097f4-112">Empfängt einen Zeiger auf die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle des Eigenschaften Setters.</span><span class="sxs-lookup"><span data-stu-id="097f4-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="097f4-113">Wenn das Objekt keinen Eigenschaften Setter aufweist, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="097f4-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097f4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="097f4-114">Return value</span></span>

<span data-ttu-id="097f4-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="097f4-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="097f4-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="097f4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="097f4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="097f4-117">Remarks</span></span>

<span data-ttu-id="097f4-118">Wenn der in *PVal* zurückgegebene Wert nicht **null** ist, weist die **ipropertysetter** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="097f4-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="097f4-119">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="097f4-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="097f4-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="097f4-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="097f4-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="097f4-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="097f4-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="097f4-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="097f4-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="097f4-123">Requirements</span></span>



| <span data-ttu-id="097f4-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="097f4-124">Requirement</span></span> | <span data-ttu-id="097f4-125">Wert</span><span class="sxs-lookup"><span data-stu-id="097f4-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="097f4-126">Header</span><span class="sxs-lookup"><span data-stu-id="097f4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="097f4-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="097f4-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="097f4-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="097f4-128">Library</span></span><br/> | <dl> <span data-ttu-id="097f4-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="097f4-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097f4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="097f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097f4-131">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="097f4-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="097f4-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="097f4-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




