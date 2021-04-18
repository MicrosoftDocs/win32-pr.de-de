---
description: Die itmediacollection-Schnittstelle ermöglicht den Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Itmediacollection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365381"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="4699a-103">Itmediacollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4699a-103">ITMediaCollection interface</span></span>

<span data-ttu-id="4699a-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4699a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4699a-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4699a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4699a-106">Die **itmediacollection** -Schnittstelle ermöglicht den Zugriff auf den Satz von Medieninformationen in einer SDP-Konferenzbeschreibung (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="4699a-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="4699a-107">Jede Medien Beschreibung im SDP wird durch eine [**ITmedia**](itmedia.md) -Schnittstelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4699a-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="4699a-108">**Itmediacollection** ermöglicht die Bearbeitung des Satzes von **ITmedia** -Informationen für den SDP, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="4699a-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="4699a-109">Ermöglicht den Medien Zugriff nach Index.</span><span class="sxs-lookup"><span data-stu-id="4699a-109">Allows media access by index.</span></span>
-   <span data-ttu-id="4699a-110">Ermöglicht das Erstellen und Löschen von Medien.</span><span class="sxs-lookup"><span data-stu-id="4699a-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="4699a-111">Die [**itsdp:: get \_ mediacollection**](itsdp-get-mediacollection.md) -Methode erstellt die **itmediacollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4699a-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="4699a-112">Member</span><span class="sxs-lookup"><span data-stu-id="4699a-112">Members</span></span>

<span data-ttu-id="4699a-113">Die **itmediacollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4699a-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4699a-114">**Itmediacollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4699a-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="4699a-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="4699a-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4699a-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="4699a-116">Methods</span></span>

<span data-ttu-id="4699a-117">Die **itmediacollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4699a-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="4699a-118">Methode</span><span class="sxs-lookup"><span data-stu-id="4699a-118">Method</span></span>                                                            | <span data-ttu-id="4699a-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4699a-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="4699a-120">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="4699a-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="4699a-121">Erstellt ein neues Medium mit Standardeigenschaften und gibt dieses zurück.</span><span class="sxs-lookup"><span data-stu-id="4699a-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="4699a-122">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="4699a-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="4699a-123">Löscht das Medium, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="4699a-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="4699a-124">**" \_ \_ netwenum"**</span><span class="sxs-lookup"><span data-stu-id="4699a-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="4699a-125">Gibt einen Enumerator für die Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="4699a-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="4699a-126">**get- \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="4699a-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="4699a-127">Ruft die Anzahl der Medien in der Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="4699a-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="4699a-128">**\_enumerationif erhalten**</span><span class="sxs-lookup"><span data-stu-id="4699a-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="4699a-129">Ruft den Zeiger auf die Enumerationsschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4699a-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="4699a-130">**\_Element erhalten**</span><span class="sxs-lookup"><span data-stu-id="4699a-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="4699a-131">Gibt das Medium zurück, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="4699a-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="4699a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4699a-132">Requirements</span></span>



| <span data-ttu-id="4699a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4699a-133">Requirement</span></span> | <span data-ttu-id="4699a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4699a-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4699a-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4699a-135">TAPI version</span></span><br/> | <span data-ttu-id="4699a-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4699a-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4699a-137">Header</span><span class="sxs-lookup"><span data-stu-id="4699a-137">Header</span></span><br/>       | <dl> <span data-ttu-id="4699a-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4699a-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4699a-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4699a-139">Library</span></span><br/>      | <dl> <span data-ttu-id="4699a-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4699a-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4699a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4699a-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="4699a-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4699a-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

