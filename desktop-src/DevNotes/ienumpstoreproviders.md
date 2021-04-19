---
description: Stellt com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Ienumpstoreproviders-Schnittstelle (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356051"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="232df-103">Ienumpstoreproviders-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="232df-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="232df-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="232df-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="232df-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="232df-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="232df-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="232df-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="232df-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="232df-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="232df-108">Stellt com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="232df-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="232df-109">Member</span><span class="sxs-lookup"><span data-stu-id="232df-109">Members</span></span>

<span data-ttu-id="232df-110">Die **ienumpstoreproviders** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="232df-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="232df-111">**Ienumpstoreproviders** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="232df-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="232df-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="232df-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="232df-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="232df-113">Methods</span></span>

<span data-ttu-id="232df-114">Die **ienumpstoreproviders** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="232df-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="232df-115">Methode</span><span class="sxs-lookup"><span data-stu-id="232df-115">Method</span></span>                                      | <span data-ttu-id="232df-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="232df-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="232df-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="232df-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="232df-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="232df-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="232df-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="232df-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="232df-120">Ruft den nächsten angegebenen Anbieter in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="232df-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="232df-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="232df-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="232df-122">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="232df-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="232df-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="232df-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="232df-124">Überspringt den angegebenen Anbieter in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="232df-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="232df-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="232df-125">Requirements</span></span>



| <span data-ttu-id="232df-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="232df-126">Requirement</span></span> | <span data-ttu-id="232df-127">Wert</span><span class="sxs-lookup"><span data-stu-id="232df-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="232df-128">Header</span><span class="sxs-lookup"><span data-stu-id="232df-128">Header</span></span><br/> | <dl> <span data-ttu-id="232df-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="232df-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="232df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="232df-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="232df-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="232df-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
