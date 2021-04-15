---
description: Qualitäts Meldungen
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Qualitäts Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521328"
---
# <a name="quality-messages"></a><span data-ttu-id="e68df-103">Qualitäts Meldungen</span><span class="sxs-lookup"><span data-stu-id="e68df-103">Quality Messages</span></span>

<span data-ttu-id="e68df-104">Qualitäts Meldungen werden mit der [**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="e68df-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="e68df-105">Diese Struktur enthält die folgenden Member:</span><span class="sxs-lookup"><span data-stu-id="e68df-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="e68df-106">**Typ:** Definiert durch die [**qualitymessagetype**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) -Enumeration. entweder eine Hungersnot, die angibt, dass der Filter zu wenig Daten empfängt, oder Überflutung, was darauf hinweist, dass der Filter zu viele Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="e68df-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="e68df-107">**Proportional:** Die angeforderte Anpassung in der Datenrate von der Baseline 1000.</span><span class="sxs-lookup"><span data-stu-id="e68df-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="e68df-108">750 gibt beispielsweise an, dass 75% und 1500 150% betragen.</span><span class="sxs-lookup"><span data-stu-id="e68df-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="e68df-109">**Spät:** Verweis Zeit, die angibt, wie spät das letzte Beispiel erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="e68df-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="e68df-110">Der Wert ist negativ, wenn das Beispiel früh eingetroffen ist.</span><span class="sxs-lookup"><span data-stu-id="e68df-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="e68df-111">**Zeitstempel:** Der Zeitstempel für das letzte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e68df-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="e68df-112">Nehmen wir beispielsweise an, dass ein Beispiel mit einem Zeitstempel von 240 Millisekunden (MS) den Renderer bei 280 ms, streamzeit erreicht.</span><span class="sxs-lookup"><span data-stu-id="e68df-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="e68df-113">Der Renderer erstellt eine Qualitäts Nachricht vom Typ Hungersnot.</span><span class="sxs-lookup"><span data-stu-id="e68df-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="e68df-114">Das Beispiel wurde 40 ms nach dem Ende erreicht, sodass das **späte** Mitglied 400000 ist.</span><span class="sxs-lookup"><span data-stu-id="e68df-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="e68df-115">(Alle Verweis Zeiten befinden sich in 100-Nanosecond-Einheiten.) Der **timestamp** -Member ist 2,4 Millionen.</span><span class="sxs-lookup"><span data-stu-id="e68df-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="e68df-116">Für das **proportional** Element kann der Renderer einen laufenden Durchschnitt verwenden, um den Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e68df-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="e68df-117">Möglicherweise sind Beispiele in der Zeit eingetroffen, und dieses Beispiel ist eine Anomalie.</span><span class="sxs-lookup"><span data-stu-id="e68df-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="e68df-118">In diesem Fall kann der Renderer nur eine kleine Korrektur anfordern.</span><span class="sxs-lookup"><span data-stu-id="e68df-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="e68df-119">Wenn die Stichproben dagegen konsistent sind, kann der Renderer eine größere Korrektur anfordern.</span><span class="sxs-lookup"><span data-stu-id="e68df-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="e68df-120">Die Qualitätskontrolle wird durch die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle behandelt.</span><span class="sxs-lookup"><span data-stu-id="e68df-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="e68df-121">Sie enthält zwei Methoden.</span><span class="sxs-lookup"><span data-stu-id="e68df-121">It contains two methods.</span></span>

-   <span data-ttu-id="e68df-122">[**Benachrichtigen**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): sendet eine Qualitäts Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e68df-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="e68df-123">[**Setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): gibt einen benutzerdefinierten Quality Manager an.</span><span class="sxs-lookup"><span data-stu-id="e68df-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="e68df-124">Ein Objekt, das **iqualitycontrol** implementiert, empfängt Qualitäts Nachrichten über seine **Benachrichtigungs** Methode.</span><span class="sxs-lookup"><span data-stu-id="e68df-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="e68df-125">Die Nachricht kann entweder verarbeitet oder an ein anderes Objekt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e68df-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="e68df-126">Wenn die Anwendung die **setsink** -Methode des Objekts aufruft, sollte das Objekt die Qualitätskontrolle an den angegebenen Quality Manager delegieren.</span><span class="sxs-lookup"><span data-stu-id="e68df-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 



