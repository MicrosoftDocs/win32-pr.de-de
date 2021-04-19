---
description: Konfigurieren des ASF-Writers
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Konfigurieren des ASF-Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342958"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="b3412-103">Konfigurieren des ASF-Writers</span><span class="sxs-lookup"><span data-stu-id="b3412-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="b3412-104">Wenn der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter erstellt wird, wird er automatisch mit dem Video Profil "wmprofile \_ V80 256" konfiguriert \_ .</span><span class="sxs-lookup"><span data-stu-id="b3412-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="b3412-105">In diesem Profil werden die Codecs Windows Media Audio und Windows Media Video Version 8 verwendet, die nicht so aktuell sind wie die Codecs der Windows Media 9-Serie.</span><span class="sxs-lookup"><span data-stu-id="b3412-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="b3412-106">Es wird empfohlen, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und den WM-ASF-Writer mit dem benutzerdefinierten Profil zu konfigurieren, wie unter [Konfigurieren von Profilen und anderen Eigenschaften von ASF-Dateien](configuring-profiles-and-other-asf-file-properties.md)beschrieben</span><span class="sxs-lookup"><span data-stu-id="b3412-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="b3412-107">Sie müssen den WM-ASF-Writer-Filter vor dem Konfigurieren des Filters dem Filter Diagramm hinzufügen und den Filter konfigurieren, bevor Sie ihn mit anderen Filtern verbinden.</span><span class="sxs-lookup"><span data-stu-id="b3412-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="b3412-108">Alle Eingabedaten müssen mit einem Zeitstempel versehen werden, und alle Eingabe Pins müssen verbunden sein, bevor der Filter ausgeführt oder angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3412-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="b3412-109">Wenn Sie den Filter mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter daher eine Audiodatei und eine Videoeingabe-PIN. beide Pins müssen miteinander verbunden sein, bevor der Filter ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3412-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="b3412-110">Da das Windows Media-Format-SDK erfordert, dass ein Audiostream funktioniert, muss der WM-ASF-Writer immer über eine eingabeaudiopin verfügen, selbst wenn es sich um einen Pseudo Datenstrom handelt – d. h. um einen stumm geschalteter Audiostream mit niedriger Bitrate.</span><span class="sxs-lookup"><span data-stu-id="b3412-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="b3412-111">Hinzufügen von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b3412-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="b3412-112">Sie können einen profilstream für dateneinheits Erweiterungen konfigurieren, wie z. b. SMPTE-Zeit Codes, entweder vor oder nach dem Verbinden des Filters, solange Sie dieser Reihenfolge von Vorgängen folgen:</span><span class="sxs-lookup"><span data-stu-id="b3412-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="b3412-113">Fügen Sie dem Stream mithilfe von **IWMStreamConfig2:: adddataunitextension** eine oder mehrere Dateneinheiten Erweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3412-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="b3412-114">Nennen Sie **iwmprofile:: reconfigstream** , um das Profil zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b3412-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="b3412-115">Nennen Sie [**iconfigasfwriter:: konfigurierfilterusingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) mit dem aktualisierten Profil Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3412-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="b3412-116">Suchen Sie die Videoeingabe-PIN, und wenden Sie Ihre [**iamwmbufferpass:: setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) -Methode an, um Ihre Anwendungs definierte [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b3412-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="b3412-117">Wenn das Diagramm ausgeführt wird, wird die [**iamwmbufferpasscallback:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) -Methode für jeden Frame aufgerufen, und Sie können Eigenschaften für das Beispiel mithilfe der **INSSBuffer3** -Schnittstellen Methoden erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="b3412-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="b3412-118">In einigen Prozessor intensiven Szenarien wie z. b. Inverse Telecine benötigt der WM-ASF-Writer möglicherweise mehr Ausgabepuffer, als von einigen downstreamfiltern unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3412-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="b3412-119">Der DV-Decoder nimmt z. b. für die Ausgabepin nicht mehr als einen Puffer an, und dasselbe gilt für den AVI-Dekompressor unter bestimmten Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="b3412-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="b3412-120">Wenn beim Versuch, eine Verbindung mit diesen Filtern herzustellen, oder möglicherweise beim Ausführen des Diagramms Probleme auftreten, kann es erforderlich sein, einen Vermittler Filter zu schreiben, der eine beliebige Anzahl von Puffern in der Ausgabe-PIN akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b3412-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b3412-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3412-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3412-122">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3412-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



