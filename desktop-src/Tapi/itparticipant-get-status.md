---
description: Die \_ Methode Get Status gibt einen Variant-booleschen Wert zurück, der den \_ Teilnehmer Status angibt
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Itteilnehmer:: get_Status-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357675"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="4f432-103">Itparticipants:: get \_ Status-Methode</span><span class="sxs-lookup"><span data-stu-id="4f432-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="4f432-104">\[**get \_ Der Status** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f432-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4f432-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4f432-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4f432-106">Die Methode **get \_ Status** gibt einen Variant-booleschen Wert zurück, der den \_ Teilnehmer Status angibt</span><span class="sxs-lookup"><span data-stu-id="4f432-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f432-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f432-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4f432-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f432-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f432-109">*pitstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f432-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f432-110">Zeiger auf die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4f432-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4f432-111">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f432-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f432-112">Variant \_ true, wenn der Teilnehmer im Stream aktiviert ist, Variant \_ false, wenn er deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4f432-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f432-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f432-113">Return value</span></span>

<span data-ttu-id="4f432-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4f432-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4f432-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4f432-115">Return code</span></span>                                                                                   | <span data-ttu-id="4f432-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f432-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f432-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4f432-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4f432-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="4f432-119"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4f432-120">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f432-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="4f432-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4f432-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4f432-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="4f432-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4f432-124">Der *pitstream* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4f432-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="4f432-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4f432-126">Der *pitstream* -Parameter verweist nicht auf eine gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4f432-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f432-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f432-127">Remarks</span></span>

<span data-ttu-id="4f432-128">Durch Aktivieren oder Deaktivieren des Status eines Teilnehmers für einen Stream kann eine Anwendung einen bestimmten Teilnehmer im wesentlichen stumm schalten.</span><span class="sxs-lookup"><span data-stu-id="4f432-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f432-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f432-129">Requirements</span></span>



| <span data-ttu-id="4f432-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f432-130">Requirement</span></span> | <span data-ttu-id="4f432-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4f432-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f432-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4f432-132">TAPI version</span></span><br/> | <span data-ttu-id="4f432-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4f432-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="4f432-134">Header</span><span class="sxs-lookup"><span data-stu-id="4f432-134">Header</span></span><br/>       | <dl> <span data-ttu-id="4f432-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f432-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f432-136">Library</span></span><br/>      | <dl> <span data-ttu-id="4f432-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="4f432-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4f432-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="4f432-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f432-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f432-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f432-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f432-141">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="4f432-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="4f432-142">**Itstream**</span><span class="sxs-lookup"><span data-stu-id="4f432-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="4f432-143">**Put- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="4f432-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

