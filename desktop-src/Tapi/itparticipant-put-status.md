---
description: Mit der Put \_ Status-Methode wird der Status eines Teilnehmers festgelegt.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: Itteilnehmer::p ut_Status-Methode (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368526"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="02ff4-103">Itteilnehmer::p UT- \_ Status Methode</span><span class="sxs-lookup"><span data-stu-id="02ff4-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="02ff4-104">\[**Put \_ Der Status** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="02ff4-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02ff4-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="02ff4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="02ff4-106">Mit der **Put \_ Status** -Methode wird der Status eines Teilnehmers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02ff4-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ff4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="02ff4-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="02ff4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="02ff4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ff4-109">*pitstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ff4-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ff4-110">Zeiger auf die [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="02ff4-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="02ff4-111">*fenckbar* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ff4-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ff4-112">Variant \_ true, wenn der Teilnehmer im Stream aktiviert ist, Variant \_ false, wenn er deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="02ff4-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ff4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02ff4-113">Return value</span></span>

<span data-ttu-id="02ff4-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="02ff4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="02ff4-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02ff4-115">Return code</span></span>                                                                                   | <span data-ttu-id="02ff4-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02ff4-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02ff4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="02ff4-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="02ff4-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="02ff4-119"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="02ff4-120">Die Methode ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="02ff4-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="02ff4-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="02ff4-122">Der *pitstream* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="02ff4-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="02ff4-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="02ff4-124">Der *pitstream* -Parameter verweist nicht auf eine gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="02ff4-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="02ff4-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="02ff4-126">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="02ff4-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="02ff4-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02ff4-127">Remarks</span></span>

<span data-ttu-id="02ff4-128">Durch Aktivieren oder Deaktivieren des Status eines Teilnehmers für einen Stream kann eine Anwendung einen bestimmten Teilnehmer im wesentlichen stumm schalten.</span><span class="sxs-lookup"><span data-stu-id="02ff4-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ff4-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02ff4-129">Requirements</span></span>



| <span data-ttu-id="02ff4-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02ff4-130">Requirement</span></span> | <span data-ttu-id="02ff4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="02ff4-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02ff4-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="02ff4-132">TAPI version</span></span><br/> | <span data-ttu-id="02ff4-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="02ff4-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="02ff4-134">Header</span><span class="sxs-lookup"><span data-stu-id="02ff4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="02ff4-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02ff4-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02ff4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="02ff4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="02ff4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="02ff4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="02ff4-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02ff4-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ff4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02ff4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ff4-141">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="02ff4-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="02ff4-142">**Itstream**</span><span class="sxs-lookup"><span data-stu-id="02ff4-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="02ff4-143">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="02ff4-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

