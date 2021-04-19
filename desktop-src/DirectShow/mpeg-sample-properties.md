---
description: MPEG-Beispiel Eigenschaften
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: MPEG-Beispiel Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346408"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="d3f00-103">MPEG-Beispiel Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d3f00-103">MPEG Sample Properties</span></span>

<span data-ttu-id="d3f00-104">MPEG-Beispiele weisen die folgenden Eigenschaften auf.</span><span class="sxs-lookup"><span data-stu-id="d3f00-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="d3f00-105">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="d3f00-105">**Time Stamps**</span></span>

<span data-ttu-id="d3f00-106">Nicht alle Beispiele haben Start-und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="d3f00-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="d3f00-107">Die Beispiel Endzeit für Paket-und Nutzlastdaten ist nicht hilfreich. Sie wird in der Regel auf die Startzeit plus 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3f00-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="d3f00-108">Für die Stichproben von MPEG-Paketen oder Nutzlastdaten wird ein Start-und Endzeit Wert festgelegt, wenn das System Schicht Paket, von dem Sie generiert werden, gültige PTS enthält.</span><span class="sxs-lookup"><span data-stu-id="d3f00-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="d3f00-109">Weitere Informationen zu Zeitstempeln finden Sie im Abschnitt 2.4.1 von ISO1 "-11172:" der Paket Header enthält möglicherweise Decodierung und/oder Präsentationszeit Stempel (DTS und PTS), die auf die erste Zugriffs Einheit im Paket verweisen. "</span><span class="sxs-lookup"><span data-stu-id="d3f00-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="d3f00-110">Bei MPEG- \_ Stream-Haupttypen ist die Startzeit die Byte Position des ersten Byte, bewertet bei 1 Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="d3f00-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="d3f00-111">Die Endzeit ist die Byte Position des letzten Bytes.</span><span class="sxs-lookup"><span data-stu-id="d3f00-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="d3f00-112">Folglich sollten aufeinanderfolgende Stichproben die Endzeit des ersten Pakets aufweisen, das der Startzeit des nächsten Pakets entspricht.</span><span class="sxs-lookup"><span data-stu-id="d3f00-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="d3f00-113">Bei Video-CD-Daten muss der Ursprung des Mediums dem Format einer Video-CD-Datei entsprechen, die von CDFS mit dem standardmäßigen Riff Block am Anfang verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d3f00-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="d3f00-114">Bei MPEG-Video Paketen und Nutz Last Typen ist der Zeitstempel die Präsentationszeit für den ersten Videoframe, dessen Bild Start Code im Beispiel beginnt.</span><span class="sxs-lookup"><span data-stu-id="d3f00-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="d3f00-115">Bei MPEG-Audiopaketen und Nutz Last Typen ist der Zeitstempel die Präsentationszeit für den ersten audioframe, dessen Synchronisierungs Code im Beispiel beginnt.</span><span class="sxs-lookup"><span data-stu-id="d3f00-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="d3f00-116">Es wird davon ausgegangen, dass Paket-und Nutzlastdaten ohne Zeitstempel von den Behandlungs Filtern erfolgreich vorab durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="d3f00-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="d3f00-117">**Unterbrechungen**</span><span class="sxs-lookup"><span data-stu-id="d3f00-117">**Discontinuities**</span></span>

<span data-ttu-id="d3f00-118">Wenn eine Unterbrechung im Stream vorliegt (z. b. eine Lücke in den Echtzeitdaten oder ein Fehler in den Daten oder nach einer Suche), wird die Diskontinuität-Eigenschaft im nächsten Medien Beispiel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3f00-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="d3f00-119">Dadurch wird auch eine Zeitstempel Diskontinuität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d3f00-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="d3f00-120">**Streamende-Benachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="d3f00-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="d3f00-121">Wenn der Decoder diese Benachrichtigung empfängt, muss er alle gepufferten Daten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3f00-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="d3f00-122">Alle neuen Daten müssen dann mit der Diskontinuität-Eigenschaft beginnen.</span><span class="sxs-lookup"><span data-stu-id="d3f00-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f00-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3f00-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f00-124">MPEG-2-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d3f00-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



