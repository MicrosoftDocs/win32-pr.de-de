---
title: Verwalten von Datenblöcken durch Abrufen
description: Verwalten von Datenblöcken durch Abrufen
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- Wellenform-Audiodaten, Abrufen von Datenblöcken
- Audiodatenblöcke, Abrufen
- Abrufen von audiodatenblöcken
- Wavehdr-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038851"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="69975-107">Verwalten von Datenblöcken durch Abrufen</span><span class="sxs-lookup"><span data-stu-id="69975-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="69975-108">Zusätzlich zur Verwendung einer Rückruffunktion können Sie den **dwFlags** -Member einer [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur Abfragen, um zu bestimmen, wann ein Audiogerät mit einem Datenblock fertig ist.</span><span class="sxs-lookup"><span data-stu-id="69975-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="69975-109">Manchmal ist es besser, **dwFlags** abzufragen, als auf einen anderen Mechanismus zum Empfangen von Nachrichten von den Treibern zu warten.</span><span class="sxs-lookup"><span data-stu-id="69975-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="69975-110">Nachdem Sie z. b. die [**waveoutset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion zum Freigeben von ausstehenden Datenblöcken aufgerufen haben, können Sie sofort Abfragen, um sicherzustellen, dass die Datenblöcke freigegeben wurden, bevor Sie [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) aufrufen und den Arbeitsspeicher für den Datenblock freigeben.</span><span class="sxs-lookup"><span data-stu-id="69975-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="69975-111">Sie können das whdr \_ done-Flag verwenden, um **den dwFlags** -Member zu testen.</span><span class="sxs-lookup"><span data-stu-id="69975-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="69975-112">Sobald das Flag "whdr \_ Done" im **dwFlags** -Member der **wavehdr** -Struktur festgelegt ist, wird der Treiber mit dem Datenblock beendet.</span><span class="sxs-lookup"><span data-stu-id="69975-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 