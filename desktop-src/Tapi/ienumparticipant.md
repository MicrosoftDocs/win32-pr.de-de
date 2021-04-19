---
description: 'Die ienumparticipants-Schnittstelle stellt com-Standard-Enumerationsmethoden für die itparticipants-Schnittstelle bereit. Die itparticipantcontrol:: enumerateparticipants-Methode gibt einen Zeiger auf ienumteilnehmer zurück.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Ienumteilnehmer-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370238"
---
# <a name="ienumparticipant-interface"></a><span data-ttu-id="ba032-104">Ienumteilnehmer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba032-104">IEnumParticipant interface</span></span>

<span data-ttu-id="ba032-105">\[**Ienumteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba032-105">\[**IEnumParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ba032-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ba032-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ba032-107">Die **ienumparticipants** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**itparticipants**](itparticipant.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="ba032-107">The **IEnumParticipant** interface provides COM-standard enumeration methods for the [**ITParticipant**](itparticipant.md) interface.</span></span> <span data-ttu-id="ba032-108">Die [**itparticipantcontrol:: enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md) -Methode gibt einen Zeiger auf **ienumteilnehmer** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba032-108">The [**ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method returns a pointer to **IEnumParticipant**.</span></span>

<span data-ttu-id="ba032-109">Die **ienumteilnehmer** -Schnittstelle ist in Visual Basic-und Skriptsprachen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ba032-109">The **IEnumParticipant** interface is hidden from Visual Basic and scripting languages.</span></span>

## <a name="members"></a><span data-ttu-id="ba032-110">Member</span><span class="sxs-lookup"><span data-stu-id="ba032-110">Members</span></span>

<span data-ttu-id="ba032-111">Die **ienumparticipants** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ba032-111">The **IEnumParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ba032-112">**Ienumparticipants** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ba032-112">**IEnumParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="ba032-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba032-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ba032-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="ba032-114">Methods</span></span>

<span data-ttu-id="ba032-115">Die **ienumparticipants** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ba032-115">The **IEnumParticipant** interface has these methods.</span></span>



| <span data-ttu-id="ba032-116">Methode</span><span class="sxs-lookup"><span data-stu-id="ba032-116">Method</span></span>                                  | <span data-ttu-id="ba032-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba032-117">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba032-118">**Klon**</span><span class="sxs-lookup"><span data-stu-id="ba032-118">**Clone**</span></span>](ienumparticipant-clone.md) | <span data-ttu-id="ba032-119">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="ba032-119">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="ba032-120">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="ba032-120">**Next**</span></span>](ienumparticipant-next.md)   | <span data-ttu-id="ba032-121">Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="ba032-121">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="ba032-122">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ba032-122">**Reset**</span></span>](ienumparticipant-reset.md) | <span data-ttu-id="ba032-123">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="ba032-123">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="ba032-124">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="ba032-124">**Skip**</span></span>](ienumparticipant-skip.md)   | <span data-ttu-id="ba032-125">Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="ba032-125">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ba032-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba032-126">Requirements</span></span>



| <span data-ttu-id="ba032-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba032-127">Requirement</span></span> | <span data-ttu-id="ba032-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ba032-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba032-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ba032-129">TAPI version</span></span><br/> | <span data-ttu-id="ba032-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ba032-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ba032-131">Header</span><span class="sxs-lookup"><span data-stu-id="ba032-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ba032-132"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ba032-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ba032-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba032-133">Library</span></span><br/>      | <dl> <span data-ttu-id="ba032-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba032-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ba032-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ba032-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="ba032-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba032-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ba032-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba032-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba032-138">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="ba032-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

