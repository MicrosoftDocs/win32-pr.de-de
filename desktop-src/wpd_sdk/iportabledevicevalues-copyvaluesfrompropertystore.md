---
description: Die copyvaluesfrompropertystore-Methode kopiert den Inhalt eines IPropertyStore in die Auflistung.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Iportabledevicevalues:: copyvaluesfrompropertystore-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355997"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="a6d80-103">Iportabledevicevalues:: copyvaluesfrompropertystore-Methode</span><span class="sxs-lookup"><span data-stu-id="a6d80-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="a6d80-104">Die **copyvaluesfrompropertystore** -Methode kopiert den Inhalt eines **IPropertyStore** in die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a6d80-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6d80-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="a6d80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6d80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6d80-107">*pstore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6d80-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6d80-108">Zeiger auf einen **IPropertyStore** , der in die Auflistung kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6d80-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6d80-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6d80-109">Return value</span></span>

<span data-ttu-id="a6d80-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a6d80-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a6d80-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a6d80-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a6d80-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a6d80-112">Return code</span></span>                                                                          | <span data-ttu-id="a6d80-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6d80-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a6d80-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6d80-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a6d80-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6d80-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6d80-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6d80-116">Remarks</span></span>

<span data-ttu-id="a6d80-117">Diese Methode konvertiert automatisch alle **VT \_ BSTR** -Werte in **VT \_ LPWSTR** -Werte.</span><span class="sxs-lookup"><span data-stu-id="a6d80-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="a6d80-118">Viele externe Anwendungen oder Komponenten, die mit Ihrer Anwendung kommunizieren (z. b. einige Shellanwendungen), verwenden die **IPropertyStore** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a6d80-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="a6d80-119">Diese Methode bietet eine schnelle und einfache Möglichkeit zum Austauschen von Daten mit diesen Programmen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="a6d80-120">Diese Methode wird in Windows Vista und höheren Versionen von Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6d80-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d80-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6d80-121">Requirements</span></span>



| <span data-ttu-id="a6d80-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6d80-122">Requirement</span></span> | <span data-ttu-id="a6d80-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a6d80-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d80-124">Header</span><span class="sxs-lookup"><span data-stu-id="a6d80-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a6d80-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d80-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6d80-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6d80-126">Library</span></span><br/> | <dl> <span data-ttu-id="a6d80-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6d80-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d80-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d80-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d80-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a6d80-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a6d80-130">**Iportablede vicevalues:: copyvaluestopropertystore**</span><span class="sxs-lookup"><span data-stu-id="a6d80-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




