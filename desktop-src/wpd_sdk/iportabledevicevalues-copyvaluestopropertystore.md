---
description: Die copyvaluestopropertystore-Methode kopiert alle Werte aus einer Auflistung in eine IPropertyStore-Schnittstelle.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Iportabledevicevalues:: copyvaluestopropertystore-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373893"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="0e710-103">Iportabledevicevalues:: copyvaluestopropertystore-Methode</span><span class="sxs-lookup"><span data-stu-id="0e710-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="0e710-104">Die **copyvaluestopropertystore** -Methode kopiert alle Werte aus einer Auflistung in eine **IPropertyStore** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0e710-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e710-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e710-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="0e710-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e710-107">*pstore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e710-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e710-108">Zeiger auf ein Speicher Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e710-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e710-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e710-109">Return value</span></span>

<span data-ttu-id="0e710-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e710-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0e710-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e710-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0e710-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0e710-112">Return code</span></span>                                                                          | <span data-ttu-id="0e710-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e710-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0e710-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e710-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0e710-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e710-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e710-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e710-116">Remarks</span></span>

<span data-ttu-id="0e710-117">Diese Methode konvertiert keine Werte von VT \_ LPWSTR in VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="0e710-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="0e710-118">Viele externe Anwendungen oder Komponenten, die mit Ihrer Anwendung kommunizieren (z. b. einige Shellanwendungen), verwenden die **IPropertyStore** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0e710-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="0e710-119">Diese Methode bietet eine schnelle und einfache Möglichkeit zum Austauschen von Daten mit diesen Programmen.</span><span class="sxs-lookup"><span data-stu-id="0e710-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="0e710-120">Diese Methode wird in Windows Vista und höheren Versionen von Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e710-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e710-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e710-121">Requirements</span></span>



| <span data-ttu-id="0e710-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e710-122">Requirement</span></span> | <span data-ttu-id="0e710-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0e710-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e710-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e710-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e710-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e710-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e710-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e710-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e710-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e710-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e710-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e710-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e710-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0e710-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0e710-130">**Iportablede vicevalues:: copyvaluesfrompropertystore**</span><span class="sxs-lookup"><span data-stu-id="0e710-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




