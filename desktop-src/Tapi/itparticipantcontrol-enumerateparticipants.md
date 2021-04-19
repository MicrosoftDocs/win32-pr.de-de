---
description: Mit der enumerateparticipants-Methode werden die der aktuellen Konferenz zugeordneten Teilnehmer aufgelistet.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Itparticipantcontrol:: enumerateparticipants-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359218"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="44585-103">Itparticipantcontrol:: enumerateparticipants-Methode</span><span class="sxs-lookup"><span data-stu-id="44585-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="44585-104">\[**Enumerateparticipants** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44585-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="44585-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="44585-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="44585-106">Mit der **enumerateparticipants** -Methode werden die der aktuellen Konferenz zugeordneten Teilnehmer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="44585-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="44585-107">Diese Methode wird für C-und C++-Anwendungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="44585-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="44585-108">Automatisierungs Client Anwendungen, wie z. b. die in Visual Basic geschriebenen, müssen die Methode [**get \_ participants**](itparticipantcontrol-get-participants.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="44585-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="44585-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="44585-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="44585-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="44585-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44585-111">*ppumschlag-Teilnehmer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="44585-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44585-112">Zeiger auf die [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="44585-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44585-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44585-113">Return value</span></span>

<span data-ttu-id="44585-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="44585-114">This method can return one of these values.</span></span>



| <span data-ttu-id="44585-115">Wert</span><span class="sxs-lookup"><span data-stu-id="44585-115">Value</span></span>                                                                                         | <span data-ttu-id="44585-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44585-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="44585-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="44585-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="44585-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="44585-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="44585-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="44585-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="44585-120">Der Parameter " *ppenumparticipants* " ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="44585-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="44585-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="44585-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="44585-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="44585-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="44585-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44585-123">Remarks</span></span>

<span data-ttu-id="44585-124">TAPI Ruft die **adressf** -Methode für die [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle auf, die von **itparticipantcontrol:: enumerateparticipants** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44585-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="44585-125">Die Anwendung muss Release auf der **ienumparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei **zugeben** .</span><span class="sxs-lookup"><span data-stu-id="44585-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="44585-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44585-126">Requirements</span></span>



| <span data-ttu-id="44585-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44585-127">Requirement</span></span> | <span data-ttu-id="44585-128">Wert</span><span class="sxs-lookup"><span data-stu-id="44585-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44585-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="44585-129">TAPI version</span></span><br/> | <span data-ttu-id="44585-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="44585-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="44585-131">Header</span><span class="sxs-lookup"><span data-stu-id="44585-131">Header</span></span><br/>       | <dl> <span data-ttu-id="44585-132"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="44585-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="44585-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44585-133">Library</span></span><br/>      | <dl> <span data-ttu-id="44585-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44585-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="44585-135">DLL</span><span class="sxs-lookup"><span data-stu-id="44585-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="44585-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44585-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="44585-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44585-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44585-138">**Itparticipantcontrol**</span><span class="sxs-lookup"><span data-stu-id="44585-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="44585-139">**\_Teilnehmer erhalten**</span><span class="sxs-lookup"><span data-stu-id="44585-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="44585-140">**Ienumteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="44585-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="44585-141">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="44585-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




