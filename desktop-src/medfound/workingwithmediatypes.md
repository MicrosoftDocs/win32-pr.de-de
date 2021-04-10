---
description: Arbeiten mit DMO-Medientypen
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Arbeiten mit DMO-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961125"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="f9044-103">Arbeiten mit DMO-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f9044-103">Working with DMO Media Types</span></span>

<span data-ttu-id="f9044-104">Die von den Codec-DMOS verwendeten Eingabe-und Ausgabemedien Typen werden mithilfe der [**\_ \_ Medientyp Struktur von DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) definiert.</span><span class="sxs-lookup"><span data-stu-id="f9044-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="f9044-105">Diese Struktur ist identisch mit dem im Windows Media SDK-SDK definierten [**Typ "WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)" und [**" \_ am \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type)", der in der Microsoft DirectShow-® definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9044-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="f9044-106">Abhängig von Ihrer Anwendung können Sie Variablen verwenden, die als einer dieser drei Typen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9044-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="f9044-107">Es ist sicher, einen Zeiger auf eine der Medientyp Strukturen als einen anderen umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="f9044-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="f9044-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f9044-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="f9044-109">Die von den Codecs verwendeten Format Typen sind in der Regel auf die von den **videoinfoheader** -und **WaveFormatEx** -Strukturen beschriebenen Typen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f9044-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="f9044-110">Zur einfacheren Handhabung sind Konstanten für diese Format Typen in der Header Datei "wmcodeckonst. h" enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9044-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="f9044-111">Die Konstanten Namen lauten wmcformat \_ videoinfo bzw. wmcformat \_ WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="f9044-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="f9044-112">Die Audiocodecs können unter bestimmten Umständen mit der **WAVEFORMATEXTENSIBLE** -Struktur verwendet werden und müssen Sie in anderen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9044-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="f9044-113">Der **DMO- \_ \_ Medientyp. formatType** wird jedoch auf denselben Wert festgelegt wie für **WaveFormatEx**.</span><span class="sxs-lookup"><span data-stu-id="f9044-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="f9044-114">Weitere Informationen zur Verwendung von **WAVEFORMATEXTENSIBLE** finden Sie unter [Verwenden von High-Definition-Audiodaten](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="f9044-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="f9044-115">Sie müssen die Formattyp Struktur, die als encoderausgabe verwendet wird, in den Container einschließen, den Sie zum Speichern der komprimierten Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9044-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="f9044-116">Die Decoder benötigen die ursprüngliche Format Struktur, um den Inhalt zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="f9044-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="f9044-117">Zusätzlich zu den Elementen der Struktur erfordern komprimierte Windows Media Audio und Video Typen zusätzliche Formatinformationen, die an die Struktur angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="f9044-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="f9044-118">Weitere Informationen finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="f9044-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9044-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9044-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9044-120">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="f9044-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
