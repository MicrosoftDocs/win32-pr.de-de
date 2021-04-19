---
description: Die RemoveAt-Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'Iportabledevicevaluescollection:: RemoveAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 004e8d855e79075fe3ae83bbde695e42487963f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367529"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="51e75-103">Iportabledevicevaluescollection:: RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="51e75-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="51e75-104">Die **RemoveAt** -Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="51e75-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51e75-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="51e75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51e75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e75-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51e75-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e75-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="51e75-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e75-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51e75-109">Return value</span></span>

<span data-ttu-id="51e75-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="51e75-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="51e75-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51e75-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="51e75-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="51e75-112">Return code</span></span>                                                                                  | <span data-ttu-id="51e75-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51e75-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="51e75-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51e75-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="51e75-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51e75-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="51e75-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="51e75-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="51e75-117">Der angegebene Index lag außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="51e75-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51e75-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51e75-118">Remarks</span></span>

<span data-ttu-id="51e75-119">Sie müssen einen NULL basierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="51e75-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e75-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51e75-120">Requirements</span></span>



| <span data-ttu-id="51e75-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51e75-121">Requirement</span></span> | <span data-ttu-id="51e75-122">Wert</span><span class="sxs-lookup"><span data-stu-id="51e75-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e75-123">Header</span><span class="sxs-lookup"><span data-stu-id="51e75-123">Header</span></span><br/>  | <dl> <span data-ttu-id="51e75-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e75-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="51e75-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51e75-125">Library</span></span><br/> | <dl> <span data-ttu-id="51e75-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51e75-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e75-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51e75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e75-128">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="51e75-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




