---
description: Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349136"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="23663-103">Warum akzeptiert ein Decoder nicht das von mir festgelegte Eingabeformat?</span><span class="sxs-lookup"><span data-stu-id="23663-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="23663-104">Es gibt zahlreiche Gründe, warum ein Decoder ein Format ablehnen könnte.</span><span class="sxs-lookup"><span data-stu-id="23663-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="23663-105">Am häufigsten werden fehlende oder falsche erweiterte Formatierungsdaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23663-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="23663-106">Bei den erweiterten Formatierungsdaten handelt es sich um Codec-spezifische Informationen, die an die Struktur angehängt werden, die den Medientyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="23663-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="23663-107">Wenn Sie einen Ausgabetyp mit einem encoderobjekt auflisten, verweist der **pbformat** -Member der [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur auf eine **WaveFormatEx** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="23663-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="23663-108">An diese Struktur werden erweiterte Formatierungsdaten angehängt, und die Größe dieser Daten wird im **WaveFormatEx. cbSize** -Element gespeichert.</span><span class="sxs-lookup"><span data-stu-id="23663-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="23663-109">Unabhängig vom Container, der zum Speichern der komprimierten Daten verwendet wird, müssen Sie die **WaveFormatEx** -Struktur persistent speichern und im Eingabetyp für den Decoder verwenden.</span><span class="sxs-lookup"><span data-stu-id="23663-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="23663-110">Ohne die erweiterten Formatierungsdaten kann der Decoder den Inhalt nicht dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="23663-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="23663-111">Bei Videoformaten müssen Sie die erweiterten Formatierungsdaten manuell abrufen und an die **videoinfoheader** -Struktur anfügen.</span><span class="sxs-lookup"><span data-stu-id="23663-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="23663-112">Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="23663-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23663-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23663-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23663-114">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="23663-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
