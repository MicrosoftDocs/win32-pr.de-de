---
description: Die getcurrentformat-Methode ruft das Medienformat des aktuellen Streams ab.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Itformatcontrol:: getcurrentformat-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355941"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="cc545-103">Itformatcontrol:: getcurrentformat-Methode</span><span class="sxs-lookup"><span data-stu-id="cc545-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="cc545-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc545-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cc545-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="cc545-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cc545-106">Die **getcurrentformat** -Methode ruft das Medienformat des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="cc545-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc545-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc545-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="cc545-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc545-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc545-109">*PpMediaType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cc545-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc545-110">Zeiger auf einen **am \_ \_ Medientyp** Deskriptor des Terminal Formats.</span><span class="sxs-lookup"><span data-stu-id="cc545-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="cc545-111">Weitere Informationen zu dem **\_ \_ Medientyp** finden Sie in der DirectX-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="cc545-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc545-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc545-112">Return value</span></span>

<span data-ttu-id="cc545-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc545-113">This method can return one of these values.</span></span>



| <span data-ttu-id="cc545-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cc545-114">Return code</span></span>                                                                                   | <span data-ttu-id="cc545-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc545-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cc545-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc545-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cc545-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="cc545-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cc545-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cc545-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cc545-119">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cc545-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc545-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc545-120">Requirements</span></span>



| <span data-ttu-id="cc545-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc545-121">Requirement</span></span> | <span data-ttu-id="cc545-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cc545-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc545-123">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="cc545-123">TAPI version</span></span><br/> | <span data-ttu-id="cc545-124">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="cc545-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="cc545-125">Header</span><span class="sxs-lookup"><span data-stu-id="cc545-125">Header</span></span><br/>       | <dl> <span data-ttu-id="cc545-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc545-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc545-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc545-127">Library</span></span><br/>      | <dl> <span data-ttu-id="cc545-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc545-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="cc545-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cc545-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="cc545-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc545-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc545-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc545-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc545-132">**Itformatcontrol**</span><span class="sxs-lookup"><span data-stu-id="cc545-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




