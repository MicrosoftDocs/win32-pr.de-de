---
description: Die RemoveAt-Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Iportabledevicepropvariantcollection:: RemoveAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351231"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="5ab77-103">Iportabledevicepropvariantcollection:: RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="5ab77-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="5ab77-104">Die **RemoveAt** -Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5ab77-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab77-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="5ab77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab77-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ab77-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab77-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="5ab77-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ab77-109">Return value</span></span>

<span data-ttu-id="5ab77-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5ab77-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5ab77-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5ab77-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5ab77-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5ab77-112">Return code</span></span>                                                                                  | <span data-ttu-id="5ab77-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ab77-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5ab77-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5ab77-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ab77-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="5ab77-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5ab77-117">Der angegebene Index lag außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5ab77-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ab77-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ab77-118">Remarks</span></span>

<span data-ttu-id="5ab77-119">Sie müssen einen NULL basierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="5ab77-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab77-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ab77-120">Requirements</span></span>



| <span data-ttu-id="5ab77-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ab77-121">Requirement</span></span> | <span data-ttu-id="5ab77-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab77-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab77-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ab77-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5ab77-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ab77-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ab77-125">Library</span></span><br/> | <dl> <span data-ttu-id="5ab77-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ab77-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab77-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ab77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab77-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5ab77-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




