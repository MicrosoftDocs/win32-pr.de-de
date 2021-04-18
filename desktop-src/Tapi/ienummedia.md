---
description: 'Die ienummedia-Schnittstelle stellt com-Standard-Enumerationsmethoden für die ITmedia-Schnittstelle bereit. Die itmediacollection:: get \_ enumerationif-Methode gibt einen Zeiger auf ienummedia zurück.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Ienummedia-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352142"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="50fc9-104">Ienummedia-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50fc9-104">IEnumMedia interface</span></span>

<span data-ttu-id="50fc9-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50fc9-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50fc9-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="50fc9-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="50fc9-107">Die **ienummedia** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**ITmedia**](itmedia.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="50fc9-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="50fc9-108">Die [**itmediacollection:: get \_ enumerationif**](itmediacollection-get-enumerationif.md) -Methode gibt einen Zeiger auf **ienummedia** zurück.</span><span class="sxs-lookup"><span data-stu-id="50fc9-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="50fc9-109">Member</span><span class="sxs-lookup"><span data-stu-id="50fc9-109">Members</span></span>

<span data-ttu-id="50fc9-110">Die **ienummedia** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="50fc9-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="50fc9-111">**Ienummedia** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50fc9-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="50fc9-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="50fc9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="50fc9-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="50fc9-113">Methods</span></span>

<span data-ttu-id="50fc9-114">Die **ienummedia** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="50fc9-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="50fc9-115">Methode</span><span class="sxs-lookup"><span data-stu-id="50fc9-115">Method</span></span>                            | <span data-ttu-id="50fc9-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50fc9-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50fc9-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="50fc9-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="50fc9-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="50fc9-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="50fc9-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="50fc9-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="50fc9-120">Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="50fc9-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="50fc9-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="50fc9-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="50fc9-122">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="50fc9-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="50fc9-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="50fc9-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="50fc9-124">Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="50fc9-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="50fc9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50fc9-125">Requirements</span></span>



| <span data-ttu-id="50fc9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50fc9-126">Requirement</span></span> | <span data-ttu-id="50fc9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="50fc9-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50fc9-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="50fc9-128">TAPI version</span></span><br/> | <span data-ttu-id="50fc9-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="50fc9-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="50fc9-130">Header</span><span class="sxs-lookup"><span data-stu-id="50fc9-130">Header</span></span><br/>       | <dl> <span data-ttu-id="50fc9-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="50fc9-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="50fc9-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50fc9-132">Library</span></span><br/>      | <dl> <span data-ttu-id="50fc9-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50fc9-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="50fc9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="50fc9-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="50fc9-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50fc9-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

