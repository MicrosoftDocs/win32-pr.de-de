---
description: Mit der switchterminalto substream-Methode wird ein Terminal auf den Teilnehmer teilstream festgelegt.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Itparticipantsubstreamcontrol:: switchterminalto substream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374029"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="8754e-103">Itparticipantsubstreamcontrol:: switchterminalto substream-Methode</span><span class="sxs-lookup"><span data-stu-id="8754e-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="8754e-104">\[**Switchterminalto substream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8754e-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8754e-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8754e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8754e-106">Mit der **switchterminalto substream** -Methode wird ein Terminal auf den Teilnehmer teilstream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8754e-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8754e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8754e-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="8754e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8754e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8754e-109">*pitterminal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8754e-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8754e-110">Zeiger auf die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8754e-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8754e-111">*pitsubstream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8754e-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8754e-112">Zeiger auf die [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8754e-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8754e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8754e-113">Return value</span></span>

<span data-ttu-id="8754e-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8754e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8754e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8754e-115">Return code</span></span>                                                                                     | <span data-ttu-id="8754e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8754e-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8754e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="8754e-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8754e-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="8754e-119"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="8754e-120">Der Zugriff auf Teilnehmer Informationen für den Stream war nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="8754e-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="8754e-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="8754e-122">Der *pparticipants* -oder der *pitsubstream* -Parameter verweist nicht auf eine gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8754e-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="8754e-123"><dt>**TAPI \_ E \_ noItems**</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="8754e-124">Der unter Datenstrom ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="8754e-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="8754e-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="8754e-126">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8754e-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="8754e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8754e-127">Requirements</span></span>



| <span data-ttu-id="8754e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8754e-128">Requirement</span></span> | <span data-ttu-id="8754e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8754e-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8754e-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8754e-130">TAPI version</span></span><br/> | <span data-ttu-id="8754e-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8754e-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8754e-132">Header</span><span class="sxs-lookup"><span data-stu-id="8754e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8754e-133"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8754e-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8754e-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8754e-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8754e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8754e-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8754e-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8754e-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8754e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8754e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8754e-139">**Itparticipantsubstreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="8754e-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="8754e-140">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="8754e-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="8754e-141">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="8754e-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="8754e-142">**Itterminal**</span><span class="sxs-lookup"><span data-stu-id="8754e-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

