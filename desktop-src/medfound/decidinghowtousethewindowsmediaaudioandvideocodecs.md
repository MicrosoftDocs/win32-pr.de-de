---
description: Verwenden der Codec-und DSP-Objekte
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Verwenden der Codec-und DSP-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363888"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="4d2c4-103">Verwenden der Codec-und DSP-Objekte</span><span class="sxs-lookup"><span data-stu-id="4d2c4-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="4d2c4-104">Es gibt mehrere Möglichkeiten, die Windows Media Audio-und Video Codecs und die DSPs zu verwenden, um den Inhalt digitaler Medien zu codieren, zu decodieren oder zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="4d2c4-105">Der Windows Media Audio und der Videocodec und die DSP-API sind für Benutzer gedacht, die Codec-und DSP-Objekte manuell konfigurieren müssen, oder Sie können Sie außerhalb des Kontexts eines der Windows Media SDKs verwenden, wie z. b. das Windows Media-Format-SDK oder Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="4d2c4-106">Inhalts Ersteller und Endbenutzer können mit einer Vielzahl von Tools und Anwendungen Inhalte in Windows Media Audio oder Windows Media Video Streams codieren.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="4d2c4-107">Windows Media Encoder ist beispielsweise speziell dafür konzipiert, den Codierungsprozess zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="4d2c4-108">Ebenso wurde Windows Media Player speziell für die Verwendung von digitalen Mediendaten entwickelt, die in Windows Media-Formaten codiert sind.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="4d2c4-109">Für viele Anwendungen ist nur die Verwendung des Windows Media Encoder SDK oder des Windows Media Player SDK erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="4d2c4-110">Insbesondere sind diese beiden Technologien für Szenarien geeignet, die der Funktionalität der von Ihnen automatisierten Tools ähneln.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="4d2c4-111">Wenn Sie eine bessere Kontrolle über den Codierungs-oder Decodierungs Prozess benötigen, aber trotzdem beabsichtigen, das Advanced Systems Format (ASF) als Container für Ihre Mediendaten zu verwenden, ist das Windows Media-Format-SDK möglicherweise eine gute Wahl.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="4d2c4-112">Die Objekte des SDK für den Windows Media-Format bieten ein flexibles Framework zum Erstellen von ASF-Dateien und bieten integrierte Unterstützung für die Windows Media Audio-und Video Codecs.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="4d2c4-113">Das Media Foundation SDK, das neu für Windows Vista ist, vereinfacht das Codieren und decodieren erheblich, indem es eine anpassbare Medien Pipeline bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="4d2c4-114">Sie können die Eigenschaften für die Eingabe-und Ausgabemedien festlegen, und der Media Foundation topologielader konfiguriert die erforderlichen Codecs und DSPs für Sie.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="4d2c4-115">Der Hauptgrund für die direkte Verwendung der Codec-Objekte ist die Verwendung des Windows Media Audio und der Video Codecs außerhalb des ASF-Containers.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="4d2c4-116">Die Verwendung der Codec-und DSP-Objekte bietet auch eine Steuerungsebene, die mit einer der abstrahierten Technologien nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4d2c4-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d2c4-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d2c4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2c4-118">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="4d2c4-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



