---
description: Die setfloatvalue-Methode fügt einen neuen float-Wert (Type VT \_ R4) hinzu oder überschreibt eine vorhandene.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'Iportabledevicevalues:: setfloatvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358349"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="a5529-103">Iportabledevicevalues:: setfloatvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="a5529-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="a5529-104">Die **setfloatvalue** -Methode fügt einen neuen **float** -Wert (Type VT \_ R4) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="a5529-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5529-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5529-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="a5529-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5529-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5529-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5529-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5529-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="a5529-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5529-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5529-110">Ein **float** -Wert, der den neuen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="a5529-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5529-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5529-111">Return value</span></span>

<span data-ttu-id="a5529-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a5529-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a5529-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a5529-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a5529-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a5529-114">Return code</span></span>                                                                          | <span data-ttu-id="a5529-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5529-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a5529-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5529-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a5529-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5529-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5529-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5529-118">Remarks</span></span>

<span data-ttu-id="a5529-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a5529-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5529-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5529-120">Requirements</span></span>



| <span data-ttu-id="a5529-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5529-121">Requirement</span></span> | <span data-ttu-id="a5529-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a5529-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5529-123">Header</span><span class="sxs-lookup"><span data-stu-id="a5529-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a5529-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5529-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5529-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5529-125">Library</span></span><br/> | <dl> <span data-ttu-id="a5529-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5529-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5529-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5529-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5529-128">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a5529-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a5529-129">**Iportablede vicevalues:: getFloatValue**</span><span class="sxs-lookup"><span data-stu-id="a5529-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




