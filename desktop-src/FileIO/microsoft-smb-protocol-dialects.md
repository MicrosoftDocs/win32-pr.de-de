---
description: Zum Herstellen einer Verbindung zwischen einem Client und einem Server mithilfe des Microsoft SMB-Protokolls müssen Sie zunächst den Dialekt mit dem höchsten Grad an Funktionalität ermitteln, die sowohl vom Client als auch vom Server unterstützt werden.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Microsoft SMB-Protokoll Dialekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484731"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="cb26a-103">Microsoft SMB-Protokoll Dialekte</span><span class="sxs-lookup"><span data-stu-id="cb26a-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="cb26a-104">Die Liste der Microsoft SMB-Protokollnachrichten Pakete ist im Laufe der Jahre gewachsen, um die zunehmende Funktionalität des Microsoft SMB-Protokolls und nun die Anzahl der Hunderte zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="cb26a-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="cb26a-105">Jede Phase ihrer Vergrößerung wird durch einen Standardpaket Satz oder einen Dialekt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cb26a-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="cb26a-106">Jeder Dialekt wird durch eine Standard Zeichenfolge identifiziert, z. b. "PC-Netzwerkprogramm 1,0", "Microsoft Networks 3,0", "DOS LanMan 2,1" oder "NT LM 0,12".</span><span class="sxs-lookup"><span data-stu-id="cb26a-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="cb26a-107">Die erste Zeichenfolge identifiziert den ersten Dialekt von SMB, und die letzte Zeichenfolge identifiziert CIFS, den ersten Dialekt des Microsoft SMB-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="cb26a-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="cb26a-108">Die meisten Windows-Clients unterstützen mindestens sechs verschiedene Dialekte des Microsoft SMB-Protokolls. Daher besteht einer der ersten Schritte beim Herstellen einer Verbindung zwischen einem Client und einem Server mithilfe des Microsoft SMB-Protokolls darin, den Dialekt mit dem höchsten Grad an Funktionalität zu ermitteln, die sowohl vom Client als auch vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cb26a-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="cb26a-109">Dieser Prozess wird als "Aushandeln des Dialekts" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cb26a-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="cb26a-110">Die oben erwähnten Dialekt Zeichenfolgen sind zu diesem Zweck in den Dialekt Aushandlungs-Anforderungs-und Antwortpaketen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cb26a-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



