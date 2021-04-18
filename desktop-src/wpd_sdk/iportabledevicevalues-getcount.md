---
description: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'Iportabledevicevalues:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361041"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="5851e-103">Iportabledevicevalues:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="5851e-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="5851e-104">Die **GetCount** -Methode ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="5851e-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5851e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5851e-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="5851e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5851e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5851e-107">*pcelt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5851e-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5851e-108">Zeiger auf ein **DWORD** , das die Anzahl der Elemente in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="5851e-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5851e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5851e-109">Return value</span></span>

<span data-ttu-id="5851e-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5851e-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5851e-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5851e-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5851e-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5851e-112">Return code</span></span>                                                                          | <span data-ttu-id="5851e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5851e-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5851e-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5851e-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5851e-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5851e-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5851e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5851e-116">Requirements</span></span>



| <span data-ttu-id="5851e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5851e-117">Requirement</span></span> | <span data-ttu-id="5851e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5851e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5851e-119">Header</span><span class="sxs-lookup"><span data-stu-id="5851e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5851e-120"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5851e-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5851e-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5851e-121">Library</span></span><br/> | <dl> <span data-ttu-id="5851e-122"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5851e-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5851e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5851e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5851e-124">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5851e-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




