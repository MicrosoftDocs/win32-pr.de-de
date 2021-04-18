---
description: Die removeValue-Methode entfernt ein Element aus der Auflistung.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Iportabledevicevalues:: removeValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372277"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="25f0f-103">Iportabledevicevalues:: removeValue-Methode</span><span class="sxs-lookup"><span data-stu-id="25f0f-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="25f0f-104">Die **removeValue** -Methode entfernt ein Element aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="25f0f-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25f0f-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="25f0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f0f-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25f0f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f0f-108">Ein **refpropertykey** , der das zu entfernenden Element angibt.</span><span class="sxs-lookup"><span data-stu-id="25f0f-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f0f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25f0f-109">Return value</span></span>

<span data-ttu-id="25f0f-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="25f0f-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="25f0f-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="25f0f-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="25f0f-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="25f0f-112">Return code</span></span>                                                                          | <span data-ttu-id="25f0f-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25f0f-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="25f0f-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25f0f-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="25f0f-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25f0f-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25f0f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f0f-116">Requirements</span></span>



| <span data-ttu-id="25f0f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25f0f-117">Requirement</span></span> | <span data-ttu-id="25f0f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="25f0f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f0f-119">Header</span><span class="sxs-lookup"><span data-stu-id="25f0f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="25f0f-120"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f0f-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="25f0f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25f0f-121">Library</span></span><br/> | <dl> <span data-ttu-id="25f0f-122"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25f0f-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f0f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f0f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f0f-124">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="25f0f-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="25f0f-125">**Iportablede vicevalues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="25f0f-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="25f0f-126">**Iportabledebug:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="25f0f-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




