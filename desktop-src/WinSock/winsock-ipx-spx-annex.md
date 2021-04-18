---
description: In diesem Abschnitt werden die für Internetwork Packet Exchange/sequenzierte Paket Austausch (IPX/SPX) spezifischen Winsock-Erweiterungen beschrieben. Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die entweder besondere Überlegungen erfordern oder eindeutiges Verhalten aufweisen können.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: WinSock-IPX/SPX-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354562"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="c3fb7-104">WinSock-IPX/SPX-Anhang</span><span class="sxs-lookup"><span data-stu-id="c3fb7-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="c3fb7-105">In diesem Abschnitt werden die für Internetwork Packet Exchange/sequenzierte Paket Austausch (IPX/SPX) spezifischen Winsock-Erweiterungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="c3fb7-106">Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die entweder besondere Überlegungen erfordern oder eindeutiges Verhalten aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="c3fb7-107">Element</span><span class="sxs-lookup"><span data-stu-id="c3fb7-107">Element</span></span>          | <span data-ttu-id="c3fb7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3fb7-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3fb7-109">Protokoll Name (n)</span><span class="sxs-lookup"><span data-stu-id="c3fb7-109">Protocol name(s)</span></span> | <span data-ttu-id="c3fb7-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="c3fb7-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="c3fb7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3fb7-111">Description</span></span>      | <span data-ttu-id="c3fb7-112">Bietet Transportdienste über die IPX-Netzwerkebene: IPX für unzuverlässige Datagramme, SPX für zuverlässige, Verbindungs orientierte Nachrichtenströme.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="c3fb7-113">Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="c3fb7-113">Address family</span></span>   | <span data-ttu-id="c3fb7-114">AF- \_ IPX</span><span class="sxs-lookup"><span data-stu-id="c3fb7-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="c3fb7-115">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c3fb7-115">Header file</span></span>      | <span data-ttu-id="c3fb7-116">Wsipx. h</span><span class="sxs-lookup"><span data-stu-id="c3fb7-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="c3fb7-117">In diesem Abschnitt wird erläutert, wie Winsock mit der IPX-Familie von Protokollen verwendet wird, sodass herkömmliche IPX-Anwendungen in Winsock portiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="c3fb7-118">IPX-Netzwerke funktionieren in einer grundlegenden Weise als IP-Netzwerke, sodass solche Unterschiede bei der Verwendung von IPX/SPX berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



