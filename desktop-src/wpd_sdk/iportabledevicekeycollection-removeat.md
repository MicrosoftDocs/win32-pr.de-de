---
description: 'IPortableDeviceKeyCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an dem vom angegebenen Index angegebenen Speicherort gespeichert ist.'
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: IPortableDeviceKeyCollection::RemoveAt-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109942"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="d628e-103">IPortableDeviceKeyCollection::RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="d628e-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="d628e-104">Die **RemoveAt-Methode** entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d628e-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d628e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d628e-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d628e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d628e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d628e-107">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d628e-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d628e-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="d628e-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d628e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d628e-109">Return value</span></span>

<span data-ttu-id="d628e-110">Die -Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="d628e-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d628e-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d628e-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d628e-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d628e-112">Return code</span></span>                                                                                  | <span data-ttu-id="d628e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d628e-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d628e-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d628e-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d628e-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d628e-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="d628e-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d628e-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d628e-117">Der angegebene Index lag außerhalb des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="d628e-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d628e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d628e-118">Remarks</span></span>

<span data-ttu-id="d628e-119">Sie müssen einen nullbasierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="d628e-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d628e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d628e-120">Requirements</span></span>



| <span data-ttu-id="d628e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d628e-121">Requirement</span></span> | <span data-ttu-id="d628e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d628e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d628e-123">Header</span><span class="sxs-lookup"><span data-stu-id="d628e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d628e-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="d628e-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d628e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d628e-125">Library</span></span><br/> | <dl> <span data-ttu-id="d628e-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d628e-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d628e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d628e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d628e-128">**IPortableDeviceKeyCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d628e-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




