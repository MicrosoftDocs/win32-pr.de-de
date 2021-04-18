---
description: Die setsignedlargeintegervalue-Methode fügt einen neuen Longlong-Wert (Typ VT \_ I8) hinzu oder überschreibt eine vorhandene.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Iportabledevicevalues:: setsignedlargeingetegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358346"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="65310-103">Iportabledevicevalues:: setsignedlargeingetegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="65310-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="65310-104">Die **setsignedlargeintegervalue** -Methode fügt einen neuen **Longlong** -Wert (Typ VT \_ I8) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="65310-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="65310-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65310-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="65310-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65310-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65310-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65310-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="65310-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="65310-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65310-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65310-110">Ein **Longlong** -Wert, der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="65310-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65310-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65310-111">Return value</span></span>

<span data-ttu-id="65310-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="65310-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="65310-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="65310-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="65310-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="65310-114">Return code</span></span>                                                                          | <span data-ttu-id="65310-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65310-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="65310-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65310-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="65310-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65310-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65310-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65310-118">Remarks</span></span>

<span data-ttu-id="65310-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="65310-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="65310-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65310-120">Requirements</span></span>



| <span data-ttu-id="65310-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65310-121">Requirement</span></span> | <span data-ttu-id="65310-122">Wert</span><span class="sxs-lookup"><span data-stu-id="65310-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65310-123">Header</span><span class="sxs-lookup"><span data-stu-id="65310-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65310-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="65310-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="65310-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65310-125">Library</span></span><br/> | <dl> <span data-ttu-id="65310-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65310-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65310-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65310-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65310-128">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="65310-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="65310-129">**Iportablede vicevalues:: getsignedlargeingetegervalue**</span><span class="sxs-lookup"><span data-stu-id="65310-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




