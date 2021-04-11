---
title: Behandeln von Fehlern mit Audiofunktionen
description: Behandeln von Fehlern mit Audiofunktionen
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- Multimedia-Audiodaten, Waveform-Audiofehler
- Audiofehler, Waveform-Audiofehler
- Multimedia-Audiodaten, zusätzliche Audiofehler
- Audiofehler, zusätzliche Audiofehler
- Wellenform-Audiodaten, Fehler
- zusätzliches Audiomaterial, Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314786"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="33a11-109">Behandeln von Fehlern mit Audiofunktionen</span><span class="sxs-lookup"><span data-stu-id="33a11-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="33a11-110">Die Waveform-Audiofunktionen und hilfsaudiofunktionen geben einen Wert ungleich 0 (null) zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="33a11-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="33a11-111">Windows stellt Funktionen bereit, die diese Fehler Werte in Textbeschreibungen der Fehler konvertieren.</span><span class="sxs-lookup"><span data-stu-id="33a11-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="33a11-112">Die Anwendung muss die Fehler Werte weiterhin überprüfen, um zu bestimmen, wie der Vorgang fortgesetzt werden kann. Textbeschreibungen von Fehlern können jedoch in Dialogfeldern verwendet werden, in denen Benutzerfehler beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="33a11-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="33a11-113">Mit den folgenden Funktionen können Sie Textbeschreibungen von audiofehlerwerten abrufen:</span><span class="sxs-lookup"><span data-stu-id="33a11-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="33a11-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="33a11-114">Function</span></span>                                           | <span data-ttu-id="33a11-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33a11-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="33a11-116">**waveingeterrortext**</span><span class="sxs-lookup"><span data-stu-id="33a11-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="33a11-117">Ruft eine Textbeschreibung eines angegebenen Waveform-audioeingabefehlers ab.</span><span class="sxs-lookup"><span data-stu-id="33a11-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="33a11-118">**waveoutgeterrortext**</span><span class="sxs-lookup"><span data-stu-id="33a11-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="33a11-119">Ruft eine Textbeschreibung eines angegebenen Waveform-audioausgabefehlers ab.</span><span class="sxs-lookup"><span data-stu-id="33a11-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="33a11-120">Die einzigen Audiofunktionen, die keine Fehler Werte zurückgeben [**, sind "**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)" "" [](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)"" "" "" "" "" "" "" "" "" "" "" "" [**".**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)</span><span class="sxs-lookup"><span data-stu-id="33a11-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="33a11-121">Diese Funktionen geben 0 (null) zurück, wenn keine Geräte in einem System vorhanden sind oder wenn Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="33a11-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 