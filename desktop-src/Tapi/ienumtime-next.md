---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'Ienumtime:: Next-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce3d88bc88e808c35ec64f827fd5925ddfe57f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371378"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="1e1f0-103">Ienumtime:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="1e1f0-103">IEnumTime::Next method</span></span>

<span data-ttu-id="1e1f0-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1e1f0-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1e1f0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1e1f0-106">Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e1f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e1f0-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="1e1f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e1f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e1f0-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e1f0-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1f0-110">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f0-111">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e1f0-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1f0-112">Zeiger auf die [**ittime**](ittime.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1e1f0-113">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1e1f0-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e1f0-114">Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="1e1f0-115">Kann **null** sein, wenn *celt* 1 ist.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e1f0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e1f0-116">Return value</span></span>

<span data-ttu-id="1e1f0-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-117">This method can return one of these values.</span></span>



| <span data-ttu-id="1e1f0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1e1f0-118">Value</span></span>                                                                                     | <span data-ttu-id="1e1f0-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e1f0-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="1e1f0-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1e1f0-121">Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="1e1f0-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="1e1f0-123">Die Anzahl der verbleibenden Elemente war kleiner als *celt*.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="1e1f0-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1e1f0-125">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="1e1f0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e1f0-126">Remarks</span></span>

<span data-ttu-id="1e1f0-127">TAPI Ruft die **adressf** -Methode für die [**ittime**](ittime.md) -Schnittstelle auf, die von **ienumtime:: Next** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1e1f0-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="1e1f0-128">Die Anwendung muss Release auf der **ittime** -Schnittstelle aufzurufen, um die damit verbundenen Ressourcen frei **zugeben** .</span><span class="sxs-lookup"><span data-stu-id="1e1f0-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e1f0-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e1f0-129">Requirements</span></span>



| <span data-ttu-id="1e1f0-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e1f0-130">Requirement</span></span> | <span data-ttu-id="1e1f0-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1e1f0-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e1f0-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1e1f0-132">TAPI version</span></span><br/> | <span data-ttu-id="1e1f0-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1e1f0-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1e1f0-134">Header</span><span class="sxs-lookup"><span data-stu-id="1e1f0-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1e1f0-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e1f0-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e1f0-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1e1f0-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1e1f0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1e1f0-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1e1f0-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e1f0-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e1f0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e1f0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e1f0-141">**Ienumtime**</span><span class="sxs-lookup"><span data-stu-id="1e1f0-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




