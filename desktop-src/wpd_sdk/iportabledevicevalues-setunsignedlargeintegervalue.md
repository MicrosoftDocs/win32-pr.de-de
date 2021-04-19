---
description: Mit der Methode "" von "" wird ein neuer ULONGLONG-Wert (Typ "VT UI8" \_ ) hinzugefügt oder ein vorhandener überschrieben.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: Iportabledevicevalues::-Methode (portabledevicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358031"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="22150-103">Iportabledevicevalues:: Server-/signedlargeintegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="22150-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="22150-104">Mit **der Methode** "" von "" wird ein neuer **ULONGLONG** -Wert (Typ "VT UI8" \_ ) hinzugefügt oder ein vorhandener überschrieben.</span><span class="sxs-lookup"><span data-stu-id="22150-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="22150-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22150-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="22150-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22150-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22150-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22150-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22150-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="22150-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="22150-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22150-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22150-110">Ein **ULONGLONG** , der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="22150-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22150-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22150-111">Return value</span></span>

<span data-ttu-id="22150-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="22150-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22150-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22150-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22150-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22150-114">Return code</span></span>                                                                          | <span data-ttu-id="22150-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22150-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22150-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22150-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22150-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22150-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="22150-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22150-118">Requirements</span></span>



| <span data-ttu-id="22150-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22150-119">Requirement</span></span> | <span data-ttu-id="22150-120">Wert</span><span class="sxs-lookup"><span data-stu-id="22150-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22150-121">Header</span><span class="sxs-lookup"><span data-stu-id="22150-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22150-122"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="22150-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="22150-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22150-123">Library</span></span><br/> | <dl> <span data-ttu-id="22150-124"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22150-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22150-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22150-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22150-126">Hinzufügen einer Ressource zu einem Objekt</span><span class="sxs-lookup"><span data-stu-id="22150-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="22150-127">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="22150-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="22150-128">**Iportablede vicevalues:: getunsignedlargeingetegervalue**</span><span class="sxs-lookup"><span data-stu-id="22150-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




