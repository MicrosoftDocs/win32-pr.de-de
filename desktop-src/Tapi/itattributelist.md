---
description: Die itattributelist-Schnittstelle stellt Methoden zum erhalten und Festlegen von nicht interpretierten Attributen bereit.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Itattributelist-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352123"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="52ccb-103">Itattributelist-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="52ccb-103">ITAttributeList interface</span></span>

<span data-ttu-id="52ccb-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52ccb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="52ccb-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="52ccb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="52ccb-106">Die **itattributelist** -Schnittstelle stellt Methoden zum erhalten und Festlegen von nicht interpretierten Attributen bereit.</span><span class="sxs-lookup"><span data-stu-id="52ccb-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="52ccb-107">Bezüglich der Position der Attribut Zeichenfolgen in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327), wird von den Methoden angenommen, dass alle Attribut Zeichenfolgen direkt vor dem Angeben der Medien Attribute und nach allen allgemeinen Attributen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="52ccb-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="52ccb-108">Die **itattributelist** -Schnittstelle wird erstellt, indem **QueryInterface** für [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="52ccb-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="52ccb-109">Member</span><span class="sxs-lookup"><span data-stu-id="52ccb-109">Members</span></span>

<span data-ttu-id="52ccb-110">Die **itattributelist** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52ccb-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="52ccb-111">**Itattributelist** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52ccb-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="52ccb-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="52ccb-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52ccb-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="52ccb-113">Methods</span></span>

<span data-ttu-id="52ccb-114">Die **itattributelist** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52ccb-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="52ccb-115">Methode</span><span class="sxs-lookup"><span data-stu-id="52ccb-115">Method</span></span>                                                          | <span data-ttu-id="52ccb-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52ccb-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="52ccb-117">**Eren**</span><span class="sxs-lookup"><span data-stu-id="52ccb-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="52ccb-118">Fügt das Attribut am angegebenen Index hinzu.</span><span class="sxs-lookup"><span data-stu-id="52ccb-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="52ccb-119">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="52ccb-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="52ccb-120">Löscht das Attribut am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="52ccb-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="52ccb-121">**\_AttributeList erhalten**</span><span class="sxs-lookup"><span data-stu-id="52ccb-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="52ccb-122">Ruft die Liste der Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="52ccb-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="52ccb-123">**get- \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="52ccb-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="52ccb-124">Ruft die Anzahl der Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="52ccb-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="52ccb-125">**\_Element erhalten**</span><span class="sxs-lookup"><span data-stu-id="52ccb-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="52ccb-126">Ruft das durch den Index angegebene Attribut ab.</span><span class="sxs-lookup"><span data-stu-id="52ccb-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="52ccb-127">**\_AttributeList platzieren**</span><span class="sxs-lookup"><span data-stu-id="52ccb-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="52ccb-128">Legt die Liste der Attribute fest.</span><span class="sxs-lookup"><span data-stu-id="52ccb-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="52ccb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52ccb-129">Requirements</span></span>



| <span data-ttu-id="52ccb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52ccb-130">Requirement</span></span> | <span data-ttu-id="52ccb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="52ccb-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52ccb-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="52ccb-132">TAPI version</span></span><br/> | <span data-ttu-id="52ccb-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="52ccb-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="52ccb-134">Header</span><span class="sxs-lookup"><span data-stu-id="52ccb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="52ccb-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ccb-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="52ccb-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52ccb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="52ccb-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ccb-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="52ccb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="52ccb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="52ccb-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52ccb-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

