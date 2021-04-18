---
description: Die reorderfunktionalitäten-Methode legt eine neue Reihenfolge für Formatierungsfunktionen fest.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Itformatcontrol:: reorderfunktionalitäten-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364766"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="727d3-103">Itformatcontrol:: reorderfunktionalitäten-Methode</span><span class="sxs-lookup"><span data-stu-id="727d3-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="727d3-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="727d3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="727d3-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="727d3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="727d3-106">Die **reorderfunktionalitäten** -Methode legt eine neue Reihenfolge für Formatierungsfunktionen fest.</span><span class="sxs-lookup"><span data-stu-id="727d3-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="727d3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="727d3-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="727d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="727d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727d3-109">*pdwindices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="727d3-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727d3-110">Index des umordneten Formats.</span><span class="sxs-lookup"><span data-stu-id="727d3-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="727d3-111">*pfaktivierte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="727d3-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727d3-112">Gibt an, ob das Format aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="727d3-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="727d3-113">*pfpublicize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="727d3-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727d3-114">Gibt an, ob das Format verfügbar gemacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="727d3-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="727d3-115">*dwnumindizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="727d3-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="727d3-116">Neue Indexnummer für das Format.</span><span class="sxs-lookup"><span data-stu-id="727d3-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727d3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="727d3-117">Return value</span></span>

<span data-ttu-id="727d3-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="727d3-118">This method can return one of these values.</span></span>



| <span data-ttu-id="727d3-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="727d3-119">Return code</span></span>                                                                                   | <span data-ttu-id="727d3-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="727d3-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="727d3-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="727d3-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="727d3-122">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="727d3-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="727d3-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="727d3-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="727d3-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="727d3-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="727d3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="727d3-125">Remarks</span></span>

<span data-ttu-id="727d3-126">Vor der Verwendung dieser Methode muss die [**getnumoffunktionalitäten**](itformatcontrol-getnumberofcapabilities.md) -Methode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="727d3-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="727d3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="727d3-127">Requirements</span></span>



| <span data-ttu-id="727d3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="727d3-128">Requirement</span></span> | <span data-ttu-id="727d3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="727d3-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="727d3-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="727d3-130">TAPI version</span></span><br/> | <span data-ttu-id="727d3-131">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="727d3-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="727d3-132">Header</span><span class="sxs-lookup"><span data-stu-id="727d3-132">Header</span></span><br/>       | <dl> <span data-ttu-id="727d3-133"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="727d3-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="727d3-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="727d3-134">Library</span></span><br/>      | <dl> <span data-ttu-id="727d3-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="727d3-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="727d3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="727d3-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="727d3-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="727d3-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727d3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="727d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727d3-139">**Itformatcontrol**</span><span class="sxs-lookup"><span data-stu-id="727d3-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="727d3-140">**Getnumof-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="727d3-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




