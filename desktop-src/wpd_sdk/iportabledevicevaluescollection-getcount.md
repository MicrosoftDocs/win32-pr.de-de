---
description: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Iportabledevicevaluescollection:: GetCount-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353810"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="5a718-103">Iportabledevicevaluescollection:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="5a718-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="5a718-104">Die **GetCount** -Methode ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="5a718-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a718-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a718-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="5a718-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a718-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a718-107">*pcelems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a718-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a718-108">Zeiger auf ein **DWORD** , das die Anzahl der **iportabledevicevalues** -Schnittstellen in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="5a718-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a718-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a718-109">Return value</span></span>

<span data-ttu-id="5a718-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a718-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a718-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a718-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a718-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5a718-112">Return code</span></span>                                                                               | <span data-ttu-id="5a718-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a718-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5a718-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a718-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5a718-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a718-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="5a718-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="5a718-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5a718-117">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="5a718-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a718-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a718-118">Requirements</span></span>



| <span data-ttu-id="5a718-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a718-119">Requirement</span></span> | <span data-ttu-id="5a718-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5a718-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a718-121">Header</span><span class="sxs-lookup"><span data-stu-id="5a718-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5a718-122"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a718-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a718-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a718-123">Library</span></span><br/> | <dl> <span data-ttu-id="5a718-124"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a718-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a718-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a718-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a718-126">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5a718-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




