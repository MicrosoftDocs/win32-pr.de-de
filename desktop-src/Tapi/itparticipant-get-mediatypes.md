---
description: Die \_ Methode Get mediatypes Ruft die einem Teilnehmer zugeordneten Medientypen ab.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Itteilnehmer:: get_MediaTypes-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358206"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="dc3c6-103">Itteilnehmer:: get \_ mediatypes-Methode</span><span class="sxs-lookup"><span data-stu-id="dc3c6-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="dc3c6-104">\[**get \_ Mediatypes** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc3c6-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dc3c6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dc3c6-106">Die Methode **get \_ mediatypes** Ruft die einem Teilnehmer zugeordneten [**Medientypen**](tapimediatype--constants.md) ab.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc3c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc3c6-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="dc3c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc3c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc3c6-109">*plmediatype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc3c6-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc3c6-110">Zeiger auf Medientyp-Flags, z. b. tapimediatype \_ Video.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc3c6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc3c6-111">Return value</span></span>

<span data-ttu-id="dc3c6-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dc3c6-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dc3c6-113">Return code</span></span>                                                                                   | <span data-ttu-id="dc3c6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc3c6-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dc3c6-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dc3c6-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dc3c6-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dc3c6-118">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="dc3c6-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dc3c6-120">Der *plmediatype* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="dc3c6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc3c6-121">Requirements</span></span>



| <span data-ttu-id="dc3c6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc3c6-122">Requirement</span></span> | <span data-ttu-id="dc3c6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="dc3c6-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc3c6-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dc3c6-124">TAPI version</span></span><br/> | <span data-ttu-id="dc3c6-125">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="dc3c6-126">Header</span><span class="sxs-lookup"><span data-stu-id="dc3c6-126">Header</span></span><br/>       | <dl> <span data-ttu-id="dc3c6-127"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc3c6-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc3c6-128">Library</span></span><br/>      | <dl> <span data-ttu-id="dc3c6-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="dc3c6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dc3c6-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="dc3c6-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc3c6-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc3c6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc3c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc3c6-133">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="dc3c6-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="dc3c6-134">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="dc3c6-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




