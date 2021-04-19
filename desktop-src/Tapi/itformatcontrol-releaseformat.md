---
description: Die releaseformat-Methode gibt die Struktur frei, die dem Format zugeordnet ist.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'Itformatcontrol:: releaseformat-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368596"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="26a01-103">Itformatcontrol:: releaseformat-Methode</span><span class="sxs-lookup"><span data-stu-id="26a01-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="26a01-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26a01-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26a01-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="26a01-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="26a01-106">Die **releaseformat** -Methode gibt die Struktur frei, die dem Format zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26a01-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26a01-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="26a01-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26a01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a01-109">*pmediatype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26a01-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26a01-110">Zeiger auf einen **am \_ \_ Medientyp** Deskriptor des Terminal Formats.</span><span class="sxs-lookup"><span data-stu-id="26a01-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="26a01-111">Weitere Informationen zu dem **\_ \_ Medientyp** finden Sie in der DirectX-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="26a01-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a01-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26a01-112">Return value</span></span>

<span data-ttu-id="26a01-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="26a01-113">This method can return one of these values.</span></span>



| <span data-ttu-id="26a01-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="26a01-114">Return code</span></span>                                                                                   | <span data-ttu-id="26a01-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26a01-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="26a01-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="26a01-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="26a01-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="26a01-118"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="26a01-119">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="26a01-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26a01-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26a01-120">Requirements</span></span>



| <span data-ttu-id="26a01-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26a01-121">Requirement</span></span> | <span data-ttu-id="26a01-122">Wert</span><span class="sxs-lookup"><span data-stu-id="26a01-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26a01-123">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="26a01-123">TAPI version</span></span><br/> | <span data-ttu-id="26a01-124">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="26a01-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="26a01-125">Header</span><span class="sxs-lookup"><span data-stu-id="26a01-125">Header</span></span><br/>       | <dl> <span data-ttu-id="26a01-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26a01-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26a01-127">Library</span></span><br/>      | <dl> <span data-ttu-id="26a01-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="26a01-129">DLL</span><span class="sxs-lookup"><span data-stu-id="26a01-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="26a01-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26a01-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a01-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26a01-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a01-132">**Itformatcontrol**</span><span class="sxs-lookup"><span data-stu-id="26a01-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




