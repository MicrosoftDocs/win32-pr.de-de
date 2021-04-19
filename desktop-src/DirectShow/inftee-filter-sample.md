---
description: Beispiel für einen inftee-Filter
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Beispiel für einen inftee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346825"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="2c380-103">Beispiel für einen inftee-Filter</span><span class="sxs-lookup"><span data-stu-id="2c380-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="2c380-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c380-104">Description</span></span>

<span data-ttu-id="2c380-105">Der inftee-Filter stellt eine Beispiel Implementierung des DirectShow-Ausgabefilters für [unendliche Pin](infinite-pin-tee-filter.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="2c380-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="2c380-106">Der Filter verfügt über eine Eingabe-PIN und eine dynamische Anzahl von Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="2c380-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="2c380-107">Alle an den Filter gesendeten Medien Beispiele werden gleichzeitig von allen Ausgabe Pins übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2c380-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="2c380-108">Dieser Filter wird in GraphEdit unter dem Namen "Sample Infinite Pin Tee" angezeigt, um ihn vom standardmäßigen unendlichen Pin-Tee-Filter zu unterscheiden, der in DirectShow bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c380-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="2c380-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="2c380-109">Usage</span></span>

<span data-ttu-id="2c380-110">Da mit diesem Filter nicht die empfangenen Daten geändert werden, müssen alle Pins dem gleichen Medientyp zustimmen.</span><span class="sxs-lookup"><span data-stu-id="2c380-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="2c380-111">Während des Verbindungs Vorgangs stellt der Filter möglicherweise eine Verbindung mit einigen Pins her, damit die Medientypen einander entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2c380-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="2c380-112">Daten, die bei der Eingabe-PIN eintreffen, werden nicht kopiert, bevor Sie an die Ausgabe Pins gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c380-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="2c380-113">Der Filter stellt außerdem sicher, dass die Daten an die downstreamfilter übermittelt werden, um sicherzustellen, dass beide Ausgaben einen rechtzeitigen Dienst empfangen.</span><span class="sxs-lookup"><span data-stu-id="2c380-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="2c380-114">Insbesondere, wenn eine der Ausgaben in der [**coutputqueue:: Receive**](coutputqueue-receive.md) -Member-Funktion blockiert werden kann, startet der Tee einen Thread, um das Beispiel zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="2c380-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="2c380-115">Wenn kein Thread zum Übermitteln des Beispiels vorhanden ist, kann der Thread, der das Beispiel an die Tee-Eingabe-PIN übergibt, die Daten an einen downstreamfilter übergeben. an diesem Punkt wird es möglicherweise blockieren, dass Daten aus dem anderen downstreamfilter über einen längeren Zeitraum hinweg aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="2c380-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="2c380-116">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2c380-116">Downloading the Sample</span></span>

<span data-ttu-id="2c380-117">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c380-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="2c380-118">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Info.</span><span class="sxs-lookup"><span data-stu-id="2c380-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c380-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c380-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c380-120">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c380-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



