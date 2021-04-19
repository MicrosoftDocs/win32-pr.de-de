---
description: TAPI 3,1 führt das Konzept eines Multitrack-Terminals ein, ein Terminal, das im Wesentlichen eine Sammlung von &\# 0034, Track&\# 0034; Terminals ist.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Multitrack-Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348819"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="bf6b9-103">Multitrack-Terminals</span><span class="sxs-lookup"><span data-stu-id="bf6b9-103">Multitrack Terminals</span></span>

<span data-ttu-id="bf6b9-104">TAPI 3,1 führt das Konzept eines Multitrack-Terminals ein, ein Terminal, bei dem es sich im Wesentlichen um eine Sammlung von "Track"-Terminals handelt.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="bf6b9-105">Multitrack-Terminals vereinfachen die Auslastung des Programmierers in Situationen, in denen mehrere Medienströme an einer Kommunikationssitzung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="bf6b9-106">Das [Datei Aufzeichnungs Terminal](file-playback-terminal-and-file-recording-terminal.md) ist ein Beispiel für ein Multitrack-Terminal.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="bf6b9-107">Er besteht aus "Track", wobei jeder "Track" ein Terminal ist, das einem Stream in der aufgezeichneten Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="bf6b9-108">Ein [Track-Terminal](track-terminals.md) kann ein anderes Multitrack-Terminal oder ein Single-Track-Terminal sein.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="bf6b9-109">Ein Single-Track-Terminal ist ein Terminal, das keine Nachverfolgung von Terminals hat.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="bf6b9-110">Ein Single-Track-Terminal ist ein Terminal im TAPI 3-Sinne des Worts.</span><span class="sxs-lookup"><span data-stu-id="bf6b9-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="bf6b9-111">Weitere Informationen zu Multitrack-Terminals finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="bf6b9-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="bf6b9-112">Informationen zu Multitrack-Terminals</span><span class="sxs-lookup"><span data-stu-id="bf6b9-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="bf6b9-113">Standardmäßiger Terminal Auswahlmechanismus</span><span class="sxs-lookup"><span data-stu-id="bf6b9-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="bf6b9-114">Manuelle Terminal Auswahl</span><span class="sxs-lookup"><span data-stu-id="bf6b9-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="bf6b9-115">Verwenden von Multitrack-Terminals und dem Standardauswahl Mechanismus</span><span class="sxs-lookup"><span data-stu-id="bf6b9-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



