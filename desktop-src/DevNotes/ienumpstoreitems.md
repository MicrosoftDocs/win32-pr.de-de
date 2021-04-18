---
description: Stellt die com-Standard-Enumerationsmethoden für die ipstore-Schnittstelle bereit.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Iumumpstoreitems-Schnittstelle (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368347"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="9666b-103">Iumumpstoreitems-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9666b-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="9666b-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9666b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9666b-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9666b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9666b-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="9666b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9666b-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="9666b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9666b-108">Stellt die com-Standard-Enumerationsmethoden für die [**ipstore**](ipstore.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="9666b-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="9666b-109">Member</span><span class="sxs-lookup"><span data-stu-id="9666b-109">Members</span></span>

<span data-ttu-id="9666b-110">Die **iumumpstoreitems** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9666b-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9666b-111">**Ienumpstoreitems** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9666b-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="9666b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="9666b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9666b-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9666b-113">Methods</span></span>

<span data-ttu-id="9666b-114">Die **ierumpstoreitems** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9666b-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="9666b-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9666b-115">Method</span></span>                                  | <span data-ttu-id="9666b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9666b-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9666b-117">**Klon**</span><span class="sxs-lookup"><span data-stu-id="9666b-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="9666b-118">Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="9666b-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="9666b-119">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="9666b-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="9666b-120">Ruft das nächste angegebene Datenelement in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="9666b-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="9666b-121">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="9666b-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="9666b-122">Setzt auf den Anfang der enumerationssequenz zurück.</span><span class="sxs-lookup"><span data-stu-id="9666b-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="9666b-123">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="9666b-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="9666b-124">Überspringt das angegebene Datenelement in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="9666b-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="9666b-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9666b-125">Remarks</span></span>

<span data-ttu-id="9666b-126">Jedes Element muss nach dem auflisten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9666b-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="9666b-127">Das Enumeratorobjekt muss auch freigegeben werden, wenn es nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9666b-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9666b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9666b-128">Requirements</span></span>



| <span data-ttu-id="9666b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9666b-129">Requirement</span></span> | <span data-ttu-id="9666b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9666b-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9666b-131">Header</span><span class="sxs-lookup"><span data-stu-id="9666b-131">Header</span></span><br/> | <dl> <span data-ttu-id="9666b-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="9666b-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="9666b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9666b-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="9666b-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9666b-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
