---
description: Konfigurieren der Audiodecodierung
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Konfigurieren der Audiodecodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749329"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="5c7d6-103">Konfigurieren der Audiodecodierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="5c7d6-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="5c7d6-104">Das Decodieren Windows Media Audio Inhalts ist viel einfacher als das Codieren.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="5c7d6-105">Legen Sie nach dem Erstellen eines audiodecoderobjekts den Eingabetyp mithilfe der **imediaobject:: setinputtype** -Methode oder der **IMF Transform:: setinputtype** -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="5c7d6-106">Der Medientyp, den Sie für die Decoder-Eingabe verwenden, muss dem Ausgabetyp entsprechen, der beim Codieren des Inhalts verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="5c7d6-107">Dies schließt die erweiterten Formatierungsdaten ein, die an die **WaveFormatEx** -Struktur angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="5c7d6-108">Sie müssen sicherstellen, dass diese Daten korrekt sind, da der Decoder keine Stichproben verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="5c7d6-109">Nachdem Sie den Eingabetyp festgelegt haben, können Sie alle Decoder-Funktionen konfigurieren, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="5c7d6-110">Decoderfeatures, wie z. b. die für die Codierung verwendeten, werden mithilfe der Methoden von **IPropertyBag** oder **IPropertyStore** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="5c7d6-111">Nachdem der Eingabetyp festgelegt und alle Decoder-Funktionen konfiguriert wurden, können Sie die vom Decoder unterstützten Ausgabetypen auflisten, indem Sie **imediaobject:: getoutputtype** oder **imftransform:: getoutputtype** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5c7d6-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c7d6-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c7d6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c7d6-113">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="5c7d6-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



