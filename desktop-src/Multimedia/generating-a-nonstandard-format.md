---
title: Erstellen eines nicht standardmäßigen Formats
description: Erstellen eines nicht standardmäßigen Formats
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Audiokomprimierungs-Manager (ACM), nicht dem Standard entsprechende Formate
- ACM (Audiokomprimierungs-Manager), nicht dem Standard entsprechende Formate
- ACM-Beispiele, nicht dem Standard entsprechende Formate
- acmformatvorschlagen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856048"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="2e0f1-107">Erstellen eines nicht standardmäßigen Formats</span><span class="sxs-lookup"><span data-stu-id="2e0f1-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="2e0f1-108">Manchmal benötigt eine Anwendung ein nicht standardmäßiges Format.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="2e0f1-109">Beispielsweise benötigt eine Anwendung möglicherweise eine Datei mit dem Format "16-kHz ADPCM-Format".</span><span class="sxs-lookup"><span data-stu-id="2e0f1-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="2e0f1-110">Da 16 kHz nicht dem Standard entspricht, wird dieses Format von den Enumerationsfunktionen nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="2e0f1-111">In der Tat gibt es keine zuverlässige Möglichkeit, ein nicht standardmäßiges Format zu generieren, wenn Sie die Format Algorithmen nicht in die Anwendung schreiben.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="2e0f1-112">Es ist jedoch manchmal möglich, ein entsprechendes Format zu generieren, indem Sie ein gültiges PCM-Format mit allen erforderlichen Informationen einrichten und dann die [**acmformatvorschlagen**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="2e0f1-113">Da Kompressoren und Dekompressoren versuchen, ein Format vorzuschlagen, das dem gewünschten Format am nächsten liegt, wird die Anzahl der Kanäle und die Häufigkeit normalerweise beibehalten.</span><span class="sxs-lookup"><span data-stu-id="2e0f1-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




