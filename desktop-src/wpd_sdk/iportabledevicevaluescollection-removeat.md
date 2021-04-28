---
description: 'IPortableDeviceValuesCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an dem vom angegebenen Index angegebenen Speicherort gespeichert ist.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: IPortableDeviceValuesCollection::RemoveAt-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083168"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="ac7c8-103">IPortableDeviceValuesCollection::RemoveAt-Methode</span><span class="sxs-lookup"><span data-stu-id="ac7c8-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="ac7c8-104">Die **RemoveAt-Methode** entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac7c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac7c8-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="ac7c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac7c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac7c8-107">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ac7c8-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac7c8-108">Gibt den Index des zu entfernenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac7c8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac7c8-109">Return value</span></span>

<span data-ttu-id="ac7c8-110">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="ac7c8-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac7c8-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac7c8-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac7c8-112">Return code</span></span>                                                                                  | <span data-ttu-id="ac7c8-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac7c8-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ac7c8-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c8-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ac7c8-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="ac7c8-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c8-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ac7c8-117">Der angegebene Index lag nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac7c8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac7c8-118">Remarks</span></span>

<span data-ttu-id="ac7c8-119">Sie müssen einen nullbasierten Index angeben.</span><span class="sxs-lookup"><span data-stu-id="ac7c8-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7c8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac7c8-120">Requirements</span></span>



| <span data-ttu-id="ac7c8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac7c8-121">Requirement</span></span> | <span data-ttu-id="ac7c8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ac7c8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7c8-123">Header</span><span class="sxs-lookup"><span data-stu-id="ac7c8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ac7c8-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c8-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac7c8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac7c8-125">Library</span></span><br/> | <dl> <span data-ttu-id="ac7c8-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac7c8-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac7c8-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ac7c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7c8-128">**IPortableDeviceValuesCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ac7c8-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




