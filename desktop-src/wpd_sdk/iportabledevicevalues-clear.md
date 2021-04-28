---
description: 'IPortableDeviceValues::Clear-Methode: Die Clear-Methode löscht alle Elemente aus der Auflistung.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: IPortableDeviceValues::Clear-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109898"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="1c37f-103">IPortableDeviceValues::Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="1c37f-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="1c37f-104">Die **Clear-Methode** löscht alle Elemente aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1c37f-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c37f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c37f-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="1c37f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c37f-106">Parameters</span></span>

<span data-ttu-id="1c37f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1c37f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c37f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c37f-108">Return value</span></span>

<span data-ttu-id="1c37f-109">Die -Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1c37f-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c37f-110">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1c37f-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1c37f-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1c37f-111">Return code</span></span>                                                                          | <span data-ttu-id="1c37f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c37f-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1c37f-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c37f-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1c37f-114">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c37f-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c37f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c37f-115">Remarks</span></span>

<span data-ttu-id="1c37f-116">Diese Methode gibt den Arbeitsspeicher für alle dynamisch zugeordneten Elemente in der Auflistung frei.</span><span class="sxs-lookup"><span data-stu-id="1c37f-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="1c37f-117">Für Schnittstellen ruft es **Release auf.**</span><span class="sxs-lookup"><span data-stu-id="1c37f-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c37f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c37f-118">Requirements</span></span>



| <span data-ttu-id="1c37f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c37f-119">Requirement</span></span> | <span data-ttu-id="1c37f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1c37f-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c37f-121">Header</span><span class="sxs-lookup"><span data-stu-id="1c37f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1c37f-122"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c37f-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c37f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c37f-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c37f-124"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c37f-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c37f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c37f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c37f-126">**IPortableDeviceValues-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1c37f-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




