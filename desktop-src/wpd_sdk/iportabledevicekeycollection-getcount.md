---
description: Die GetCount-Methode ruft die Anzahl der Schlüssel in dieser Auflistung ab.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'Iportabledevicekeycollection:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358735"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="4d4ba-103">Iportabledevicekeycollection:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="4d4ba-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="4d4ba-104">Die **GetCount** -Methode ruft die Anzahl der Schlüssel in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d4ba-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="4d4ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d4ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d4ba-107">*pcelems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d4ba-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d4ba-108">Zeiger auf ein **DWORD** , das die Anzahl der Schlüssel in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d4ba-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d4ba-109">Return value</span></span>

<span data-ttu-id="4d4ba-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4d4ba-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4d4ba-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4d4ba-112">Return code</span></span>                                                                               | <span data-ttu-id="4d4ba-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d4ba-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4d4ba-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4ba-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4d4ba-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="4d4ba-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4d4ba-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4d4ba-117">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="4d4ba-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4d4ba-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d4ba-118">Examples</span></span>

<span data-ttu-id="4d4ba-119">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="4d4ba-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4ba-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d4ba-120">Requirements</span></span>



| <span data-ttu-id="4d4ba-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d4ba-121">Requirement</span></span> | <span data-ttu-id="4d4ba-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4d4ba-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4ba-123">Header</span><span class="sxs-lookup"><span data-stu-id="4d4ba-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4d4ba-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d4ba-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d4ba-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d4ba-125">Library</span></span><br/> | <dl> <span data-ttu-id="4d4ba-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d4ba-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d4ba-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d4ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4ba-128">**Iportabledevicekeycollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4d4ba-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="4d4ba-129">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4d4ba-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="4d4ba-130">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="4d4ba-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




