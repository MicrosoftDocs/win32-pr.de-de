---
description: Die Peer Infrastruktur verwendet die folgenden allgemeinen Strukturen.
ms.assetid: b8f290fb-ae0b-44de-87cc-d25f7e0e3ae6
title: Allgemeine Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fb4afd791d42565202ef55779d1b4ee9260efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362237"
---
# <a name="common-structures"></a><span data-ttu-id="9f481-103">Allgemeine Strukturen</span><span class="sxs-lookup"><span data-stu-id="9f481-103">Common Structures</span></span>

<span data-ttu-id="9f481-104">Die Peer Infrastruktur verwendet die folgenden allgemeinen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f481-104">The Peer Infrastructure uses the following common structures.</span></span>



| <span data-ttu-id="9f481-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="9f481-105">Structure</span></span>                                                                          | <span data-ttu-id="9f481-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f481-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f481-107">**Peer \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="9f481-107">**PEER\_ADDRESS**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_address)                                              | <span data-ttu-id="9f481-108">Gibt die Informationen zur IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="9f481-108">Specifies the information about the IP address.</span></span>                                                                                     |
| [<span data-ttu-id="9f481-109">**Peer \_ Verbindungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9f481-109">**PEER\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_connection_info)                             | <span data-ttu-id="9f481-110">Enthält Informationen zu einer Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9f481-110">Contains information about a connection.</span></span> <span data-ttu-id="9f481-111">Diese Struktur wird zurückgegeben, wenn Sie Peer Diagramm-oder Gruppierungs Verbindungen auflisten.</span><span class="sxs-lookup"><span data-stu-id="9f481-111">This structure is returned when you are enumerating peer graphing or grouping connections.</span></span> |
| [<span data-ttu-id="9f481-112">**Peer \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9f481-112">**PEER\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_data)                                                    | <span data-ttu-id="9f481-113">Enthält Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="9f481-113">Contains binary data.</span></span>                                                                                                               |
| [<span data-ttu-id="9f481-114">**\_ \_ \_ Änderungs Daten für Peer Ereignis Verbindung \_**</span><span class="sxs-lookup"><span data-stu-id="9f481-114">**PEER\_EVENT\_CONNECTION\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_connection_change_data) | <span data-ttu-id="9f481-115">Enthält aktualisierte Informationen, die Änderungen an einer benachbarten oder direkten Verbindung enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f481-115">Contains updated information that includes changes to a neighbor or direct connection.</span></span>                                              |
| [<span data-ttu-id="9f481-116">**\_ \_ eingehende \_ Daten des Peer Ereignisses**</span><span class="sxs-lookup"><span data-stu-id="9f481-116">**PEER\_EVENT\_INCOMING\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)                    | <span data-ttu-id="9f481-117">Enthält aktualisierte Informationen, die Datenänderungen enthalten, die ein Knoten von einer benachbarten oder direkten Verbindung empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f481-117">Contains updated information that includes data changes a node receives from a neighbor or direct connection.</span></span>                       |
| [<span data-ttu-id="9f481-118">**\_Änderungs Daten des Peer Ereignis \_ Datensatzes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9f481-118">**PEER\_EVENT\_RECORD\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data)         | <span data-ttu-id="9f481-119">Enthält aktualisierte Informationen, die von einer Anwendung für Datenänderungen an einem Datensatz-oder Datenbanktyp angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9f481-119">Contains updated information that an application requests for data changes to a record or record type.</span></span>                              |
| [<span data-ttu-id="9f481-120">**Peer \_ Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="9f481-120">**PEER\_RECORD**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_record)                                                | <span data-ttu-id="9f481-121">Enthält das Daten Satz Objekt, das von einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f481-121">Contains the record object that an application uses.</span></span>                                                                                |
| [<span data-ttu-id="9f481-122">**Peer \_ Versions \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9f481-122">**PEER\_VERSION\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_version_data)                                   | <span data-ttu-id="9f481-123">Enthält die Versionsinformationen zu den Peer-und Gruppierungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="9f481-123">Contains the version information about the Peer Graphing and Grouping APIs.</span></span>                                                         |



 

 

 



