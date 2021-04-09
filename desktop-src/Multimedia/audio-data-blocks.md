---
title: Audiodatenblöcke
description: Audiodatenblöcke
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- Multimedia-Audiodaten, Datenblöcke
- Audiodaten, Datenblöcke
- Wellenform-Audiodaten, Datenblöcke
- Audiodatenblöcke, Informationen zu
- Wavehdr-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948627"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="6393e-108">Audiodatenblöcke</span><span class="sxs-lookup"><span data-stu-id="6393e-108">Audio Data Blocks</span></span>

<span data-ttu-id="6393e-109">Die Funktionen [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) und [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) erfordern, dass Anwendungen Datenblöcke zuordnen, die zu Aufzeichnungs-oder Wiedergabe Zwecken an die Gerätetreiber übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6393e-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="6393e-110">Beide Funktionen verwenden die [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, um den zugehörigen Datenblock zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6393e-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="6393e-111">Bevor Sie eine dieser Funktionen verwenden können, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie für den Datenblock und die Header Struktur, die den Datenblock beschreibt, Arbeitsspeicher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6393e-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="6393e-112">Die Header können mithilfe der folgenden Funktionen vorbereitet und nicht vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="6393e-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="6393e-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="6393e-113">Function</span></span>                                                 | <span data-ttu-id="6393e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6393e-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="6393e-115">**wavone prepareheader**</span><span class="sxs-lookup"><span data-stu-id="6393e-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="6393e-116">Bereitet einen Eingabedaten Block mit Waveform-Audiodaten vor.</span><span class="sxs-lookup"><span data-stu-id="6393e-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="6393e-117">**waveingeunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="6393e-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="6393e-118">Bereinigt die Vorbereitung auf einem Datenblock mit Waveform-Audioeingabe.</span><span class="sxs-lookup"><span data-stu-id="6393e-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="6393e-119">**waveoutprepareheader**</span><span class="sxs-lookup"><span data-stu-id="6393e-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="6393e-120">Bereitet einen "Waveform-Audioausgabe"-Ausgabedaten Block vor.</span><span class="sxs-lookup"><span data-stu-id="6393e-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="6393e-121">**waveoutunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="6393e-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="6393e-122">Bereinigt die Vorbereitung für einen Waveform-audioausgabedatenblock.</span><span class="sxs-lookup"><span data-stu-id="6393e-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="6393e-123">Bevor Sie einen audiodatenblock an einen Gerätetreiber übergeben, müssen Sie den Datenblock vorbereiten, indem Sie ihn entweder an [**waveingeprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) oder [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)übergeben.</span><span class="sxs-lookup"><span data-stu-id="6393e-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="6393e-124">Wenn der Gerätetreiber mit dem Datenblock fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigen, indem Sie den Datenblock entweder an [**waveinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) oder [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) übergeben, bevor zugeordneter Arbeitsspeicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6393e-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="6393e-125">Wenn die Eingabe-und Ausgabedaten des Waveform-Audiodaten klein genug sind, um in einem einzelnen Datenblock enthalten zu sein, müssen Anwendungen den Gerätetreiber kontinuierlich mit Datenblöcken bereitstellen, bis die Wiedergabe oder Aufzeichnung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6393e-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="6393e-126">Selbst wenn ein einzelner Datenblock verwendet wird, muss eine Anwendung in der Lage sein, zu bestimmen, wann ein Gerätetreiber mit dem Datenblock fertig ist, damit die Anwendung den dem Datenblock und der Header Struktur zugeordneten Arbeitsspeicher freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="6393e-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="6393e-127">Es gibt mehrere Möglichkeiten, um zu bestimmen, wann ein Gerätetreiber mit einem Datenblock fertiggestellt ist:</span><span class="sxs-lookup"><span data-stu-id="6393e-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="6393e-128">Durch Angeben einer Rückruffunktion zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn er mit einem Datenblock fertig ist</span><span class="sxs-lookup"><span data-stu-id="6393e-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="6393e-129">Mithilfe eines Ereignis Rückrufs</span><span class="sxs-lookup"><span data-stu-id="6393e-129">By using an event callback</span></span>
-   <span data-ttu-id="6393e-130">Durch Angeben eines Fensters oder Threads zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn er mit einem Datenblock fertig ist</span><span class="sxs-lookup"><span data-stu-id="6393e-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="6393e-131">Durch Abrufen des Bits "whdr \_ Done" im **dwFlags** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die mit jedem Datenblock gesendet wird</span><span class="sxs-lookup"><span data-stu-id="6393e-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="6393e-132">Wenn eine Anwendung bei Bedarf keinen Datenblock für den Gerätetreiber erhält, kann es eine akustische Lücke bei der Wiedergabe oder einen Verlust eingehender aufgezeichneter Informationen geben.</span><span class="sxs-lookup"><span data-stu-id="6393e-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="6393e-133">Hierfür ist mindestens ein doppeltes Puffer Schema erforderlich – mindestens ein Datenblock vor dem Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="6393e-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="6393e-134">In den folgenden Themen wird beschrieben, wie Sie bestimmen können, wann ein Gerätetreiber mit einem-Datenblock fertig ist:</span><span class="sxs-lookup"><span data-stu-id="6393e-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="6393e-135">Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6393e-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="6393e-136">Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6393e-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="6393e-137">Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6393e-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="6393e-138">Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6393e-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="6393e-139">Verwalten von Datenblöcken durch Abrufen</span><span class="sxs-lookup"><span data-stu-id="6393e-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 