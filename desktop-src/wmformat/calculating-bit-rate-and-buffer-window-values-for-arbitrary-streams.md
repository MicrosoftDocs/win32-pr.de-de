---
title: Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams
description: Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- Streams, Bitraten
- Codecs, berechnen von Bitraten für beliebige Streams
- Bitraten, berechnen für beliebige Streams
- Streams, berechnen von Bitraten für beliebige Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036388"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a><span data-ttu-id="c7a89-107">Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams</span><span class="sxs-lookup"><span data-stu-id="c7a89-107">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>

<span data-ttu-id="c7a89-108">Das Berechnen der richtigen Bitrate und des Puffer Fensters für einen beliebigen Streamtyp ist keine exakte Wissenschaft.</span><span class="sxs-lookup"><span data-stu-id="c7a89-108">Calculating the proper bit rate and buffer window for an arbitrary stream type is not an exact science.</span></span> <span data-ttu-id="c7a89-109">Ein einfacher Ansatz ist die Festlegung der Bitrate entsprechend der Größe des Streams dividiert durch die Länge in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c7a89-109">One simple approach is to set the bit rate to match the size of the stream divided by its length, in seconds.</span></span> <span data-ttu-id="c7a89-110">Beispielsweise kann ein Datenstrom, der insgesamt 68000 Bits mit einer Dauer von 20 Sekunden enthält, eine Bitrate von 3400 Bits pro Sekunde aufweisen (68000 Bits/20 Sekunden = 3400 Bits pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="c7a89-110">For example, a stream containing a total of 68000 bits lasting 20 seconds might have a bit rate of 3400 bits per second (68000 bits / 20 seconds = 3400 bits per second).</span></span>

<span data-ttu-id="c7a89-111">Das Problem bei dieser einfachen Methode zum Zuweisen der Bitrate besteht darin, dass die Verteilung der Daten innerhalb des Streams nicht berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7a89-111">The problem with this simple technique of assigning bit rate is that it does not take into account the distribution of data within the stream.</span></span> <span data-ttu-id="c7a89-112">Viele beliebige Streams enthalten größere Datenmengen in Intervallen entlang der Zeitachse der Datei.</span><span class="sxs-lookup"><span data-stu-id="c7a89-112">Many arbitrary streams contain larger amounts of data at intervals along the timeline of the file.</span></span> <span data-ttu-id="c7a89-113">Bild Datenströme verfügen z. b. über Beispiele, die recht groß sind, aber in der Regel mehrere Sekunden voneinander entfernt sind.</span><span class="sxs-lookup"><span data-stu-id="c7a89-113">Image streams, for example, have samples that are rather large, but are usually spaced several seconds apart.</span></span> <span data-ttu-id="c7a89-114">Das Puffer Fenster muss festgelegt werden, um sicherzustellen, dass der Puffer keinen Überlauf verursacht.</span><span class="sxs-lookup"><span data-stu-id="c7a89-114">The buffer window must be set to ensure that the buffer will not overflow.</span></span>

<span data-ttu-id="c7a89-115">Um das Puffer Fenster zu überprüfen, Multiplizieren Sie die Bitrate (Bits pro Sekunde) mit dem Puffer Fenster (in Sekunden), und teilen Sie durch 1000, um die Größe des Puffers für den Datenstrom in Bits zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7a89-115">To check the buffer window, multiply the bit rate (bits per second) by the buffer window (in seconds) and divide by 1000 to get the size, in bits, of the buffer for the stream.</span></span> <span data-ttu-id="c7a89-116">Stellen Sie dann sicher, dass die Puffergröße groß genug ist, um eine beliebige Kombination von Beispielen im Stream aufzunehmen, die kleiner sind als das Puffer Fenster, das in der Präsentationszeit abweicht.</span><span class="sxs-lookup"><span data-stu-id="c7a89-116">Then make sure that the buffer size is large enough to hold any combination of samples in the stream that are less than the buffer window apart in presentation time.</span></span> <span data-ttu-id="c7a89-117">Legen Sie im Zweifelsfall beide Werte etwas höher fest, als Sie vermuten, dass Sie Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="c7a89-117">When in doubt, set both values a little higher than you think you need them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7a89-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7a89-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a89-119">**Pufferung von Inhalten**</span><span class="sxs-lookup"><span data-stu-id="c7a89-119">**Buffering Content**</span></span>](buffering-content.md)
</dt> <dt>

[<span data-ttu-id="c7a89-120">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="c7a89-120">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




