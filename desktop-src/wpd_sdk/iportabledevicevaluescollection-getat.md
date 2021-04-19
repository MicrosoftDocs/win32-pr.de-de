---
description: Die GetAt-Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Iportabledevicevaluescollection:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373590"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="ee2cb-103">Iportabledevicevaluescollection:: GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="ee2cb-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="ee2cb-104">Die **GetAt** -Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee2cb-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="ee2cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee2cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee2cb-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee2cb-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2cb-108">**DWORD** , das einen NULL basierten Index in der Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ee2cb-109">*ppvalues* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee2cb-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee2cb-110">Adresse einer Variablen, die einen Zeiger auf eine [**iportableendvicevalues**](iportabledevicevalues.md) -Schnittstelle aus der Auflistung empfängt.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="ee2cb-111">Der Aufrufer ist für das Aufrufen der **Freigabe** auf dieser Schnittstelle verantwortlich, wenn er damit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee2cb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee2cb-112">Return value</span></span>

<span data-ttu-id="ee2cb-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ee2cb-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ee2cb-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ee2cb-115">Return code</span></span>                                                                                  | <span data-ttu-id="ee2cb-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee2cb-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee2cb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ee2cb-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="ee2cb-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ee2cb-120">Der null basierte Index, der in der Übergabe war, liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="ee2cb-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ee2cb-122">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="ee2cb-123"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="ee2cb-124">Die-Auflistung enthält einen **null** - **iportableendvicevalues** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee2cb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee2cb-125">Remarks</span></span>

<span data-ttu-id="ee2cb-126">Alle Änderungen, die an Werten in der abgerufenen Schnittstelle vorgenommen werden, werden an der in der Auflistung gespeicherten Version vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="ee2cb-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2cb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee2cb-127">Requirements</span></span>



| <span data-ttu-id="ee2cb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee2cb-128">Requirement</span></span> | <span data-ttu-id="ee2cb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ee2cb-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee2cb-130">Header</span><span class="sxs-lookup"><span data-stu-id="ee2cb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ee2cb-131"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee2cb-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee2cb-132">Library</span></span><br/> | <dl> <span data-ttu-id="ee2cb-133"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee2cb-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee2cb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee2cb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2cb-135">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ee2cb-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




