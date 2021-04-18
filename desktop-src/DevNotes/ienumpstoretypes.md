---
description: Stellt com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Iumumpstoretypes-Schnittstelle (pstore. h)
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
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371503"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="5c980-103">Iumumpstoretypes-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5c980-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="5c980-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c980-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5c980-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c980-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5c980-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="5c980-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5c980-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="5c980-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5c980-108">Stellt com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="5c980-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="5c980-109">Member</span><span class="sxs-lookup"><span data-stu-id="5c980-109">Members</span></span>

<span data-ttu-id="5c980-110">Die **ierumpstoretypes** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5c980-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5c980-111">**Ienumpstoretypes** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5c980-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="5c980-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c980-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c980-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5c980-113">Methods</span></span>

<span data-ttu-id="5c980-114">Die **ierumpstoretypes** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5c980-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="5c980-115">Methode</span><span class="sxs-lookup"><span data-stu-id="5c980-115">Method</span></span>                                  | <span data-ttu-id="5c980-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c980-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c980-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="5c980-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="5c980-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="5c980-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="5c980-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="5c980-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="5c980-120">Ruft den nächsten angegebenen Anbietertyp in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="5c980-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="5c980-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="5c980-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="5c980-122">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="5c980-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="5c980-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="5c980-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="5c980-124">Überspringt den angegebenen Anbietertyp in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="5c980-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="5c980-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c980-125">Remarks</span></span>

<span data-ttu-id="5c980-126">Das Enumeratorobjekt muss freigegeben werden, wenn es nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c980-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c980-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c980-127">Requirements</span></span>



| <span data-ttu-id="5c980-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c980-128">Requirement</span></span> | <span data-ttu-id="5c980-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5c980-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c980-130">Header</span><span class="sxs-lookup"><span data-stu-id="5c980-130">Header</span></span><br/> | <dl> <span data-ttu-id="5c980-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c980-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5c980-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5c980-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="5c980-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c980-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
