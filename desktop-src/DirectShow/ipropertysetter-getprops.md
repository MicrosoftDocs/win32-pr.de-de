---
description: Die GetProperties-Methode ruft die Eigenschaften, die für dieses Objekt festgelegt sind, mit den entsprechenden Werten ab.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Ipropertysetter:: getrequiemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365955"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="e0aa4-103">Ipropertysetter:: getrequismethode</span><span class="sxs-lookup"><span data-stu-id="e0aa4-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="e0aa4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-104">\[Deprecated.</span></span> <span data-ttu-id="e0aa4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e0aa4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0aa4-106">Die- `GetProps` Methode ruft die für dieses-Objekt festgelegten Eigenschaften mit ihren entsprechenden Werten ab.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aa4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0aa4-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="e0aa4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0aa4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0aa4-109">*pcparametriams* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0aa4-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa4-110">Empfängt die Anzahl der in einem *paar* zurückgegebenen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="e0aa4-111">mit einem *paar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0aa4-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa4-112">Adresse eines Zeigers auf ein Array von [**Dexter \_ param**](dexter-param.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e0aa4-113">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0aa4-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa4-114">Adresse eines Zeigers auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0aa4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0aa4-115">Return value</span></span>

<span data-ttu-id="e0aa4-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0aa4-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0aa4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0aa4-118">Remarks</span></span>

<span data-ttu-id="e0aa4-119">Der **nvalues** -Member gibt für jede Eigenschaft, die in der-Eigenschaft zurückgegeben wird, die Anzahl der der Eigenschaft zugeordneten [**Dexter- \_ Wert**](dexter-value.md) *Strukturen an.*</span><span class="sxs-lookup"><span data-stu-id="e0aa4-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="e0aa4-120">Die Paare werden für jede Eigenschaft in aufsteigender Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="e0aa4-121">Wenn Sie mit der Verwendung der zurückgegebenen Strukturen fertig sind, müssen Sie [**ipropertysetter:: Free-Eigenschaften**](ipropertysetter-freeprops.md) aufrufen, um die von dieser Methode zugeordneten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="e0aa4-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0aa4-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e0aa4-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0aa4-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e0aa4-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0aa4-125">Examples</span></span>

<span data-ttu-id="e0aa4-126">Im folgenden Codebeispiel wird gezeigt, wie alle Werte in einer Instanz des Eigenschaften Setter durchlaufen werden:</span><span class="sxs-lookup"><span data-stu-id="e0aa4-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="e0aa4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0aa4-127">Requirements</span></span>



| <span data-ttu-id="e0aa4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0aa4-128">Requirement</span></span> | <span data-ttu-id="e0aa4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e0aa4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aa4-130">Header</span><span class="sxs-lookup"><span data-stu-id="e0aa4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e0aa4-131"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa4-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e0aa4-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0aa4-132">Library</span></span><br/> | <dl> <span data-ttu-id="e0aa4-133"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa4-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0aa4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0aa4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aa4-135">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e0aa4-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="e0aa4-136">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e0aa4-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




