---
description: Die Methode "nettunsignedintegervalue" fügt einen neuen ulong-Wert (Type VT \_ UI4) hinzu oder überschreibt eine vorhandene.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Iportabledevicevalues:: Server Value-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369481"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="17659-103">Iportabledevicevalues:: Server Value-Methode</span><span class="sxs-lookup"><span data-stu-id="17659-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="17659-104">Die Methode " **nettunsignedintegervalue** " fügt einen neuen **ulong** -Wert (Type VT \_ UI4) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="17659-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="17659-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17659-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="17659-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17659-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17659-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17659-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="17659-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="17659-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17659-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17659-110">Ein **ulong** -Wert, der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="17659-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17659-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17659-111">Return value</span></span>

<span data-ttu-id="17659-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="17659-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17659-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="17659-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="17659-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="17659-114">Return code</span></span>                                                                          | <span data-ttu-id="17659-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17659-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="17659-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17659-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="17659-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17659-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17659-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17659-118">Remarks</span></span>

<span data-ttu-id="17659-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="17659-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="17659-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17659-120">Examples</span></span>

<span data-ttu-id="17659-121">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [**Angeben von Client Informationen**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="17659-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17659-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17659-122">Requirements</span></span>



| <span data-ttu-id="17659-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17659-123">Requirement</span></span> | <span data-ttu-id="17659-124">Wert</span><span class="sxs-lookup"><span data-stu-id="17659-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17659-125">Header</span><span class="sxs-lookup"><span data-stu-id="17659-125">Header</span></span><br/>  | <dl> <span data-ttu-id="17659-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="17659-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="17659-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17659-127">Library</span></span><br/> | <dl> <span data-ttu-id="17659-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17659-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17659-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17659-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17659-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="17659-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="17659-131">**Iportablede vicevalues:: getunsignedintegervalue**</span><span class="sxs-lookup"><span data-stu-id="17659-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="17659-132">**Angeben von Client Informationen**</span><span class="sxs-lookup"><span data-stu-id="17659-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




