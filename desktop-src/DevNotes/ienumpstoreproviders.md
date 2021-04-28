---
description: 'IEnumPStoreProviders-Schnittstelle: Stellt COM-Standard-Enumerationsmethoden für die IPStore-Schnittstelle bereit.'
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: IEnumPStoreProviders-Schnittstelle (Pstore.h)
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
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089348"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="0dd10-103">IEnumPStoreProviders-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0dd10-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="0dd10-104">\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0dd10-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0dd10-105">Es ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0dd10-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0dd10-106">Pstore verwendet eine ältere Implementierung des Datenschutzes.</span><span class="sxs-lookup"><span data-stu-id="0dd10-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0dd10-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]</span><span class="sxs-lookup"><span data-stu-id="0dd10-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0dd10-108">Stellt COM-Standard-Enumerationsmethoden für die [**IPStore-Schnittstelle**](ipstore.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="0dd10-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="0dd10-109">Member</span><span class="sxs-lookup"><span data-stu-id="0dd10-109">Members</span></span>

<span data-ttu-id="0dd10-110">Die **IEnumPStoreProviders-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="0dd10-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0dd10-111">**IEnumPStoreProviders** verfügt auch über diese Membertypen:</span><span class="sxs-lookup"><span data-stu-id="0dd10-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="0dd10-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0dd10-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0dd10-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0dd10-113">Methods</span></span>

<span data-ttu-id="0dd10-114">Die **IEnumPStoreProviders-Schnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0dd10-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="0dd10-115">Methode</span><span class="sxs-lookup"><span data-stu-id="0dd10-115">Method</span></span>                                      | <span data-ttu-id="0dd10-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dd10-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dd10-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="0dd10-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="0dd10-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="0dd10-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="0dd10-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="0dd10-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="0dd10-120">Ruft den nächsten angegebenen Anbieter in der Enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="0dd10-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="0dd10-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="0dd10-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="0dd10-122">Setzt auf den Anfang der Enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="0dd10-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="0dd10-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="0dd10-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="0dd10-124">Überspringt den angegebenen Anbieter in der Enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="0dd10-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="0dd10-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dd10-125">Requirements</span></span>



| <span data-ttu-id="0dd10-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dd10-126">Requirement</span></span> | <span data-ttu-id="0dd10-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0dd10-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd10-128">Header</span><span class="sxs-lookup"><span data-stu-id="0dd10-128">Header</span></span><br/> | <dl> <span data-ttu-id="0dd10-129"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd10-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0dd10-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0dd10-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="0dd10-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dd10-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
