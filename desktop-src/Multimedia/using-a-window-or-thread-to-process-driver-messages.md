---
title: Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten
description: Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- Wellenform-Audiodatei, Fenster Rückruf
- Audiodatenblöcke, Fenster Rückruf
- Wellenform-Audiodatei, Thread Rückruf
- Audiodatenblöcke, Thread Rückruf
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Wavin Open-Funktion
- WaveOutOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948735"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="35fd2-112">Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="35fd2-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="35fd2-113">Um eine Fenster Rückruffunktion zu verwenden, geben Sie das Rückruf \_ Fenster-Flag im *fdwopen* -Parameter und ein Fenster Handle im nieder wertigen Wort des *dwcallback* -Parameters der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion oder der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="35fd2-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="35fd2-114">Treiber Meldungen werden an die Fenster Prozedur für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="35fd2-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="35fd2-115">Um einen Thread Rückruf zu verwenden, geben Sie auch \_ den Rückruf Thread und ein Thread Handle im Aufrufs von **waveinopen** oder **WaveOutOpen** an.</span><span class="sxs-lookup"><span data-stu-id="35fd2-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="35fd2-116">In diesem Fall werden Nachrichten anstelle eines Fensters an den angegebenen Thread gesendet.</span><span class="sxs-lookup"><span data-stu-id="35fd2-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="35fd2-117">Nachrichten, die an den Fenster-oder Thread Rückruf gesendet werden, sind spezifisch für den verwendeten audiogerätetyp.</span><span class="sxs-lookup"><span data-stu-id="35fd2-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="35fd2-118">Weitere Informationen zu diesen Meldungen finden Sie unter wieder [Gabe Waveform-Audio Dateien](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="35fd2-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 