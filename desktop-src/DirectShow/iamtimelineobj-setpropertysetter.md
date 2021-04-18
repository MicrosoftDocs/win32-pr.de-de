---
description: Die setpropertysetter-Methode legt den Eigenschaften Setter des Objekts fest. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet. Diese Methode wird bei Übergangs-und Effekt Objekten aufgerufen.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Iamtimelineobj:: setpropertysetter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371670"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="802a9-105">Iamtimelineobj:: setpropertysetter-Methode</span><span class="sxs-lookup"><span data-stu-id="802a9-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="802a9-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="802a9-106">\[Deprecated.</span></span> <span data-ttu-id="802a9-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="802a9-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="802a9-108">Die `SetPropertySetter` -Methode legt den Eigenschaften Setter des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="802a9-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="802a9-109">Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet.</span><span class="sxs-lookup"><span data-stu-id="802a9-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="802a9-110">Diese Methode wird bei Übergangs-und Effekt Objekten aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="802a9-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="802a9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="802a9-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="802a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="802a9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="802a9-113">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="802a9-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="802a9-114">Ein Zeiger auf die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle des Eigenschaften Setters.</span><span class="sxs-lookup"><span data-stu-id="802a9-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="802a9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="802a9-115">Return value</span></span>

<span data-ttu-id="802a9-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="802a9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="802a9-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="802a9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="802a9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="802a9-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="802a9-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="802a9-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="802a9-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="802a9-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="802a9-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="802a9-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="802a9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="802a9-122">Requirements</span></span>



| <span data-ttu-id="802a9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="802a9-123">Requirement</span></span> | <span data-ttu-id="802a9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="802a9-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="802a9-125">Header</span><span class="sxs-lookup"><span data-stu-id="802a9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="802a9-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="802a9-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="802a9-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="802a9-127">Library</span></span><br/> | <dl> <span data-ttu-id="802a9-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="802a9-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="802a9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="802a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802a9-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="802a9-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="802a9-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="802a9-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




