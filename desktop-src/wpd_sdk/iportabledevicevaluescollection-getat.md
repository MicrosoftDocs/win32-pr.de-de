---
description: 'IPortableDeviceValuesCollection::GetAt-Methode: Die GetAt-Methode ruft ein Element von einem nullbasierten Index aus der Auflistung ab.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: IPortableDeviceValuesCollection::GetAt-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083256"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="52599-103">IPortableDeviceValuesCollection::GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="52599-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="52599-104">Die **GetAt-Methode** ruft ein Element von einem nullbasierten Index aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="52599-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="52599-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52599-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="52599-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52599-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52599-107">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="52599-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52599-108">**DWORD,** das einen nullbasierten Index in der Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="52599-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="52599-109">*ppValues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52599-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52599-110">Adresse einer Variablen, die einen Zeiger auf eine [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md) aus der Auflistung empfängt.</span><span class="sxs-lookup"><span data-stu-id="52599-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="52599-111">Der Aufrufer ist für den Aufruf von **Release auf** dieser Schnittstelle verantwortlich, wenn er damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="52599-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52599-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52599-112">Return value</span></span>

<span data-ttu-id="52599-113">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="52599-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52599-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="52599-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52599-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="52599-115">Return code</span></span>                                                                                  | <span data-ttu-id="52599-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52599-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52599-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52599-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="52599-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52599-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="52599-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="52599-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="52599-120">Der nullbasierte Index, der übergeben wurde, lag nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="52599-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="52599-121"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="52599-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="52599-122">Ein erforderliches Zeigerargument war **NULL.**</span><span class="sxs-lookup"><span data-stu-id="52599-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="52599-123"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="52599-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="52599-124">Die Auflistung enthält einen  **NULL-IPortableDeviceValues-Zeiger.**</span><span class="sxs-lookup"><span data-stu-id="52599-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52599-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52599-125">Remarks</span></span>

<span data-ttu-id="52599-126">Alle Änderungen, die an Werten in der abgerufenen Schnittstelle vorgenommen werden, werden an der in der Auflistung gespeicherten Version vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="52599-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="52599-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52599-127">Requirements</span></span>



| <span data-ttu-id="52599-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52599-128">Requirement</span></span> | <span data-ttu-id="52599-129">Wert</span><span class="sxs-lookup"><span data-stu-id="52599-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52599-130">Header</span><span class="sxs-lookup"><span data-stu-id="52599-130">Header</span></span><br/>  | <dl> <span data-ttu-id="52599-131"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="52599-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="52599-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52599-132">Library</span></span><br/> | <dl> <span data-ttu-id="52599-133"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="52599-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52599-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52599-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52599-135">**IPortableDeviceValuesCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="52599-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




