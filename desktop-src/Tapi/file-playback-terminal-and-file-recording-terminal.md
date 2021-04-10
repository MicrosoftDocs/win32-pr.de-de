---
description: Das Terminal für die Dateiwiedergabe und das Datei Aufzeichnungs Terminal machen die Schnittstellen itterminal und itmultitrackterminal verfügbar. Diese Objekte machen außerdem die itmediacontrol-Schnittstelle verfügbar, die Methoden für das Beenden, starten und die Medien Navigation bereitstellt.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal Dateiwiedergabe Terminal und Datei Aufzeichnungs Terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959716"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="cb636-104">Terminal Dateiwiedergabe Terminal und Datei Aufzeichnungs Terminal</span><span class="sxs-lookup"><span data-stu-id="cb636-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="cb636-105">Das Terminal für die Dateiwiedergabe und das Datei Aufzeichnungs Terminal machen die Schnittstellen [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) und [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb636-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="cb636-106">Diese Objekte machen außerdem die [**itmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) -Schnittstelle verfügbar, die Methoden für das Beenden, starten und die Medien Navigation bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb636-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="cb636-107">Das Terminal für die Dateiwiedergabe macht die [**itmediaplayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) -Schnittstelle verfügbar, die über Wiedergabe spezifische Methoden verfügt.</span><span class="sxs-lookup"><span data-stu-id="cb636-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="cb636-108">Das Datei Aufzeichnungs Terminal macht die [**itmediarecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) -Schnittstelle verfügbar, die Aufzeichnungs spezifische Methoden bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb636-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="cb636-109">Bei [Multitrack-Terminals](multitrack-terminals.md)verwalten das Terminal für die Datei Aufzeichnung und das Dateiwiedergabe Terminal jeweils eine Sammlung von nach [Verfolgung von Terminals](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="cb636-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
