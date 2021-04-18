---
description: Gibt den Speicherort eines Zertifikat Speicher an.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358684"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="08ca2-103">CAPICOM \_ Store \_ Location-Enumeration</span><span class="sxs-lookup"><span data-stu-id="08ca2-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="08ca2-104">Der Enumerationstyp " **CAPICOM \_ Store \_ Location** " gibt den Speicherort eines [*Zertifikat Speicher*](../secgloss/c-gly.md)an.</span><span class="sxs-lookup"><span data-stu-id="08ca2-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="08ca2-105">Member</span><span class="sxs-lookup"><span data-stu-id="08ca2-105">Members</span></span>



| <span data-ttu-id="08ca2-106">Member</span><span class="sxs-lookup"><span data-stu-id="08ca2-106">Member</span></span>                                      | <span data-ttu-id="08ca2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08ca2-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="08ca2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="08ca2-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="08ca2-109">**CAPICOM- \_ Speicher Speicher \_**</span><span class="sxs-lookup"><span data-stu-id="08ca2-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="08ca2-110">Der Speicher ist ein Speicher Speicher.</span><span class="sxs-lookup"><span data-stu-id="08ca2-110">The store is a memory store.</span></span> <span data-ttu-id="08ca2-111">Alle Änderungen im Inhalt des Stores werden nicht persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08ca2-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="08ca2-112">0</span><span class="sxs-lookup"><span data-stu-id="08ca2-112">0</span></span>     |
| <span data-ttu-id="08ca2-113">**lokaler CAPICOM- \_ \_ Computer \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="08ca2-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="08ca2-114">Der Speicher ist ein lokaler Computerspeicher.</span><span class="sxs-lookup"><span data-stu-id="08ca2-114">The store is a local machine store.</span></span> <span data-ttu-id="08ca2-115">Lokale Computerspeicher können nur Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="08ca2-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="08ca2-116">Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen im Inhalt des Stores beibehalten.</span><span class="sxs-lookup"><span data-stu-id="08ca2-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="08ca2-117">1</span><span class="sxs-lookup"><span data-stu-id="08ca2-117">1</span></span>     |
| <span data-ttu-id="08ca2-118">**CAPICOM \_ aktueller \_ Benutzer \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="08ca2-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="08ca2-119">Der Speicher ist ein aktueller Benutzerspeicher.</span><span class="sxs-lookup"><span data-stu-id="08ca2-119">The store is a current user store.</span></span> <span data-ttu-id="08ca2-120">Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein.</span><span class="sxs-lookup"><span data-stu-id="08ca2-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="08ca2-121">Wenn dies der Fall ist, werden Änderungen am Inhalt des Stores persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08ca2-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="08ca2-122">2</span><span class="sxs-lookup"><span data-stu-id="08ca2-122">2</span></span>     |
| <span data-ttu-id="08ca2-123">**CAPICOM \_ Active \_ Directory- \_ Benutzer \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="08ca2-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="08ca2-124">Der Speicher ist ein Active Directory Speicher.</span><span class="sxs-lookup"><span data-stu-id="08ca2-124">The store is an Active Directory store.</span></span> <span data-ttu-id="08ca2-125">Active Directory Stores können nur im schreibgeschützten Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="08ca2-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="08ca2-126">Zertifikate können Active Directory speichern nicht hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="08ca2-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="08ca2-127">3</span><span class="sxs-lookup"><span data-stu-id="08ca2-127">3</span></span>     |
| <span data-ttu-id="08ca2-128">**CAPICOM \_ - \_ Smartcard- \_ Benutzer \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="08ca2-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="08ca2-129">Stores unterstützen Smartcard – basierte Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="08ca2-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="08ca2-130">Der Speicher ist die Gruppe der vorhandenen Smartcards.</span><span class="sxs-lookup"><span data-stu-id="08ca2-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="08ca2-131">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="08ca2-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="08ca2-132">4</span><span class="sxs-lookup"><span data-stu-id="08ca2-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="08ca2-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08ca2-133">Remarks</span></span>

<span data-ttu-id="08ca2-134">Der Enumerationstyp " **CAPICOM \_ Store \_ Location** " wird von den folgenden Methoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="08ca2-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="08ca2-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="08ca2-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="08ca2-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="08ca2-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="08ca2-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08ca2-137">Requirements</span></span>



| <span data-ttu-id="08ca2-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08ca2-138">Requirement</span></span> | <span data-ttu-id="08ca2-139">Wert</span><span class="sxs-lookup"><span data-stu-id="08ca2-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08ca2-140">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="08ca2-140">Redistributable</span></span><br/> | <span data-ttu-id="08ca2-141">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="08ca2-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="08ca2-142">Header</span><span class="sxs-lookup"><span data-stu-id="08ca2-142">Header</span></span><br/>          | <dl> <span data-ttu-id="08ca2-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ca2-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
