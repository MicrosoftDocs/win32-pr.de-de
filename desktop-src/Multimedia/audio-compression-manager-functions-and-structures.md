---
title: Funktionen und Strukturen des Audiokomprimierungs-Managers
description: Funktionen und Strukturen des Audiokomprimierungs-Managers
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- Multimedia-Audiofunktionen, ACM-Funktionen
- Audiofunktionen, ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- Multimedia-Audiodaten, ACM-Strukturen
- Audiodaten, ACM-Strukturen
- Audiokomprimierungs-Manager (ACM), Strukturen
- ACM (Audiokomprimierungs-Manager), Strukturen
- ACM-Strukturen
- ACM-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339055"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="66533-113">Funktionen und Strukturen des Audiokomprimierungs-Managers</span><span class="sxs-lookup"><span data-stu-id="66533-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="66533-114">Die ACM-Funktionen sind in verschiedene Kategorien unterteilt.</span><span class="sxs-lookup"><span data-stu-id="66533-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="66533-115">Benennungs Konventionen für die-Funktionen erleichtern die Identifizierung dieser Kategorien.</span><span class="sxs-lookup"><span data-stu-id="66533-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="66533-116">Funktionsnamen (mit zwei Ausnahmen) weisen die Form *acmgroupfunction* auf, wobei die *Gruppe* die ACM-Kategorie festlegt (z. b. "Driver", "Format", "Formattag", "Filter", "Filtertag" oder "Stream") und die *Funktion* die von der Funktion ausgeführte Aktion beschreibt.</span><span class="sxs-lookup"><span data-stu-id="66533-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="66533-117">Die Funktionen in den Filter-und Format Gruppen sind sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="66533-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="66533-118">Fast jede Funktion, die auf Filter angewendet wird, verfügt über eine parallele Funktion, die für Formate fungiert.</span><span class="sxs-lookup"><span data-stu-id="66533-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="66533-119">In der Format Gruppe verwenden einige Funktionen wellenformat-Audiotags (das **wformattag** -Element einer [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur), während andere die vollständigen wellenformat-Audioformate (die vollständige **WaveFormatEx** -Struktur) benötigen.</span><span class="sxs-lookup"><span data-stu-id="66533-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="66533-120">(Referenzinformationen zur **WaveFormatEx** -Struktur finden Sie unter [Error](error.md).)</span><span class="sxs-lookup"><span data-stu-id="66533-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="66533-121">In der Filter Gruppe verwenden einige Funktionen Waveform-audiofiltertags (das **dwfiltertag** -Element einer [**wavefilter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) -Struktur), während andere die vollständigen Wellenform-Audiofilter (die vollständige **Wellen Filter** Struktur) erfordern.</span><span class="sxs-lookup"><span data-stu-id="66533-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="66533-122">Die Funktionen in der streamgruppe stellen die vielen Schritte dar, die an einer Konvertierung beteiligt sind: das Öffnen einer Konvertierungs Instanz, das Vorbereiten der Konvertierung, das Ausführen der Konvertierung, das Bereinigen nach Abschluss der Konvertierung und das Schließen der Konvertierungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="66533-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 