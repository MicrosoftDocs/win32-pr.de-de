---
description: Die cloneproperties-Methode klont eine Reihe von Eigenschaften aus diesem Eigenschaften Setter und fügt Sie einem neuen Eigenschaften Setter hinzu.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Ipropertysetter:: cloneproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352876"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="97ddc-103">Ipropertysetter:: clonerequismethode</span><span class="sxs-lookup"><span data-stu-id="97ddc-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="97ddc-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="97ddc-104">\[Deprecated.</span></span> <span data-ttu-id="97ddc-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="97ddc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="97ddc-106">`CloneProps`Mit der-Methode wird ein Satz von Eigenschaften aus diesem Eigenschaften Setter geklont und einem neuen Eigenschaften Setter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97ddc-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ddc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97ddc-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="97ddc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97ddc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ddc-109">*ppsetter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="97ddc-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97ddc-110">Empfängt einen Zeiger auf die **ipropertysetter** -Schnittstelle des neuen Eigenschaften Setters.</span><span class="sxs-lookup"><span data-stu-id="97ddc-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="97ddc-111">*rtstart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97ddc-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ddc-112">Die Startzeit des zu klonenden Wertebereichs in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="97ddc-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="97ddc-113">*rtstopps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97ddc-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ddc-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="97ddc-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ddc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97ddc-115">Return value</span></span>

<span data-ttu-id="97ddc-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="97ddc-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="97ddc-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97ddc-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97ddc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97ddc-118">Remarks</span></span>

<span data-ttu-id="97ddc-119">Nur die Werte, die nach der angegebenen Startzeit liegen, werden geklont.</span><span class="sxs-lookup"><span data-stu-id="97ddc-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="97ddc-120">Die Uhrzeiten für die geklonten Werte werden dann in Relation zur Startzeit angepasst.</span><span class="sxs-lookup"><span data-stu-id="97ddc-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="97ddc-121">Wenn *rtstart* beispielsweise 20 Millionen (2 Sekunden) ist, wird ein Wert zur Zeit 30 Millionen (3 Sekunden) mit der Zeit 10 Millionen (1 Sekunde) geklont.</span><span class="sxs-lookup"><span data-stu-id="97ddc-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="97ddc-122">Zum Schluss erhält jede geklonte Eigenschaft einen Anfangswert, der dem Wert der ursprünglichen Eigenschaft zur Startzeit entspricht (bei Bedarf korrekt interpoliert).</span><span class="sxs-lookup"><span data-stu-id="97ddc-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="97ddc-123">Tatsächlich werden die Eigenschaften Daten zur angegebenen Startzeit aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="97ddc-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="97ddc-124">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene [**ipropertysetter**](ipropertysetter.md) -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="97ddc-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="97ddc-125">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="97ddc-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="97ddc-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="97ddc-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="97ddc-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="97ddc-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="97ddc-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97ddc-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97ddc-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97ddc-129">Requirements</span></span>



| <span data-ttu-id="97ddc-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97ddc-130">Requirement</span></span> | <span data-ttu-id="97ddc-131">Wert</span><span class="sxs-lookup"><span data-stu-id="97ddc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97ddc-132">Header</span><span class="sxs-lookup"><span data-stu-id="97ddc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="97ddc-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="97ddc-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="97ddc-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97ddc-134">Library</span></span><br/> | <dl> <span data-ttu-id="97ddc-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="97ddc-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ddc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97ddc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ddc-137">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="97ddc-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="97ddc-138">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="97ddc-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




