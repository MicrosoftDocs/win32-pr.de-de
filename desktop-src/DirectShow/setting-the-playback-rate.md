---
description: Festlegen der Wiedergabe Rate
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Festlegen der Wiedergabe Rate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338849"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="5cb7a-103">Festlegen der Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="5cb7a-103">Setting the Playback Rate</span></span>

<span data-ttu-id="5cb7a-104">Um die Wiedergabe Rate zu ändern, rufen Sie die [**imediaseeking:: Server trate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="5cb7a-105">Geben Sie die neue Rate als Bruchteil der ursprünglichen Rate an.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="5cb7a-106">Verwenden Sie z. b. Folgendes, um die Geschwindigkeit mit zweimal normaler Geschwindigkeit wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="5cb7a-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="5cb7a-107">Die Sätze größer als 1 sind schneller als üblich.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="5cb7a-108">Die Raten zwischen null und eins sind langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="5cb7a-109">Negative Raten werden als Rückwärts Wiedergabe definiert, aber in der Praxis wird Sie von den meisten Filtern nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="5cb7a-110">Zurzeit unterstützt keiner der standardmäßigen DirectShow-Filter die umgekehrte Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="5cb7a-111">Unabhängig von der Wiedergabe Rate werden die aktuelle Position und die Position des Stopps immer relativ zur ursprünglichen Quelle ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="5cb7a-112">Wenn eine Quelldatei z. b. 20 Sekunden lang mit normaler Wiedergabe Rate ist, wird durch das Festlegen der aktuellen Position auf 10 Sekunden die Mitte der Datei gesucht.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="5cb7a-113">Wenn die Wiedergabe Rate den Wert 2,0 hat, die Endposition 20 Sekunden beträgt und Sie die 10-Sekunden-Position suchen, wird die Datei für 5 Sekunden der Echt Zeit wiedergegeben: 10 Sekunden, bei der doppelten Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="5cb7a-114">Bei einer Wiedergabe Rate von 2,0 erhöht sich die aktuelle Position um die doppelte Geschwindigkeit der Referenzuhr.</span><span class="sxs-lookup"><span data-stu-id="5cb7a-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



