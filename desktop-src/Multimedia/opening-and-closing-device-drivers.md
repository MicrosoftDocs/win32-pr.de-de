---
title: Öffnen und Schließen von Gerätetreibern
description: Öffnen und Schließen von Gerätetreibern
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Digital Instrumentation Digital Interface (MIDI), Öffnen von Geräten
- MIDI (Digital Instrumentation Digital Interface), Öffnen von Geräten
- MIDI-Dienste, Öffnen von Geräten
- Öffnen von MIDI-Geräten
- Digital Instrumentation Digital Interface (MIDI), schließen von Geräten
- MIDI (Digital Instrumentation Digital Interface), schließen von Geräten
- MIDI-Dienste, schließen von Geräten
- Schließen von MIDI-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725080"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="4be95-111">Öffnen und Schließen von Gerätetreibern</span><span class="sxs-lookup"><span data-stu-id="4be95-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="4be95-112">Sie müssen ein MIDI-Gerät öffnen, bevor Sie es verwenden können, und Sie sollten das Gerät schließen, sobald Sie es verwenden.</span><span class="sxs-lookup"><span data-stu-id="4be95-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="4be95-113">Windows bietet die folgenden Funktionen, um unterschiedliche Arten von MIDI-Geräten zu öffnen und zu schließen.</span><span class="sxs-lookup"><span data-stu-id="4be95-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="4be95-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4be95-114">Value</span></span>                                | <span data-ttu-id="4be95-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4be95-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="4be95-116">**midiinclose**</span><span class="sxs-lookup"><span data-stu-id="4be95-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="4be95-117">Schließt ein angegebenes MIDI-Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="4be95-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="4be95-118">**midiinopen**</span><span class="sxs-lookup"><span data-stu-id="4be95-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="4be95-119">Öffnet ein angegebenes MIDI-Eingabegerät für die Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="4be95-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="4be95-120">**midioutclose**</span><span class="sxs-lookup"><span data-stu-id="4be95-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="4be95-121">Schließt ein angegebenes MIDI-Ausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="4be95-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="4be95-122">**midioutopen**</span><span class="sxs-lookup"><span data-stu-id="4be95-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="4be95-123">Öffnet ein MIDI-Ausgabegerät für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="4be95-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="4be95-124">Jede Funktion, die ein MIDI-Gerät öffnet, benötigt als Parameter einen Geräte Bezeichner, eine Adresse eines Speicher Orts und einige Parameter, die für die Verwendung von MIDI-Geräten eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="4be95-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="4be95-125">Der Speicherort wird mit einem Geräte handle gefüllt, das verwendet wird, um das geöffnete Audiogerät in Aufrufen von anderen Audiofunktionen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4be95-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="4be95-126">Viele MIDI-Funktionen können entweder ein Geräte handle oder einen Geräte Bezeichner akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4be95-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="4be95-127">Obwohl Sie ein Geräte handle überall dort verwenden können, wo Sie einen Geräte Bezeichner verwenden würden, können Sie nicht immer einen Geräte Bezeichner verwenden, wenn ein Handle für aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4be95-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="4be95-128">Bei der Erstellung von MIDI-Geräten ist es nicht zwingend möglich, dass ein bestimmtes Gerät nicht verfügbar ist, wenn ein Benutzer es anfordert.</span><span class="sxs-lookup"><span data-stu-id="4be95-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="4be95-129">In diesem Fall sollte die Anwendung den Benutzer benachrichtigen und dem Benutzer gestatten, das Gerät erneut zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4be95-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4be95-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4be95-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be95-131">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="4be95-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 