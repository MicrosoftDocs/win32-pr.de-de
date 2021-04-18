---
description: Die itparticipantsubstreamcontrol-Schnittstelle wird von ipconf MSP implementiert.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Itparticipantsubstreamcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372765"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="5f6b5-103">Itparticipantsubstreamcontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5f6b5-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="5f6b5-104">\[**Itparticipantsubstreamcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f6b5-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5f6b5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5f6b5-106">Die **itparticipantsubstreamcontrol** -Schnittstelle wird von ipconf MSP implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="5f6b5-107">Diese Schnittstelle wird für das-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="5f6b5-108">Diese Schnittstelle stellt Methoden bereit, die es einer Anwendung ermöglichen, die Übereinstimmung von unter Datenstrom und Teilnehmer zu ermitteln oder zu steuern.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="5f6b5-109">Die **itparticipantsubstreamcontrol** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="5f6b5-110">Member</span><span class="sxs-lookup"><span data-stu-id="5f6b5-110">Members</span></span>

<span data-ttu-id="5f6b5-111">Die **itparticipantsubstreamcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5f6b5-112">**Itparticipantsubstreamcontrol** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5f6b5-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="5f6b5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5f6b5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f6b5-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="5f6b5-114">Methods</span></span>

<span data-ttu-id="5f6b5-115">Die **itparticipantsubstreamcontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="5f6b5-116">Methode</span><span class="sxs-lookup"><span data-stu-id="5f6b5-116">Method</span></span>                                                                                              | <span data-ttu-id="5f6b5-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f6b5-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="5f6b5-118">**" \_ participantfromsubstream" erhalten**</span><span class="sxs-lookup"><span data-stu-id="5f6b5-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="5f6b5-119">Ruft Teilnehmer ab, die einem angegebenen teilstream zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="5f6b5-120">**\_substreamfromteilnehmer aufrufen**</span><span class="sxs-lookup"><span data-stu-id="5f6b5-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="5f6b5-121">Ruft die einem angegebenen Teilnehmer zugeordneten Substreams ab.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="5f6b5-122">**Switchterminalto substream**</span><span class="sxs-lookup"><span data-stu-id="5f6b5-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="5f6b5-123">Legt einen Teilnehmer an einem substream fest.</span><span class="sxs-lookup"><span data-stu-id="5f6b5-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="5f6b5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f6b5-124">Requirements</span></span>



| <span data-ttu-id="5f6b5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f6b5-125">Requirement</span></span> | <span data-ttu-id="5f6b5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5f6b5-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6b5-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5f6b5-127">TAPI version</span></span><br/> | <span data-ttu-id="5f6b5-128">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5f6b5-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5f6b5-129">Header</span><span class="sxs-lookup"><span data-stu-id="5f6b5-129">Header</span></span><br/>       | <dl> <span data-ttu-id="5f6b5-130"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5f6b5-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5f6b5-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f6b5-131">Library</span></span><br/>      | <dl> <span data-ttu-id="5f6b5-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f6b5-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5f6b5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5f6b5-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="5f6b5-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f6b5-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5f6b5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f6b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6b5-136">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="5f6b5-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="5f6b5-137">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="5f6b5-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

