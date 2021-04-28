---
description: 'IEnumPStoreTypes-Schnittstelle: Stellt COM-Standard-Enumerationsmethoden für die IPStore-Schnittstelle bereit.'
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: IEnumPStoreTypes-Schnittstelle (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089358"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="4612d-103">IEnumPStoreTypes-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4612d-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="4612d-104">\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4612d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4612d-105">Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4612d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4612d-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="4612d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4612d-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]</span><span class="sxs-lookup"><span data-stu-id="4612d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4612d-108">Stellt COM-Standard-Enumerationsmethoden für die [**IPStore-Schnittstelle**](ipstore.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="4612d-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4612d-109">Member</span><span class="sxs-lookup"><span data-stu-id="4612d-109">Members</span></span>

<span data-ttu-id="4612d-110">Die **IEnumPStoreTypes-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4612d-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4612d-111">**IEnumPStoreTypes** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="4612d-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="4612d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4612d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4612d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="4612d-113">Methods</span></span>

<span data-ttu-id="4612d-114">Die **IEnumPStoreTypes-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4612d-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="4612d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="4612d-115">Method</span></span>                                  | <span data-ttu-id="4612d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4612d-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4612d-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="4612d-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="4612d-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="4612d-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="4612d-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="4612d-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="4612d-120">Ruft den nächsten angegebenen Anbietertyp in der Enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="4612d-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="4612d-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4612d-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="4612d-122">Setzt auf den Anfang der Enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="4612d-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="4612d-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="4612d-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="4612d-124">Überspringt den angegebenen Anbietertyp in der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="4612d-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="4612d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4612d-125">Remarks</span></span>

<span data-ttu-id="4612d-126">Das Enumeratorobjekt muss freigegeben werden, wenn es nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4612d-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4612d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4612d-127">Requirements</span></span>



| <span data-ttu-id="4612d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4612d-128">Requirement</span></span> | <span data-ttu-id="4612d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4612d-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4612d-130">Header</span><span class="sxs-lookup"><span data-stu-id="4612d-130">Header</span></span><br/> | <dl> <span data-ttu-id="4612d-131"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="4612d-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4612d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4612d-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="4612d-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4612d-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
