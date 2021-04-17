---
title: Abfragen von MIDI-Geräten
description: Abfragen von MIDI-Geräten
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Digital Instrumentation Digital Interface (MIDI), Abfragen von Geräten
- MIDI (Digital Instrumentation Digital Interface), Abfragen von Geräten
- MIDI-Dienste, Abfragen von Geräten
- Abfragen von MIDI-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390183"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="2e4e0-107">Abfragen von MIDI-Geräten</span><span class="sxs-lookup"><span data-stu-id="2e4e0-107">Querying MIDI Devices</span></span>

<span data-ttu-id="2e4e0-108">Vor der Wiedergabe oder Aufzeichnung von MIDI-Daten müssen Sie die Funktionen der im System vorhandenen MIDI-Hardware ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="2e4e0-109">Die Funktionen von MIDI können von einem Multimedia-Computer bis zum nächsten abweichen. Anwendungen sollten keine Annahmen über die Hardware treffen, die in einem bestimmten System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="2e4e0-110">Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele MIDI-Geräte für die Eingabe oder Ausgabe in einem bestimmten System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="2e4e0-111">Wert</span><span class="sxs-lookup"><span data-stu-id="2e4e0-111">Value</span></span>                                          | <span data-ttu-id="2e4e0-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2e4e0-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="2e4e0-113">**midiingetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="2e4e0-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="2e4e0-114">Ruft die Anzahl der im System vorhandenen MIDI-Eingabegeräte ab.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="2e4e0-115">**midioutgetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="2e4e0-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="2e4e0-116">Ruft die Anzahl der im System vorhandenen Ausgabegeräte im System ab.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="2e4e0-117">Wie bei anderen Audiogeräten werden die MIDI-Geräte durch einen Geräte Bezeichner identifiziert, der implizit von der Anzahl der in einem bestimmten System vorhandenen Geräte bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="2e4e0-118">Geräte Bezeichner reichen von Null bis zur Anzahl der vorhandenen Geräte, minus 1.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="2e4e0-119">Wenn z. b. zwei MIDI-Ausgabegeräte in einem System vorhanden sind, sind gültige Geräte Bezeichner 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="2e4e0-120">Nachdem Sie festgelegt haben, wie viele Eingabe-oder Ausgabegeräte in einem System vorhanden sind, können Sie sich über die Funktionen der einzelnen Geräte informieren.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="2e4e0-121">Windows stellt die folgenden Funktionen bereit, um die Funktionen von Audiogeräten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="2e4e0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2e4e0-122">Value</span></span>                                          | <span data-ttu-id="2e4e0-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2e4e0-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e4e0-124">**midiingetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="2e4e0-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="2e4e0-125">Ruft die Funktionen eines angegebenen MIDI-Eingabe Geräts ab und platziert diese Informationen in der [**midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="2e4e0-126">**midioutgetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="2e4e0-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="2e4e0-127">Ruft die Funktionen eines angegebenen Ausgabegeräts von MIDI ab und platziert diese Informationen in der [**midioutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="2e4e0-128">Jede dieser Funktionen verfügt über einen Parameter, der die Adresse einer Struktur angibt, die die Funktion mit Informationen zu den Funktionen eines bestimmten Geräts füllt.</span><span class="sxs-lookup"><span data-stu-id="2e4e0-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e4e0-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2e4e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e4e0-130">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="2e4e0-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 