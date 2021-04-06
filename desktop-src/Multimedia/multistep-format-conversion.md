---
title: Mehrstufige Format Konvertierung
description: Mehrstufige Format Konvertierung
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Audiokomprimierungs-Manager (ACM), Daten werden umgerechnet
- ACM (Audiokomprimierungs-Manager), Daten werden umgerechnet
- ACM-Beispiele, Daten werden umgerechnet
- Konvertieren von Daten
- acmformatvorschlagen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947772"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="2bbdd-108">Mehrstufige Format Konvertierung</span><span class="sxs-lookup"><span data-stu-id="2bbdd-108">Multistep Format Conversion</span></span>

<span data-ttu-id="2bbdd-109">Manchmal kann das ACM in einem einzigen Schritt keine Daten von einem Format in ein anderes konvertieren.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="2bbdd-110">Beispielsweise muss eine Anwendung möglicherweise 16-Bit-, 44-kHz-Stereodaten in 11-kHz Mono ADPCM konvertieren.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="2bbdd-111">Wenn der-Kompressor oder der Dekompressor diese Konvertierung nicht direkt ausführen kann, kann Sie von der Anwendung in zwei Schritten versucht werden.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="2bbdd-112">Dies bedeutet in der Regel, dass eine Konvertierung zwischen zwei PCM-Formaten durchführen und dann eine weitere Konvertierung in den endgültigen Formattyp erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="2bbdd-113">Um in zwei Schritten zu konvertieren, verwenden Sie die [**acmformatvorschlagen**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) -Funktion, um ein PCM-Format zu finden, das dem ADPCM-Format entspricht.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="2bbdd-114">Verwenden Sie dann zwei Konvertierungsdaten Ströme, um die Konvertierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="2bbdd-115">Führen Sie z. b. eine Konvertierung von 16-Bit-, 44-kHz-Stereo-PCM in 16-Bit, 11-kHz Mono aus, und konvertieren Sie dann von 16-Bit-, 11-kHz Mono in 11-kHz Mono ADPCM.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="2bbdd-116">Die mehrstufige Konvertierung ist auch dann der Fall, wenn das Quell-oder Zielformat nicht PCM ist.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="2bbdd-117">Wenn das Quellformat nicht PCM ist, sollte es vor der Konvertierung in ein PCM-Format geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="2bbdd-118">Wenn das Zielformat nicht PCM ist, muss die Quelle in ein zwischen-PCM-Format konvertiert und dann in das endgültige Zielformat konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="2bbdd-119">Die einfachsten Konvertierungen treten auf, wenn es sich bei den Quell-und Zielformaten um PCM-Formate handelt.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="2bbdd-120">Wenn das Quell-oder Zielformat nicht PCM ist, ist für die Konvertierung möglicherweise ein zusätzlicher Schritt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="2bbdd-121">Wenn das Quell-und Zielformat nicht PCM sind, ist für die Konvertierung in der Regel mehr als ein Schritt erforderlich, und in manchen Fällen ist eine Konvertierung möglicherweise nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="2bbdd-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




