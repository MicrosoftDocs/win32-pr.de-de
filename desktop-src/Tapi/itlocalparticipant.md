---
description: Die itlocalteilnehmer-Schnittstelle wird für das Stream-Objekt verfügbar gemacht, wenn der ipconf-MSP den-Befehl unterstützt.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Itlocalteilnehmer-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355978"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="96320-103">Itlocalteilnehmer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="96320-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="96320-104">Die **itlocalteilnehmer** -Schnittstelle wird für das Stream-Objekt verfügbar gemacht, wenn der ipconf-MSP den-Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="96320-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="96320-105">Der MSP implementiert Methoden, die es einer Anwendung ermöglichen, Teilnehmer Informationen zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="96320-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="96320-106">Die **itlocalteilnehmer** -Schnittstelle wird durch Aufrufen von **QueryInterface** in [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)erstellt.</span><span class="sxs-lookup"><span data-stu-id="96320-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="96320-107">Member</span><span class="sxs-lookup"><span data-stu-id="96320-107">Members</span></span>

<span data-ttu-id="96320-108">Die **itlocalteilnehmer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="96320-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96320-109">**Itlocalparticipants** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="96320-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="96320-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="96320-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96320-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="96320-111">Methods</span></span>

<span data-ttu-id="96320-112">Die **itlocalparticipants** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="96320-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="96320-113">Methode</span><span class="sxs-lookup"><span data-stu-id="96320-113">Method</span></span>                                                                                     | <span data-ttu-id="96320-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96320-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="96320-115">**\_localparticipanttypdinfo erhalten**</span><span class="sxs-lookup"><span data-stu-id="96320-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="96320-116">Ruft Teilnehmer Informationen ab, z. b. e-Mail-Name oder geografischer Standort</span><span class="sxs-lookup"><span data-stu-id="96320-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="96320-117">**\_localparticipanttypeer dinfo platzieren**</span><span class="sxs-lookup"><span data-stu-id="96320-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="96320-118">Legt Teilnehmer Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="96320-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="96320-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96320-119">Requirements</span></span>



| <span data-ttu-id="96320-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96320-120">Requirement</span></span> | <span data-ttu-id="96320-121">Wert</span><span class="sxs-lookup"><span data-stu-id="96320-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96320-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="96320-122">TAPI version</span></span><br/> | <span data-ttu-id="96320-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="96320-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="96320-124">Header</span><span class="sxs-lookup"><span data-stu-id="96320-124">Header</span></span><br/>       | <dl> <span data-ttu-id="96320-125"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="96320-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="96320-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96320-126">Library</span></span><br/>      | <dl> <span data-ttu-id="96320-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96320-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="96320-128">DLL</span><span class="sxs-lookup"><span data-stu-id="96320-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="96320-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96320-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96320-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96320-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96320-131">**Itstream**</span><span class="sxs-lookup"><span data-stu-id="96320-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

