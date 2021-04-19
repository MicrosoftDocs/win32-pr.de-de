---
description: Die GetStringValue-Methode ruft einen Zeichen folgen Wert (Typ VT \_ LPWSTR) ab, der von einem Schlüssel angegeben wird.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Iportabledevicevalues:: GetStringValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361645"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="14f54-103">Iportabledevicevalues:: GetStringValue-Methode</span><span class="sxs-lookup"><span data-stu-id="14f54-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="14f54-104">Die **GetStringValue** -Methode ruft einen Zeichen folgen Wert (Typ VT \_ LPWSTR) ab, der von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="14f54-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14f54-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="14f54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14f54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f54-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14f54-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f54-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="14f54-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="14f54-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14f54-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14f54-110">Zeiger auf den abgerufenen **LPWSTR** -Wert.</span><span class="sxs-lookup"><span data-stu-id="14f54-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="14f54-111">Der Aufrufer ist verantwortlich für den Aufruf von **CoTaskMemFree** , um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="14f54-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f54-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14f54-112">Return value</span></span>

<span data-ttu-id="14f54-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="14f54-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="14f54-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14f54-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="14f54-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="14f54-115">Return code</span></span>                                                                                                            | <span data-ttu-id="14f54-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14f54-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="14f54-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14f54-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="14f54-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14f54-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="14f54-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="14f54-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="14f54-120">Die von *Key* angegebene Eigenschaft ist kein **LPWSTR** -Typ.</span><span class="sxs-lookup"><span data-stu-id="14f54-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="14f54-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="14f54-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="14f54-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="14f54-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="14f54-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14f54-123">Examples</span></span>

<span data-ttu-id="14f54-124">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="14f54-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14f54-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14f54-125">Requirements</span></span>



| <span data-ttu-id="14f54-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14f54-126">Requirement</span></span> | <span data-ttu-id="14f54-127">Wert</span><span class="sxs-lookup"><span data-stu-id="14f54-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f54-128">Header</span><span class="sxs-lookup"><span data-stu-id="14f54-128">Header</span></span><br/>  | <dl> <span data-ttu-id="14f54-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="14f54-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="14f54-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14f54-130">Library</span></span><br/> | <dl> <span data-ttu-id="14f54-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14f54-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f54-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14f54-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f54-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="14f54-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="14f54-134">**Iportablede vicevalues:: GetAt**</span><span class="sxs-lookup"><span data-stu-id="14f54-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="14f54-135">**Iportabledebug:: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="14f54-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="14f54-136">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="14f54-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="14f54-137">Abrufen unterstützter Dienst Formate</span><span class="sxs-lookup"><span data-stu-id="14f54-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="14f54-138">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="14f54-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




