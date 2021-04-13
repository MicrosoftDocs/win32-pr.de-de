---
title: Schreiben von komprimierten Beispielen
description: Schreiben von komprimierten Beispielen
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), Schreiben von komprimierten Beispielen
- ASF (Advanced Systems Format), Schreiben von komprimierten Beispielen
- Advanced Systems Format (ASF), übergeben von komprimierten Beispielen
- ASF (Advanced Systems Format), übergeben von komprimierten Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472252"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="0e755-107">Schreiben von komprimierten Beispielen</span><span class="sxs-lookup"><span data-stu-id="0e755-107">Writing Compressed Samples</span></span>

<span data-ttu-id="0e755-108">Für einige Audiodaten und Videostreams empfiehlt es sich, bereits komprimierte Beispiele zu übergeben, anstatt Rohdaten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e755-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="0e755-109">Diese Funktion wird verwendet, um einen vorhandenen Stream zu kopieren oder um mit einem Drittanbieter-Codec komprimierte Beispiele zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0e755-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="0e755-110">Der Prozess zum Schreiben eines komprimierten Beispiels ist mit dem Schreiben eines unkomprimierten Beispiels identisch, mit dem Unterschied, dass Sie anstelle von [**iwmwriter:: writesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)den Wert [**iwmwriteradvanced:: writestreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e755-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="0e755-111">Weitere Informationen zum Schreiben von nicht komprimierten Beispielen finden [Sie unter so schreiben Sie Beispiele](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0e755-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="0e755-112">Wenn Sie komprimierte Beispiele für CBR-profile schreiben, löscht der Writer ggf. einige Beispiele, damit der Inhalt innerhalb der angegebenen Bitrate und Puffer Fenster Werte aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="0e755-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="0e755-113">Für VBR werden von dem Writer keine Stichproben gelöscht, aber es gibt keine Möglichkeit, sicherzustellen, dass die Werte für Bitrate und Puffer Fenster korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="0e755-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="0e755-114">Wenn Sie einen Stream aus einer Datei in eine andere kopieren, sollten Sie das Datenstrom-Konfigurationsobjekt immer aus dem Profil der ursprünglichen Datei in das Profil der neuen Datei kopieren.</span><span class="sxs-lookup"><span data-stu-id="0e755-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="0e755-115">Dadurch wird sichergestellt, dass Sie über die richtigen Bitrate-und Puffer Fenster Informationen verfügen.</span><span class="sxs-lookup"><span data-stu-id="0e755-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="0e755-116">Wenn Sie einen komprimierten Stream in einen Stream kopieren, für den ein niedrigeres Puffer Fenster festgelegt ist, werden beim Schreiben von Dateien Stichproben gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0e755-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e755-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e755-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e755-118">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="0e755-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




