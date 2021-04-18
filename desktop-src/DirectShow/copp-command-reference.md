---
description: COPP-Befehlsreferenz
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: COPP-Befehlsreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dfeebe42b877604ab880ef1855035242d6eca8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343952"
---
# <a name="copp-command-reference"></a><span data-ttu-id="54cc7-103">COPP-Befehlsreferenz</span><span class="sxs-lookup"><span data-stu-id="54cc7-103">COPP Command Reference</span></span>

<span data-ttu-id="54cc7-104">In diesem Abschnitt werden die Befehle des Certified Output Protection Protocol (COPP) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="54cc7-104">This section describes the Certified Output Protection Protocol (COPP) commands.</span></span> <span data-ttu-id="54cc7-105">Die folgenden Befehle sind definiert.</span><span class="sxs-lookup"><span data-stu-id="54cc7-105">The following commands are defined.</span></span>



| <span data-ttu-id="54cc7-106">Get-Help</span><span class="sxs-lookup"><span data-stu-id="54cc7-106">Command</span></span>              | <span data-ttu-id="54cc7-107">GUID</span><span class="sxs-lookup"><span data-stu-id="54cc7-107">GUID</span></span>                             |
|----------------------|----------------------------------|
| <span data-ttu-id="54cc7-108">Schutz Ebene festlegen</span><span class="sxs-lookup"><span data-stu-id="54cc7-108">Set Protection Level</span></span> | <span data-ttu-id="54cc7-109">**DXVA- \_ coppsetschutzlevel**</span><span class="sxs-lookup"><span data-stu-id="54cc7-109">**DXVA\_COPPSetProtectionLevel**</span></span> |
| <span data-ttu-id="54cc7-110">Signalisierung festlegen</span><span class="sxs-lookup"><span data-stu-id="54cc7-110">Set Signaling</span></span>        | <span data-ttu-id="54cc7-111">**DXVA- \_ coppsetsignalisierung**</span><span class="sxs-lookup"><span data-stu-id="54cc7-111">**DXVA\_COPPSetSignaling**</span></span>       |



 

<span data-ttu-id="54cc7-112">Befehl zum Festlegen der Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="54cc7-112">Set Protection Level Command</span></span>

<span data-ttu-id="54cc7-113">Legt die Schutz Ebene für einen angegebenen Ausgabe Schutzmechanismus fest.</span><span class="sxs-lookup"><span data-stu-id="54cc7-113">Sets the protection level for a specified output protection mechanism.</span></span> <span data-ttu-id="54cc7-114">Abhängig vom Connector ist es möglicherweise möglich, mehr als einen Schutzmechanismus auf demselben Connector mit unterschiedlichen Einstellungen für jeden Mechanismus anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="54cc7-114">Depending on the connector, it might be possible to apply more than one protection mechanism on the same connector, with different settings for each mechanism.</span></span>

<span data-ttu-id="54cc7-115">**GUID**: DXVA- \_ coppsetschutzlevel</span><span class="sxs-lookup"><span data-stu-id="54cc7-115">**GUID**: DXVA\_COPPSetProtectionLevel</span></span>

<span data-ttu-id="54cc7-116">**Eingabedaten**: eine [**DXVA-Struktur " \_ coppsetschutzlevelcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) ".</span><span class="sxs-lookup"><span data-stu-id="54cc7-116">**Input data**: A [**DXVA\_COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) structure.</span></span>

<span data-ttu-id="54cc7-117">Signalisierungs Befehl festlegen</span><span class="sxs-lookup"><span data-stu-id="54cc7-117">Set Signaling Command</span></span>

<span data-ttu-id="54cc7-118">Gibt Informationen zum anderen Videosignal als der Schutz Ebene an.</span><span class="sxs-lookup"><span data-stu-id="54cc7-118">Specifies information about the video signal other than the protection level.</span></span>

<span data-ttu-id="54cc7-119">Für CGMS-A erfordern bestimmte Schutzstandards, dass das Televsion-Signalinformationen über das Seitenverhältnis und andere Informationen in denselben VBI-Wellenform-Paketen wie die CGMS-a-Bits enthält.</span><span class="sxs-lookup"><span data-stu-id="54cc7-119">For CGMS-A, certain protection standards require that the televsion signal contains information about the aspect ratio and other information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="54cc7-120">Fernsehgeräte können schlecht angezeigt werden, wenn die Seitenverhältnis Informationen nicht mit dem Videostream konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="54cc7-120">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="54cc7-121">Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, damit der Grafiktreiber die richtigen VBI-Pakete generieren kann.</span><span class="sxs-lookup"><span data-stu-id="54cc7-121">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

<span data-ttu-id="54cc7-122">Dieser Befehl ist auch erweiterbar, wenn in zukünftigen Standards zusätzliche Signalinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="54cc7-122">This command is also designed to be extensible if additional signal information is required in future standards.</span></span>

<span data-ttu-id="54cc7-123">**GUID**: DXVA- \_ coppsetsignalisierung</span><span class="sxs-lookup"><span data-stu-id="54cc7-123">**GUID**: DXVA\_COPPSetSignaling</span></span>

<span data-ttu-id="54cc7-124">**Eingabedaten**: eine [**DXVA-Struktur " \_ coppsetsignalingcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) ".</span><span class="sxs-lookup"><span data-stu-id="54cc7-124">**Input data**: A [**DXVA\_COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54cc7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54cc7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54cc7-126">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="54cc7-126">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



