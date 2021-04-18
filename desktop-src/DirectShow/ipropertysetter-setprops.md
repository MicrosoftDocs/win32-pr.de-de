---
description: Die SetProperties-Methode legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Ipropertysetter:: setrequiproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361325"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="e2f75-103">Ipropertysetter:: setrequiproper-Methode</span><span class="sxs-lookup"><span data-stu-id="e2f75-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="e2f75-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e2f75-104">\[Deprecated.</span></span> <span data-ttu-id="e2f75-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e2f75-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e2f75-106">Die- `SetProps` Methode legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.</span><span class="sxs-lookup"><span data-stu-id="e2f75-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f75-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f75-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="e2f75-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2f75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f75-109">*pTARGET* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f75-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f75-110">Zeiger auf das Zielobjekt, für das die Eigenschaften festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e2f75-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="e2f75-111">*rtnow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2f75-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f75-112">Der Zeitpunkt, zu dem die Eigenschaften festgelegt werden sollen, in 100-Nanosecond-Einheiten oder – 1, um statische Eigenschaften festzulegen (solche, die sich im Laufe der Zeit nicht unterscheiden).</span><span class="sxs-lookup"><span data-stu-id="e2f75-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f75-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2f75-113">Return value</span></span>

<span data-ttu-id="e2f75-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2f75-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e2f75-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2f75-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f75-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2f75-116">Remarks</span></span>

<span data-ttu-id="e2f75-117">Diese Methode wird von des aufgerufen, um die Eigenschaften eines Übergangs oder Effekts festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e2f75-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="e2f75-118">Eine Anwendung ruft normalerweise diese Methode nicht auf.</span><span class="sxs-lookup"><span data-stu-id="e2f75-118">An application will not normally call this method.</span></span>

<span data-ttu-id="e2f75-119">Das von *pTARGET* angegebene Objekt muss die **IDispatch** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="e2f75-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="e2f75-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e2f75-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2f75-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e2f75-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2f75-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2f75-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2f75-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2f75-123">Requirements</span></span>



| <span data-ttu-id="e2f75-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2f75-124">Requirement</span></span> | <span data-ttu-id="e2f75-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e2f75-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f75-126">Header</span><span class="sxs-lookup"><span data-stu-id="e2f75-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f75-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e2f75-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e2f75-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2f75-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2f75-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e2f75-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f75-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f75-131">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2f75-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="e2f75-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e2f75-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




