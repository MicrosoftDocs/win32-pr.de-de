---
description: 'Die Methode "frei-Eigenschaften" gibt Ressourcen frei, die von der ipropertysetter:: getrequiemethode zugeordnet werden. Rufen Sie diese Methode nach dem Aufrufen von gettial auf, und übergeben Sie dabei die von gettial zurückgegebenen Strukturen.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Ipropertysetter:: frerequiproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352875"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="91df3-104">Ipropertysetter:: frerequismethode</span><span class="sxs-lookup"><span data-stu-id="91df3-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="91df3-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="91df3-105">\[Deprecated.</span></span> <span data-ttu-id="91df3-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="91df3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="91df3-107">Die-Methode gibt Ressourcen frei, `FreeProps` die von der [**ipropertysetter:: getrequiemethode**](ipropertysetter-getprops.md) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="91df3-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="91df3-108">Rufen Sie diese Methode nach dem Aufrufen von **gettial** auf, und übergeben Sie dabei die von **gettial** zurückgegebenen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="91df3-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="91df3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91df3-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="91df3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91df3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91df3-111">*cparameams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91df3-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df3-112">Die Anzahl der Elemente *im Array Array* .</span><span class="sxs-lookup"><span data-stu-id="91df3-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="91df3-113">mit einem *paar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91df3-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df3-114">Zeiger auf ein Array von [**Dexter- \_ param**](dexter-param.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="91df3-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="91df3-115">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91df3-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91df3-116">Zeiger auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="91df3-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91df3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91df3-117">Return value</span></span>

<span data-ttu-id="91df3-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="91df3-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91df3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91df3-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91df3-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="91df3-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="91df3-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="91df3-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="91df3-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91df3-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91df3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91df3-123">Requirements</span></span>



| <span data-ttu-id="91df3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91df3-124">Requirement</span></span> | <span data-ttu-id="91df3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="91df3-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91df3-126">Header</span><span class="sxs-lookup"><span data-stu-id="91df3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="91df3-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="91df3-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="91df3-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91df3-128">Library</span></span><br/> | <dl> <span data-ttu-id="91df3-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="91df3-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91df3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91df3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91df3-131">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91df3-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="91df3-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="91df3-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




