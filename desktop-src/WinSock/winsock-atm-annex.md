---
description: ATM ist für LAN-und WAN-Umgebungen anwendbar.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356567"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="92a70-103">Winsock ATM-Anhang</span><span class="sxs-lookup"><span data-stu-id="92a70-103">Winsock ATM Annex</span></span>

<span data-ttu-id="92a70-104">ATM ist für LAN-und WAN-Umgebungen anwendbar.</span><span class="sxs-lookup"><span data-stu-id="92a70-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="92a70-105">Ein ATM-Netzwerk transportiert gleichzeitig eine Vielzahl von Netzwerk Datenverkehr – sprach-, Daten-, Bild-und Videodaten.</span><span class="sxs-lookup"><span data-stu-id="92a70-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="92a70-106">Der Benutzer erhält eine garantierte Quality of Service-Qualität auf Basis eines virtuellen Kanals (VC).</span><span class="sxs-lookup"><span data-stu-id="92a70-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="92a70-107">Element</span><span class="sxs-lookup"><span data-stu-id="92a70-107">Element</span></span>          | <span data-ttu-id="92a70-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92a70-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a70-109">Protokoll Name (n)</span><span class="sxs-lookup"><span data-stu-id="92a70-109">Protocol name(s)</span></span> | <span data-ttu-id="92a70-110">Atmproto \_ AAL5, atmproto \_ aaluser</span><span class="sxs-lookup"><span data-stu-id="92a70-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="92a70-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92a70-111">Description</span></span>      | <span data-ttu-id="92a70-112">ATM AAL5 stellt einen Transportdienst bereit, der verbindungsorientiert, Nachrichten Begrenzung beibehalten und QoS garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="92a70-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="92a70-113">Atmproto \_ aaluser ist eine benutzerdefinierte Aal-Datei.</span><span class="sxs-lookup"><span data-stu-id="92a70-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="92a70-114">Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="92a70-114">Address family</span></span>   | <span data-ttu-id="92a70-115">AF- \_ ATM</span><span class="sxs-lookup"><span data-stu-id="92a70-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="92a70-116">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="92a70-116">Header file</span></span>      | <span data-ttu-id="92a70-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="92a70-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="92a70-118">In diesem Abschnitt werden die Anforderungen für den asynchronen Übertragungsmodus (ATM) beschrieben, die zur Unterstützung der systemeigenen ATM-Dienste erforderlich sind, die verfügbar sind und in der Spezifikation für die Benutzer Netzwerkschnittstelle (Uni), Version 3. x (3,0 und 3,1) des ATM-Forums</span><span class="sxs-lookup"><span data-stu-id="92a70-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="92a70-119">In diesem Dokument werden Aal-Typ 5 (Nachrichten Modus) und benutzerdefinierte Aal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92a70-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="92a70-120">In zukünftigen Versionen dieses Dokuments werden andere Arten von Aal und Uni 4,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92a70-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



