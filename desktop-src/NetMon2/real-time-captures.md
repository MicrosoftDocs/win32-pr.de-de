---
description: Monitore empfangen erfasste Netzwerk Frames im Echtzeitmodus. Die Frames werden von einem Netzwerk Paketanbieter (NPP) mithilfe der-Schnittstelle "untc-com-Schnittstelle" erfasst und an den Monitor in einem der Monitore mit zwei Ausführungsthreads übermittelt.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Real-Time Erfassungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869032"
---
# <a name="real-time-captures"></a><span data-ttu-id="c3606-104">Real-Time Erfassungen</span><span class="sxs-lookup"><span data-stu-id="c3606-104">Real-Time Captures</span></span>

<span data-ttu-id="c3606-105">Monitore empfangen erfasste Netzwerk Frames im Echtzeitmodus.</span><span class="sxs-lookup"><span data-stu-id="c3606-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="c3606-106">Die Frames werden von einem [*Netzwerk Paketanbieter*](n.md) (NPP) mithilfe der-Schnittstelle des Anbieters " [untc](irtc.md) -com" aufgezeichnet und an den Monitor in einem der zwei Ausführungsthreads des Monitors übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c3606-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="c3606-107">Monitore können die Anzahl der zu verarbeitenden Rahmen beschränken, indem Sie einen [*Erfassungs Filter*](c.md) an den NPP übergeben, der die Frames bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c3606-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="c3606-108">In der Regel ist ein bestimmter Monitor auf bestimmte Arten von Datenverkehr, z. b. http, RIPX oder SMB, ausgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3606-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="c3606-109">Im Unterschied zu Experten, die anspruchsvolle Parser verwenden, um die zu analysierenden Informationen auszuwählen, muss ein Monitor jeden Frame auf die für die Erkennung vorgesehenen Bedingungen untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c3606-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="c3606-110">Der Grund für diese Frame-für-Frame-Methode ist die Leistung.</span><span class="sxs-lookup"><span data-stu-id="c3606-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="c3606-111">Ein Monitor muss seine Rahmen schnell genug verarbeiten, damit er nicht hinter den Treiber fällt, der die Frames an den NPP liefert.</span><span class="sxs-lookup"><span data-stu-id="c3606-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="c3606-112">Andernfalls gehen Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="c3606-112">Otherwise, data will be lost.</span></span>

 

 



