---
description: Dumpfilterbeispiel
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Dumpfilterbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522416"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="fe222-103">Dumpfilterbeispiel</span><span class="sxs-lookup"><span data-stu-id="fe222-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="fe222-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe222-104">Description</span></span>

<span data-ttu-id="fe222-105">Der dumpfilter ist ein rendererfilter, der die empfangenen Medien Beispiele in eine Textdatei schreibt.</span><span class="sxs-lookup"><span data-stu-id="fe222-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="fe222-106">In diesem Beispiel wird veranschaulicht, wie die Basis Filterklasse [**cbasefilter**](cbasefilter.md) und die gerenderte Eingabe-PIN-Klasse [**crenderedinputpin**](crenderedinputpin.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe222-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="fe222-107">Außerdem wird veranschaulicht, wie die [**ifilesink Filter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe222-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="fe222-108">Der dumpfilter verfügt über eine einzelne Eingabe-PIN, die jedes empfangene Beispiel direkt in eine Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="fe222-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="fe222-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fe222-109">Usage</span></span>

<span data-ttu-id="fe222-110">Dieser Filter ist ein nützliches Debugtool.</span><span class="sxs-lookup"><span data-stu-id="fe222-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="fe222-111">Beispielsweise können Sie die Ergebnisse eines Transformations Filters mit Bit und Bit überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fe222-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="fe222-112">Sie können ein Diagramm manuell erstellen, indem Sie GraphEdit verwenden und den dumpfilter mit der Ausgabe eines Transformations Filters oder einer anderen Ausgabepin verbinden.</span><span class="sxs-lookup"><span data-stu-id="fe222-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="fe222-113">Sie können auch einen Tee-Filter verbinden und den dumpfilter auf einem Teil des Tee-Filters und die typische Ausgabe in einem anderen Abschnitt platzieren, um die Ergebnisse in einem echt Zeit Szenario zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="fe222-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="fe222-114">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="fe222-114">Downloading the Sample</span></span>

<span data-ttu-id="fe222-115">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fe222-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="fe222-116">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Dump.</span><span class="sxs-lookup"><span data-stu-id="fe222-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe222-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe222-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe222-118">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe222-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



