---
title: Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten
description: Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- Wellenform-Audiodaten, Rückruf Funktionen
- Audiodatenblöcke, Rückruf Funktionen
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Wavin Open-Funktion
- WaveOutOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341300"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="1682f-110">Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1682f-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="1682f-111">Sie können eine eigene Rückruffunktion schreiben, um Nachrichten zu verarbeiten, die vom Gerätetreiber gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1682f-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="1682f-112">Um eine Rückruffunktion zu verwenden, geben Sie das Rückruf \_ funktionsflag im Parameter *fdwopen* und die Adresse des Rückrufs im *dwcallback* -Parameter der [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion oder der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="1682f-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="1682f-113">An eine Rückruffunktion gesendete Nachrichten ähneln Nachrichten, die an ein Fenster gesendet werden, mit dem Unterschied, dass Sie anstelle eines **uint** -und **DWORD** -Parameters zwei **DWORD** -Parameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1682f-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="1682f-114">Ausführliche Informationen zu diesen Meldungen finden Sie unter wieder [Gabe Waveform-Audio Dateien](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="1682f-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="1682f-115">Verwenden Sie eine der folgenden Verfahren, um Instanzdaten von einer Anwendung an eine Rückruffunktion zu übergeben:</span><span class="sxs-lookup"><span data-stu-id="1682f-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="1682f-116">Übergeben Sie die Instanzdaten mit dem *dwinstance* -Parameter der Funktion, die den Gerätetreiber öffnet.</span><span class="sxs-lookup"><span data-stu-id="1682f-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="1682f-117">Übergeben Sie die Instanzdaten mit dem **DWUser** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die einen audiodatenblock identifiziert, der an einen Gerätetreiber gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1682f-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="1682f-118">Wenn Sie mehr als 32 Bits von Instanzdaten benötigen, übergeben Sie einen Zeiger auf eine-Struktur, die die zusätzlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="1682f-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 