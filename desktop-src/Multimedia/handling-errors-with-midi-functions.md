---
title: Behandeln von Fehlern mit MIDI-Funktionen
description: Behandeln von Fehlern mit MIDI-Funktionen
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Digital Instrumentation Digital Interface (MIDI), Fehler
- MIDI (Digital Interface Digital Interface), Fehler
- MIDI-Dienste, Fehler
- MIDI-Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340270"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="54f01-107">Behandeln von Fehlern mit MIDI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="54f01-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="54f01-108">Die Funktionen von MIDI-Audiofunktionen geben einen Fehlercode ungleich NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="54f01-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="54f01-109">Bei Fehlern, die mit einem Fehler in einem Zusammenhang mit einem Fehler in einem Fehlercode auftreten, rufen die Funktionen [**midiingeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) und [**midioutgeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) die Textbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="54f01-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="54f01-110">Die Anwendung muss weiterhin den Fehlerwert selbst überprüfen, um zu bestimmen, wie der Vorgang fortgesetzt werden kann. Sie kann jedoch die Fehlerbeschreibungen in Dialogfeldern verwenden, um Benutzer über die Fehlerbedingungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="54f01-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="54f01-111">Die einzigen MIDI-Funktionen, die keine Fehlercodes zurückgeben, sind die Funktionen [**midiingetnumdevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) und [**midioutgetnumdevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="54f01-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="54f01-112">Diese Funktionen geben den Wert 0 (null) zurück, wenn keine Geräte in einem System vorhanden sind oder wenn von der Funktion Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="54f01-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54f01-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54f01-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54f01-114">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="54f01-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 