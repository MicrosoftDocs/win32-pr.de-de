---
description: Die ittimecollection-Schnittstelle ist eine anbieterspezifische Schnittstelle für das Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Ittimecollection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373710"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="a70d8-103">Ittimecollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a70d8-103">ITTimeCollection interface</span></span>

<span data-ttu-id="a70d8-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a70d8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a70d8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a70d8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a70d8-106">Die **ittimecollection** -Schnittstelle ist eine anbieterspezifische Schnittstelle für das Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a70d8-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="a70d8-107">Diese Schnittstelle ermöglicht den Zugriff auf [**ittime**](ittime.md) -Schnittstellen nach Index und ermöglicht außerdem das Erstellen und Löschen von Zeit Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a70d8-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="a70d8-108">Die [**itsdp:: get \_ timecollection**](itsdp-get-timecollection.md) -Methode erstellt die **ittimecollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a70d8-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="a70d8-109">Member</span><span class="sxs-lookup"><span data-stu-id="a70d8-109">Members</span></span>

<span data-ttu-id="a70d8-110">Die **ittimecollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a70d8-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a70d8-111">**Ittimecollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a70d8-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="a70d8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70d8-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a70d8-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="a70d8-113">Methods</span></span>

<span data-ttu-id="a70d8-114">Die **ittimecollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a70d8-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="a70d8-115">Methode</span><span class="sxs-lookup"><span data-stu-id="a70d8-115">Method</span></span>                                                           | <span data-ttu-id="a70d8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a70d8-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a70d8-117">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="a70d8-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="a70d8-118">Erstellt eine [**ittime**](ittime.md) -Komponente.</span><span class="sxs-lookup"><span data-stu-id="a70d8-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="a70d8-119">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="a70d8-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="a70d8-120">Löscht eine [**ittime**](ittime.md) -Komponente.</span><span class="sxs-lookup"><span data-stu-id="a70d8-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="a70d8-121">**" \_ \_ netwenum"**</span><span class="sxs-lookup"><span data-stu-id="a70d8-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="a70d8-122">Gibt einen Enumerator für die Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="a70d8-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="a70d8-123">**get- \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="a70d8-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="a70d8-124">Ruft die Anzahl der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="a70d8-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="a70d8-125">**\_enumerationif erhalten**</span><span class="sxs-lookup"><span data-stu-id="a70d8-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="a70d8-126">Gibt die [**ienumtime**](ienumtime.md) -Enumerationsschnittstelle zurück, die [**ittime**](ittime.md)auflistet.</span><span class="sxs-lookup"><span data-stu-id="a70d8-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="a70d8-127">**\_Element erhalten**</span><span class="sxs-lookup"><span data-stu-id="a70d8-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="a70d8-128">Gibt ein Element in der Auflistung zurück, wenn ein Index angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a70d8-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a70d8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a70d8-129">Requirements</span></span>



| <span data-ttu-id="a70d8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a70d8-130">Requirement</span></span> | <span data-ttu-id="a70d8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a70d8-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a70d8-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a70d8-132">TAPI version</span></span><br/> | <span data-ttu-id="a70d8-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a70d8-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a70d8-134">Header</span><span class="sxs-lookup"><span data-stu-id="a70d8-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a70d8-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a70d8-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a70d8-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a70d8-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a70d8-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70d8-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a70d8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a70d8-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a70d8-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a70d8-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

