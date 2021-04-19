---
description: Die \_ Methode Get participanttyetdinfo erhält eine BSTR-Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Itteilnehmer:: get_ParticipantTypedInfo-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356359"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="7ca34-103">Itteilnehmer:: get \_ participanttypdinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="7ca34-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="7ca34-104">\[**get \_ "Participanttypeer** " ist für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ca34-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7ca34-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7ca34-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7ca34-106">Die Methode **get \_ participanttyetdinfo** erhält eine **BSTR** -Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress.</span><span class="sxs-lookup"><span data-stu-id="7ca34-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca34-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ca34-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ca34-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ca34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca34-109">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ca34-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca34-110">[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Deskriptor des Typs der benötigten Informationen.</span><span class="sxs-lookup"><span data-stu-id="7ca34-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="7ca34-111">*ppinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ca34-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca34-112">Ein Zeiger auf die **BSTR** -Darstellung der benötigten Informationen.</span><span class="sxs-lookup"><span data-stu-id="7ca34-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca34-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ca34-113">Return value</span></span>

<span data-ttu-id="7ca34-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7ca34-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7ca34-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7ca34-115">Return code</span></span>                                                                                    | <span data-ttu-id="7ca34-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ca34-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7ca34-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="7ca34-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7ca34-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7ca34-119"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="7ca34-120">Fehler beim Speichern von Informationen in *ppinfo* .</span><span class="sxs-lookup"><span data-stu-id="7ca34-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="7ca34-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="7ca34-122">Der *InfoType* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7ca34-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="7ca34-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="7ca34-124">Der *ppinfo* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="7ca34-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="7ca34-125"><dt>**TAPI \_ E \_ noitem**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="7ca34-126">TAPI weist keine Informationen zum angegebenen Typ auf.</span><span class="sxs-lookup"><span data-stu-id="7ca34-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="7ca34-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="7ca34-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7ca34-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ca34-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ca34-129">Remarks</span></span>

<span data-ttu-id="7ca34-130">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppinfo* -Parameter zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7ca34-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca34-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ca34-131">Requirements</span></span>



| <span data-ttu-id="7ca34-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ca34-132">Requirement</span></span> | <span data-ttu-id="7ca34-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7ca34-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca34-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="7ca34-134">TAPI version</span></span><br/> | <span data-ttu-id="7ca34-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7ca34-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="7ca34-136">Header</span><span class="sxs-lookup"><span data-stu-id="7ca34-136">Header</span></span><br/>       | <dl> <span data-ttu-id="7ca34-137"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ca34-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ca34-138">Library</span></span><br/>      | <dl> <span data-ttu-id="7ca34-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7ca34-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7ca34-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="7ca34-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ca34-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca34-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ca34-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca34-143">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="7ca34-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="7ca34-144">**\_typisierte Teilnehmer \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="7ca34-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="7ca34-145">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="7ca34-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

