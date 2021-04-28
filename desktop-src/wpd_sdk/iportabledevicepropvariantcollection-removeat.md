---
description: 'IPortableDevicePropVariantCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an dem vom angegebenen Index angegebenen Speicherort gespeichert ist.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: IPortableDevicePropVariantCollection::RemoveAt-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109943"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="b8ccc-103">IPortableDevicePropVariantCollection::RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="b8ccc-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="b8ccc-104">Die **RemoveAt-Methode** entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ccc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ccc-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b8ccc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8ccc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ccc-107">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b8ccc-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ccc-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ccc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8ccc-109">Return value</span></span>

<span data-ttu-id="b8ccc-110">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="b8ccc-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b8ccc-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b8ccc-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b8ccc-112">Return code</span></span>                                                                                  | <span data-ttu-id="b8ccc-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8ccc-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b8ccc-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8ccc-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b8ccc-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="b8ccc-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b8ccc-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b8ccc-117">Der angegebene Index lag nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8ccc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8ccc-118">Remarks</span></span>

<span data-ttu-id="b8ccc-119">Sie müssen einen nullbasierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="b8ccc-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ccc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ccc-120">Requirements</span></span>



| <span data-ttu-id="b8ccc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ccc-121">Requirement</span></span> | <span data-ttu-id="b8ccc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b8ccc-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ccc-123">Header</span><span class="sxs-lookup"><span data-stu-id="b8ccc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b8ccc-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ccc-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8ccc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8ccc-125">Library</span></span><br/> | <dl> <span data-ttu-id="b8ccc-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8ccc-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ccc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8ccc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ccc-128">**IPortableDevicePropVariantCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b8ccc-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




