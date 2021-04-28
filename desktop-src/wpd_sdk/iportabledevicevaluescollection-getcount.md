---
description: 'IPortableDeviceValuesCollection::GetCount-Methode: Die GetCount-Methode ruft die Anzahl der Elemente in der Auflistung ab.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: IPortableDeviceValuesCollection::GetCount-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083178"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="a8cf8-103">IPortableDeviceValuesCollection::GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="a8cf8-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="a8cf8-104">Die **GetCount-Methode** ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="a8cf8-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8cf8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8cf8-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="a8cf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8cf8-107">*pcElems* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a8cf8-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8cf8-108">Zeiger auf ein **DWORD,** das die Anzahl der **IPortableDeviceValues-Schnittstellen** in der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="a8cf8-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8cf8-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8cf8-109">Return value</span></span>

<span data-ttu-id="a8cf8-110">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="a8cf8-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a8cf8-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8cf8-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a8cf8-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a8cf8-112">Return code</span></span>                                                                               | <span data-ttu-id="a8cf8-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8cf8-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a8cf8-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8cf8-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="a8cf8-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8cf8-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="a8cf8-116"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="a8cf8-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a8cf8-117">Ein erforderliches Zeigerargument war **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a8cf8-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8cf8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8cf8-118">Requirements</span></span>



| <span data-ttu-id="a8cf8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8cf8-119">Requirement</span></span> | <span data-ttu-id="a8cf8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a8cf8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8cf8-121">Header</span><span class="sxs-lookup"><span data-stu-id="a8cf8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a8cf8-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="a8cf8-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8cf8-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8cf8-123">Library</span></span><br/> | <dl> <span data-ttu-id="a8cf8-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8cf8-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8cf8-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8cf8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8cf8-126">**IPortableDeviceValuesCollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a8cf8-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




