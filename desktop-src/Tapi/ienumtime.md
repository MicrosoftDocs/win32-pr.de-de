---
description: 'Die ienumtime-Schnittstelle stellt com-Standard-Enumerationsmethoden für die ittime-Schnittstelle bereit. Die ittimecollection:: get \_ enumerationif-Methode gibt einen Zeiger auf ienumtime zurück.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Ienumtime-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370730"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="61892-104">Ienumtime-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="61892-104">IEnumTime interface</span></span>

<span data-ttu-id="61892-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61892-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="61892-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="61892-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="61892-107">Die **ienumtime** -Schnittstelle stellt com-Standard-Enumerationsmethoden für die [**ittime**](ittime.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="61892-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="61892-108">Die [**ittimecollection:: get \_ enumerationif**](ittimecollection-get-enumerationif.md) -Methode gibt einen Zeiger auf **ienumtime** zurück.</span><span class="sxs-lookup"><span data-stu-id="61892-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="61892-109">Member</span><span class="sxs-lookup"><span data-stu-id="61892-109">Members</span></span>

<span data-ttu-id="61892-110">Die **ienumtime** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="61892-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="61892-111">**Ienumtime** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="61892-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="61892-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="61892-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61892-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="61892-113">Methods</span></span>

<span data-ttu-id="61892-114">Die **ienumtime** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="61892-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="61892-115">Methode</span><span class="sxs-lookup"><span data-stu-id="61892-115">Method</span></span>                           | <span data-ttu-id="61892-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61892-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61892-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="61892-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="61892-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="61892-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="61892-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="61892-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="61892-120">Ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="61892-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="61892-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="61892-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="61892-122">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="61892-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="61892-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="61892-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="61892-124">Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="61892-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="61892-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61892-125">Requirements</span></span>



| <span data-ttu-id="61892-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61892-126">Requirement</span></span> | <span data-ttu-id="61892-127">Wert</span><span class="sxs-lookup"><span data-stu-id="61892-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61892-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="61892-128">TAPI version</span></span><br/> | <span data-ttu-id="61892-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="61892-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="61892-130">Header</span><span class="sxs-lookup"><span data-stu-id="61892-130">Header</span></span><br/>       | <dl> <span data-ttu-id="61892-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="61892-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="61892-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61892-132">Library</span></span><br/>      | <dl> <span data-ttu-id="61892-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61892-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="61892-134">DLL</span><span class="sxs-lookup"><span data-stu-id="61892-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="61892-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61892-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

