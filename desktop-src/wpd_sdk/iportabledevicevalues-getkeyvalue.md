---
description: Die getkeyvalue-Methode ruft einen PropertyKey-Wert ab, der von einem Schlüssel angegeben wird.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'Iportabledevicevalues:: getkeyvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358053"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="c4e37-103">Iportabledevicevalues:: getkeyvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="c4e37-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="c4e37-104">Die **getkeyvalue** -Methode ruft einen **PropertyKey** -Wert ab, der von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4e37-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4e37-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="c4e37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e37-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4e37-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e37-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="c4e37-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c4e37-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4e37-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e37-110">Zeiger auf den abgerufenen **PropertyKey** -Wert.</span><span class="sxs-lookup"><span data-stu-id="c4e37-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e37-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4e37-111">Return value</span></span>

<span data-ttu-id="c4e37-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c4e37-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c4e37-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c4e37-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c4e37-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4e37-114">Return code</span></span>                                                                                                            | <span data-ttu-id="c4e37-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4e37-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4e37-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4e37-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c4e37-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4e37-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c4e37-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="c4e37-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c4e37-119">Die von *Key* angegebene Eigenschaft ist kein **PropertyKey** -Typ.</span><span class="sxs-lookup"><span data-stu-id="c4e37-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="c4e37-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="c4e37-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c4e37-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c4e37-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="c4e37-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4e37-122">Requirements</span></span>



| <span data-ttu-id="c4e37-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4e37-123">Requirement</span></span> | <span data-ttu-id="c4e37-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c4e37-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e37-125">Header</span><span class="sxs-lookup"><span data-stu-id="c4e37-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c4e37-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e37-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4e37-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4e37-127">Library</span></span><br/> | <dl> <span data-ttu-id="c4e37-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4e37-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e37-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4e37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e37-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4e37-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c4e37-131">**Iportabledebug:: SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="c4e37-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




