---
title: Kopieren von Streams mithilfe von nicht komprimierten Beispielen
description: Kopieren von Streams mithilfe von nicht komprimierten Beispielen
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media-Format-SDK, Kopieren von Streams
- Advanced Systems Format (ASF), Kopieren von Streams
- ASF (Advanced Systems Format), Kopieren von Streams
- Streams, Kopieren mithilfe von entkomprimierten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340238"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="2b637-107">Kopieren von Streams mithilfe von nicht komprimierten Beispielen</span><span class="sxs-lookup"><span data-stu-id="2b637-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="2b637-108">Es wird dringend empfohlen, Datenströme nicht mithilfe von dekomprimierten Beispielen aus einer Datei in eine andere Datei zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="2b637-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="2b637-109">Durch das Dekomprimieren und Erneutes Komprimieren von Beispielen wird die Qualität der Ausgabe herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="2b637-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="2b637-110">Wenn Sie die Beispiele Dekomprimieren und Sie dann in einen anderen Stream kopieren müssen, kann es schwierig sein, mit Qualitäts basierten, VBR-codierten Streams (Variable Bitrate) zu tun.</span><span class="sxs-lookup"><span data-stu-id="2b637-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="2b637-111">Wenn der Codec das Komprimieren eines Qualitäts basierten VBR-Streams beendet, zeichnet er die Bitrate und das Puffer Fenster des resultierenden Inhalts auf.</span><span class="sxs-lookup"><span data-stu-id="2b637-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="2b637-112">Wenn Sie eine Datei mit einem Stream lesen, der mit einer qualitativ hochwertigen VBR-Codierung codiert ist, werden von dem vom Reader erhaltenen Profil sowohl die Bitrate als auch das Puffer Fenster sowie die maximale Bitrate und das maximale Puffer Fenster festgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b637-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="2b637-113">Diese Konfiguration im Profil weist normalerweise einen Bitraten-Stream mit eingeschränkter Bitrate auf.</span><span class="sxs-lookup"><span data-stu-id="2b637-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="2b637-114">Wenn Sie das Profil für den Writer festlegen, wird daher ein Vorverarbeitungs Durchlauf für den Datenstrom erwartet, da VBR-Streams mit Bitrate-Einschränkung eine zwei-Pass-Codierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="2b637-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="2b637-115">Der Stream sollte so behandelt werden, als ob es sich um einen eingeschränkten VBR-Stream mit Bitraten handelt, und die Beispiele für die Vorverarbeitung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2b637-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="2b637-116">Da Sie die Werte verwenden, die nach dem Codieren des Inhalts auf einer bestimmten Qualitätsstufe zurückgegeben werden, stellen diese Werte die gewünschte Qualitätsstufe dar.</span><span class="sxs-lookup"><span data-stu-id="2b637-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="2b637-117">Natürlich wird die Qualität der neu codierten Ausgabe nach wie vor durch die erneute Codierung etwas beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="2b637-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b637-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b637-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b637-119">**Kopieren von Daten aus einer Datei in eine andere**</span><span class="sxs-lookup"><span data-stu-id="2b637-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="2b637-120">**Kopieren von Streams, ohne die Daten zu entkomprimieren**</span><span class="sxs-lookup"><span data-stu-id="2b637-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




