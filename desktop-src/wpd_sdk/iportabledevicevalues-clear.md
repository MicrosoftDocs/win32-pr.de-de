---
description: Die Clear-Methode löscht alle Elemente aus der Auflistung.
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'Iportabledevicevalues:: Clear-Methode (portabledevicetypes. h)'
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
ms.openlocfilehash: 45c04319b5691e3bbcfb56d5a447cf2eb60bfaac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352923"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="0e693-103">Iportabledevicevalues:: Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="0e693-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="0e693-104">Die **Clear** -Methode löscht alle Elemente aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0e693-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e693-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e693-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="0e693-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e693-106">Parameters</span></span>

<span data-ttu-id="0e693-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0e693-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e693-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e693-108">Return value</span></span>

<span data-ttu-id="0e693-109">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e693-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0e693-110">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e693-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0e693-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0e693-111">Return code</span></span>                                                                          | <span data-ttu-id="0e693-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e693-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0e693-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e693-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0e693-114">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e693-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e693-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e693-115">Remarks</span></span>

<span data-ttu-id="0e693-116">Diese Methode gibt den Speicher für alle dynamisch zugewiesenen Elemente in der Auflistung frei.</span><span class="sxs-lookup"><span data-stu-id="0e693-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="0e693-117">Für Schnittstellen wird **Release** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0e693-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e693-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e693-118">Requirements</span></span>



| <span data-ttu-id="0e693-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e693-119">Requirement</span></span> | <span data-ttu-id="0e693-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0e693-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e693-121">Header</span><span class="sxs-lookup"><span data-stu-id="0e693-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0e693-122"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e693-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e693-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e693-123">Library</span></span><br/> | <dl> <span data-ttu-id="0e693-124"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e693-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e693-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e693-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e693-126">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0e693-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




