---
description: Die itparticipantcontrol-Schnittstelle wird von ipconf MSP implementiert.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Itparticipantcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373788"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="e0b7d-103">Itparticipantcontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e0b7d-103">ITParticipantControl interface</span></span>

<span data-ttu-id="e0b7d-104">\[**Itparticipantcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0b7d-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e0b7d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0b7d-106">Die **itparticipantcontrol** -Schnittstelle wird von ipconf MSP implementiert.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="e0b7d-107">Diese Schnittstelle wird für das-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="e0b7d-108">Diese Schnittstelle ermöglicht es einer Anwendung, Zeiger auf die Teilnehmer einer Konferenz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="e0b7d-109">Die **itparticipantcontrol** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="e0b7d-110">Member</span><span class="sxs-lookup"><span data-stu-id="e0b7d-110">Members</span></span>

<span data-ttu-id="e0b7d-111">Die **itparticipantcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e0b7d-112">**Itparticipantcontrol** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e0b7d-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="e0b7d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e0b7d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e0b7d-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e0b7d-114">Methods</span></span>

<span data-ttu-id="e0b7d-115">Die **itparticipantcontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="e0b7d-116">Methode</span><span class="sxs-lookup"><span data-stu-id="e0b7d-116">Method</span></span>                                                                      | <span data-ttu-id="e0b7d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b7d-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0b7d-118">**Enumerateparticipants**</span><span class="sxs-lookup"><span data-stu-id="e0b7d-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="e0b7d-119">Listet die Teilnehmer auf, die derzeit an der Konferenz beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="e0b7d-120">**\_Teilnehmer erhalten**</span><span class="sxs-lookup"><span data-stu-id="e0b7d-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="e0b7d-121">Erstellt eine Auflistung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="e0b7d-122">Wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. die in Visual Basic geschriebenen.</span><span class="sxs-lookup"><span data-stu-id="e0b7d-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e0b7d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0b7d-123">Requirements</span></span>



| <span data-ttu-id="e0b7d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0b7d-124">Requirement</span></span> | <span data-ttu-id="e0b7d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e0b7d-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b7d-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e0b7d-126">TAPI version</span></span><br/> | <span data-ttu-id="e0b7d-127">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e0b7d-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e0b7d-128">Header</span><span class="sxs-lookup"><span data-stu-id="e0b7d-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e0b7d-129"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e0b7d-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="e0b7d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0b7d-130">Library</span></span><br/>      | <dl> <span data-ttu-id="e0b7d-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b7d-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e0b7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b7d-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0b7d-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b7d-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

