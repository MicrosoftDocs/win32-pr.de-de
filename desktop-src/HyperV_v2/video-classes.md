---
description: Alle virtuellen Computer spiegeln das vorhanden sein eines emulierten S3-Video Controllers und eines beschleunigten, synthetischen Video Controllers wider.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Video Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485694"
---
# <a name="video-classes"></a><span data-ttu-id="72744-103">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="72744-103">Video classes</span></span>

<span data-ttu-id="72744-104">Alle virtuellen Computer spiegeln das vorhanden sein eines emulierten S3-Video Controllers und eines beschleunigten, synthetischen Video Controllers wider.</span><span class="sxs-lookup"><span data-stu-id="72744-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="72744-105">Jedem Anzeige Controller ist ein Video Head-Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="72744-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="72744-106">Auf einem virtuellen Computer kann zu einem beliebigen Zeitpunkt nur ein Anzeige Controller aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="72744-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="72744-107">Für jede aktive Remote Sitzung, die mit einem virtuellen Computer verbunden ist, ist eine Terminal Verbindung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="72744-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="72744-108">Im folgenden finden Sie WMI-Klassen für die Virtualisierung im Zusammenhang mit Videos.</span><span class="sxs-lookup"><span data-stu-id="72744-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72744-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="72744-109">In this section</span></span>



| <span data-ttu-id="72744-110">Thema</span><span class="sxs-lookup"><span data-stu-id="72744-110">Topic</span></span>                                                                                  | <span data-ttu-id="72744-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72744-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72744-112">**MSVM \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="72744-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="72744-113">Stellt den Zustand des emulierten S3-Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="72744-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="72744-114">**MSVM \_ syntheticdisplaycontroller**</span><span class="sxs-lookup"><span data-stu-id="72744-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="72744-115">Stellt den Status des synthetischen Anzeige Controllers dar, der in jeder Konfiguration der virtuellen Maschine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="72744-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="72744-116">**MSVM \_ systemterminalconnection**</span><span class="sxs-lookup"><span data-stu-id="72744-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="72744-117">Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.</span><span class="sxs-lookup"><span data-stu-id="72744-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="72744-118">**MSVM \_ terminalconnection**</span><span class="sxs-lookup"><span data-stu-id="72744-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="72744-119">Gibt den Status einer aktiven Remote Sitzung an, die mit einer virtuellen Maschine interagiert.</span><span class="sxs-lookup"><span data-stu-id="72744-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="72744-120">**MSVM- \_ videohead**</span><span class="sxs-lookup"><span data-stu-id="72744-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="72744-121">Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.</span><span class="sxs-lookup"><span data-stu-id="72744-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="72744-122">**MSVM \_ videoheadoncontroller**</span><span class="sxs-lookup"><span data-stu-id="72744-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="72744-123">Ordnet einen Video Kopf dem Videocontroller zu, der ihn enthält.</span><span class="sxs-lookup"><span data-stu-id="72744-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




