---
description: Die RemoveAt-Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Iportabledevicekeycollection:: RemoveAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371504"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="4f105-103">Iportabledevicekeycollection:: RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="4f105-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="4f105-104">Die **RemoveAt** -Methode entfernt das Element, das an der durch den angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4f105-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f105-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f105-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="4f105-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f105-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f105-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f105-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="4f105-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f105-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f105-109">Return value</span></span>

<span data-ttu-id="4f105-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4f105-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f105-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4f105-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f105-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4f105-112">Return code</span></span>                                                                                  | <span data-ttu-id="4f105-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f105-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4f105-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f105-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4f105-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f105-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="4f105-116"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4f105-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4f105-117">Der angegebene Index lag außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4f105-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f105-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f105-118">Remarks</span></span>

<span data-ttu-id="4f105-119">Sie müssen einen NULL basierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="4f105-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f105-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f105-120">Requirements</span></span>



| <span data-ttu-id="4f105-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f105-121">Requirement</span></span> | <span data-ttu-id="4f105-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4f105-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f105-123">Header</span><span class="sxs-lookup"><span data-stu-id="4f105-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4f105-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f105-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f105-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f105-125">Library</span></span><br/> | <dl> <span data-ttu-id="4f105-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f105-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f105-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f105-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f105-128">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4f105-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




