---
description: Die folgenden Enumerationen unterstützen die DRT-API (verteilte Routing Tabelle).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Verteilte Routing Tabellen-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349865"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="16a1a-103">Verteilte Routing Tabellen-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="16a1a-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="16a1a-104">Die folgenden Enumerationen unterstützen die DRT-API (verteilte Routing Tabelle).</span><span class="sxs-lookup"><span data-stu-id="16a1a-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="16a1a-105">Enumeration</span><span class="sxs-lookup"><span data-stu-id="16a1a-105">Enumeration</span></span>                                                            | <span data-ttu-id="16a1a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16a1a-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16a1a-107">**DRT- \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="16a1a-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="16a1a-108">Definiert den Satz von IPv6-Bereichen, in denen DRT verwendet wird, wenn der von [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)erstellte IPv6-UDP-Transport verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16a1a-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="16a1a-109">**DRT \_ - \_ adressflags**</span><span class="sxs-lookup"><span data-stu-id="16a1a-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="16a1a-110">Definiert den Satz von Antworten, der von einem zwischen Knoten beim Ausführen einer Suche nach einem Schlüssel zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="16a1a-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="16a1a-111">**DRT- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="16a1a-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="16a1a-112">Definiert die möglichen Verbindungs-und Fehlerzustände eines lokalen Knotens.</span><span class="sxs-lookup"><span data-stu-id="16a1a-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="16a1a-113">**DRT-Übereinstimmungs \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="16a1a-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="16a1a-114">Definiert die Genauigkeit der Ergebnisse, die zurückgegeben werden, wenn eine Suche durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16a1a-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="16a1a-115">**\_ \_ \_ regeländerungstyp für DRT-blattsatz \_**</span><span class="sxs-lookup"><span data-stu-id="16a1a-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="16a1a-116">Definiert die Gruppe von Änderungs Typen, die auf einem lokalen Blatt Satz Knoten im lokalen DRT-Cache ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="16a1a-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="16a1a-117">**DRT \_ - \_ Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="16a1a-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="16a1a-118">Definiert den Satz von Ereignissen, die von der DRT ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="16a1a-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="16a1a-119">**DRT- \_ Sicherheits \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="16a1a-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="16a1a-120">Definiert die möglichen Sicherheitsmodi des DRT.</span><span class="sxs-lookup"><span data-stu-id="16a1a-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="16a1a-121">Diese Enumeration ist ein Feld der [**DRT- \_ Einstellungs**](/windows/desktop/api/drt/ns-drt-drt_settings) Struktur.</span><span class="sxs-lookup"><span data-stu-id="16a1a-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="16a1a-122">**DRT- \_ Registrierungs \_ Status**</span><span class="sxs-lookup"><span data-stu-id="16a1a-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="16a1a-123">Definiert den Zustand eines registrierten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="16a1a-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="16a1a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16a1a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a1a-125">Strukturen verteilter Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="16a1a-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="16a1a-126">Tabellen Funktionen für verteilte Routing</span><span class="sxs-lookup"><span data-stu-id="16a1a-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="16a1a-127">Tabellen-API Referenz zu verteiltem Routing</span><span class="sxs-lookup"><span data-stu-id="16a1a-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



