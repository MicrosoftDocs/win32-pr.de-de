---
description: Nachdem sich ein-Rückruf im verbundenen Zustand befindet, kann er über ihn übermittelt werden.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Erstellen von Inband-Ziffern und-Tönen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354446"
---
# <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="2f435-103">Erstellen von Inband-Ziffern und-Tönen</span><span class="sxs-lookup"><span data-stu-id="2f435-103">Generating Inband Digits and Tones</span></span>

<span data-ttu-id="2f435-104">Nachdem sich ein-Rückruf im *verbundenen* Zustand befindet, kann er über ihn übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="2f435-104">After a call is in the *connected* state, information can be transmitted over it.</span></span> <span data-ttu-id="2f435-105">Es werden zwei Funktionen bereitgestellt, die eine End-to-End-Inband-Signalisierung zwischen der Anwendung und den Remote Stations Geräten ermöglichen, z. b</span><span class="sxs-lookup"><span data-stu-id="2f435-105">Two functions are provided that allow end-to-end inband signaling between the application and remote station equipment such as an answering machine.</span></span> <span data-ttu-id="2f435-106">Eine Funktion ist " [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)", die bei einem Anruf inbandziffern generiert und diese über den voicechannel signalisiert.</span><span class="sxs-lookup"><span data-stu-id="2f435-106">One function is [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), which generates inband digits on a call, signaling them over the voice channel.</span></span> <span data-ttu-id="2f435-107">Ziffern können als Zeichen folgen oder als DTMF-Töne signalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2f435-107">Digits can be signaled as either rotary/pulse sequences or as DTMF tones.</span></span> <span data-ttu-id="2f435-108">Die andere Funktion ist " [**linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)", die es der Anwendung ermöglicht, eine Vielzahl von mehr Frequenz Tönen (über den Mediendaten Strom) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2f435-108">The other function is [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), which enables the application to generate one of a variety of multifrequency tones inband (over the media stream).</span></span> <span data-ttu-id="2f435-109">Dadurch werden telefonietöne, wie z. b. "Ringback", "Beep" und "ausgelastet", sowie beliebige Multifrequenz-, multikad-Töne erzeugt.</span><span class="sxs-lookup"><span data-stu-id="2f435-109">This generates telephony tones, such as ringback, beep, and busy, as well as arbitrary multifrequency, multicadenced tones.</span></span>

<span data-ttu-id="2f435-110">Nur eine Ziffern-oder Tongenerierung kann bei einem Aufruf zu einem beliebigen Zeitpunkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2f435-110">Only one digit or tone generation can be in progress on a call at any one time.</span></span> <span data-ttu-id="2f435-111">Wenn die Ziffern-oder Tongenerierung abgeschlossen ist, wird eine [**Zeile zum \_ Generieren von Zeilen**](line-generate.md) an die Anwendung gesendet, die die Generierung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="2f435-111">When digit or tone generation completes, a [**LINE\_GENERATE**](line-generate.md) message is sent to the application that requested the generation.</span></span> <span data-ttu-id="2f435-112">Wenn mehrere Ziffern generiert werden, wird nur eine einzelne Nachricht zurückgesendet, nachdem alle Ziffern generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2f435-112">In the case where multiple digits are generated, only a single message is sent back after all digits have been generated.</span></span> <span data-ttu-id="2f435-113">Beim Aufrufen von [**linegeneratedigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) oder [**linegeneratetone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) während der Ziffern-oder Tongenerierung wird die Generierung abgebrochen, und die Zeile zum \_ generieren der Nachricht wird an die Anwendung gesendet, deren Generierung mit einer Abbruch Angabe abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="2f435-113">Calling [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) or [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) while digit or tone generation is in progress will abort the generation currently in progress and send the LINE\_GENERATE message to the application whose generation was aborted with a cancel indication.</span></span>

 

 



