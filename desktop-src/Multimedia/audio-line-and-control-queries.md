---
title: Audioline-und Steuerelement Abfragen
description: Audioline-und Steuerelement Abfragen
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- Multimedia-Audiosteuer Elemente
- Audiodaten, Mixer-Steuerelemente
- Audiomixer, audiolinien
- audiolinien
- Audiomischungen, Steuerelemente
- Mischungen, Steuerelemente
- Mixer, audiolinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725088"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="3e4dd-110">Audioline-und Steuerelement Abfragen</span><span class="sxs-lookup"><span data-stu-id="3e4dd-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="3e4dd-111">Die Mixer-Dienste stellen Funktionen zum Bestimmen von Informationen über audiolinien, audioliniensteuerelemente und Steuerelement Details bereit.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="3e4dd-112">Die Dienste stellen auch Funktionen zum Festlegen von Steuerungs Details bereit.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="3e4dd-113">Sie können die [**mixergetlineinfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) -Funktion verwenden, um Informationen zu einer angegebenen audiozeile abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="3e4dd-114">Diese Funktion füllt die [**mixerline**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) -Struktur für eine angegebene quellaudiozeile, eine zielaudiozeile oder einen Zeilen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="3e4dd-115">Die Struktur enthält die Ziel Zeilennummer, die Anzahl der Kanäle in der Audiolinie sowie einen kurzen und langen Namen für die Audiolinie.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="3e4dd-116">Die [**mixergetlinecontrols**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) -Funktion Ruft allgemeine Informationen zu einem oder mehreren Steuerelementen ab, die einer audiozeile zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="3e4dd-117">Diese Funktion füllt die [**mixerlinecontrols**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) -Struktur mit Informationen über das angegebene Steuerelement oder Steuerelemente aus.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="3e4dd-118">Sie können **mixergetlinecontrols** zum Abrufen von Steuerelement Eigenschaften für eine der folgenden Elemente verwenden:</span><span class="sxs-lookup"><span data-stu-id="3e4dd-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="3e4dd-119">Alle Steuerelemente für eine angegebene Quellzeile</span><span class="sxs-lookup"><span data-stu-id="3e4dd-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="3e4dd-120">Ein angegebenes Steuerelement für eine angegebene Quellzeile.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="3e4dd-121">Das erste Steuerelement einer bestimmten Klasse für eine angegebene Quellzeile.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="3e4dd-122">Die [**mixergetcontroldetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) -Funktion Ruft die Eigenschaften eines einzelnen Steuer Elements ab, das einer Audiolinie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="3e4dd-123">Diese Funktion füllt die [**mixercontroldetails**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) -Struktur mit den aktuellen Werten für ein Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="3e4dd-124">Die [**mixersetcontroldetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) -Funktion verwendet den Inhalt der **mixercontroldetails** -Struktur, um die Eigenschaften des angegebenen Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="3e4dd-125">Sie müssen sicherstellen, dass alle Elemente dieser Struktur ausgefüllt werden, bevor Sie **mixersetcontroldetails** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3e4dd-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 