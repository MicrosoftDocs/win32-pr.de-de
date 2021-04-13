---
title: Informationen zu streamkonfigurations Informationen von Codecs
description: Informationen zu streamkonfigurations Informationen von Codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- Streams, Konfigurationen von Codecs
- Codecs, von dem Datenstrom Konfigurationen abgeleitet werden
- Streams, Codec-Formate
- Codecs, Formate
- Streams, iwmcodecinfo-Schnittstelle
- Iwmcodecinfo, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390040"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="e9d60-109">Informationen zu streamkonfigurations Informationen von Codecs</span><span class="sxs-lookup"><span data-stu-id="e9d60-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="e9d60-110">Für Audiodaten und Videostreams, die die Windows Media Audio-und Video Codecs verwenden, sollten Sie die Werte für die Datenstrom-Konfigurations Strukturen aus dem Codec erhalten, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e9d60-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="e9d60-111">Obwohl es möglich ist, diese Werte selbst festzulegen, stellt die Verwendung der Codecs sicher, dass die Werte genau sind.</span><span class="sxs-lookup"><span data-stu-id="e9d60-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="e9d60-112">Sie sollten die Werte in diesen Strukturen nur dann ändern, wenn in der Dokumentation ausdrücklich eine bestimmte Änderung empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="e9d60-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="e9d60-113">Informationen aus den Codecs werden in Form von Codec-Formaten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9d60-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="e9d60-114">Jedes Codec-Format ist ein einzelnes Streamformat, das vom Codec unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d60-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="e9d60-115">Weitere Informationen zu streamformaten finden Sie unter [Formate](formats.md).</span><span class="sxs-lookup"><span data-stu-id="e9d60-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="e9d60-116">Sie können Informationen von den Windows Media-Codecs mithilfe der Schnittstellen [**iwmcodecinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)und [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) des Profil-Manager-Objekts anfordern.</span><span class="sxs-lookup"><span data-stu-id="e9d60-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="e9d60-117">Um die [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle eines Profil-Manager-Objekts abzurufen, müssen Sie die [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e9d60-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="e9d60-118">Nennen Sie **QueryInterface** für **iwmprofilemanager** , um **IWMCodecInfo3** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9d60-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="e9d60-119">In den folgenden Abschnitten wird beschrieben, wie Sie die benötigten Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="e9d60-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="e9d60-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="e9d60-120">Section</span></span>                                                                                                | <span data-ttu-id="e9d60-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9d60-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9d60-122">So zählen Sie alle installierten Windows Media-Codecs auf</span><span class="sxs-lookup"><span data-stu-id="e9d60-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="e9d60-123">Beschreibt, wie die-Methoden der **iwmcodecinfo** -Schnittstelle und der **IWMCodecInfo2** -Schnittstelle verwendet werden, um den Namen und den Codec-Index der einzelnen installierten Windows Media Codec abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9d60-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="e9d60-124">So zählen Sie Codec-Formate auf</span><span class="sxs-lookup"><span data-stu-id="e9d60-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="e9d60-125">Hier wird beschrieben, wie Sie Datenstrom-Konfigurationsobjekte aus Codecs für die Verwendung in ihren Profilen erhalten.</span><span class="sxs-lookup"><span data-stu-id="e9d60-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e9d60-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9d60-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9d60-127">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="e9d60-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




