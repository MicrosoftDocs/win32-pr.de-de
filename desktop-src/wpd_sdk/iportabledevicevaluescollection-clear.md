---
description: Die Clear-Methode gibt alle Elemente aus der Auflistung frei.
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'Iportabledevicevaluescollection:: Clear-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356315"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="ca700-103">Iportabledevicevaluescollection:: Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="ca700-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="ca700-104">Die **Clear** -Methode gibt alle Elemente aus der Auflistung frei.</span><span class="sxs-lookup"><span data-stu-id="ca700-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca700-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca700-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="ca700-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca700-106">Parameters</span></span>

<span data-ttu-id="ca700-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca700-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca700-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca700-108">Return value</span></span>

<span data-ttu-id="ca700-109">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ca700-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca700-110">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ca700-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca700-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ca700-111">Return code</span></span>                                                                          | <span data-ttu-id="ca700-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca700-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca700-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca700-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca700-114">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca700-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca700-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca700-115">Remarks</span></span>

<span data-ttu-id="ca700-116">Die-Methode gibt den gesamten Arbeitsspeicher frei, der den Elementen in der Auflistung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca700-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca700-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca700-117">Requirements</span></span>



| <span data-ttu-id="ca700-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca700-118">Requirement</span></span> | <span data-ttu-id="ca700-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ca700-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca700-120">Header</span><span class="sxs-lookup"><span data-stu-id="ca700-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ca700-121"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca700-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca700-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca700-122">Library</span></span><br/> | <dl> <span data-ttu-id="ca700-123"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca700-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca700-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca700-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca700-125">**Iportableabvicevaluescollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca700-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




