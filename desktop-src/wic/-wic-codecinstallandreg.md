---
description: Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren. Sie müssen auch sicherstellen, dass der Miniatur Ansichts Cache aktualisiert wird, falls bereits Bilder in Ihrem Format auf dem Computer vorhanden sind.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Codec-Installation und-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368814"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="3405d-104">Codec-Installation und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="3405d-104">Codec Installation and Registration</span></span>

<span data-ttu-id="3405d-105">Wenn Sie einen Codec installieren, müssen Sie ihn in der Registrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="3405d-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="3405d-106">Sie müssen auch sicherstellen, dass der Miniatur Ansichts Cache aktualisiert wird, falls bereits Bilder in Ihrem Format auf dem Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3405d-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="3405d-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3405d-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3405d-108">Registrieren eines Codecs</span><span class="sxs-lookup"><span data-stu-id="3405d-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="3405d-109">Aktualisieren des Miniatur Ansichts Caches bei der Installation Ihres Codecs</span><span class="sxs-lookup"><span data-stu-id="3405d-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="3405d-110">Verfügbar machung Ihres WIC-Enabled Codecs für Benutzer</span><span class="sxs-lookup"><span data-stu-id="3405d-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="3405d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3405d-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="3405d-112">Registrieren eines Codecs</span><span class="sxs-lookup"><span data-stu-id="3405d-112">Registering a Codec</span></span>

<span data-ttu-id="3405d-113">Wenn Sie einen Codec registrieren, registrieren Sie tatsächlich zwei Komponenten: den Encoder und den Decoder.</span><span class="sxs-lookup"><span data-stu-id="3405d-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="3405d-114">Sie müssen auch Registrierungseinträge erstellen, um Ihr Containerformat bei den metadatenhandlern für die Metadatenformate zu registrieren, die von Ihrem Bildformat unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3405d-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="3405d-115">In den folgenden Themen werden die Registrierungseinträge beschrieben, die Sie benötigen, um Ihren Codec zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="3405d-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="3405d-116">Allgemeine Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="3405d-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="3405d-117">Codierungs spezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="3405d-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="3405d-118">Decoderspezifische Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="3405d-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="3405d-119">Integration in Windows Photo Gallery und Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="3405d-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="3405d-120">Aktualisieren des Miniatur Ansichts Caches bei der Installation Ihres Codecs</span><span class="sxs-lookup"><span data-stu-id="3405d-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="3405d-121">Wenn ein Codec installiert ist, muss das Installationsprogramm die folgende Funktion nach dem Schreiben der zugehörigen Registrierungseinträge aufruft.</span><span class="sxs-lookup"><span data-stu-id="3405d-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="3405d-122">Dieser Befehl benachrichtigt Windows, dass neue Datei Zuordnungs Informationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3405d-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="3405d-123">Wenn bereits Bilder im Bildformat auf dem Computer vorhanden sind, enthält der Miniatur Ansichts Cache standardmäßige Miniaturansichten für diese, da kein Decoder zum Extrahieren der Miniaturansichten verfügbar war, als die Bilder zum ersten mal abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="3405d-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="3405d-124">Wenn Sie Windows Benachrichtigen, dass eine neue Datei Zuordnung verfügbar ist, verwirft der Miniatur Ansichts Cache alle leeren Miniaturansichten und extrahiert die eigentlichen Miniaturansichten aus den Dateien, die nun decodiert werden können.</span><span class="sxs-lookup"><span data-stu-id="3405d-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="3405d-125">Verfügbar machung Ihres WIC-Enabled Codecs für Benutzer</span><span class="sxs-lookup"><span data-stu-id="3405d-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="3405d-126">Wenn Sie ein Kamerahersteller sind, können Sie Ihre unformatierten Codecs in der Box mit ihren Kameras versenden.</span><span class="sxs-lookup"><span data-stu-id="3405d-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="3405d-127">Sie können Ihre Codecs auch auf der Download Seite Ihrer Website veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="3405d-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="3405d-128">Wenn ein Benutzer jedoch eine Bilddatei in Ihrem Format aus einer anderen Quelle, z. b. einem Friend, einem Geschäftspartner oder einer anderen Website, erhält, wissen Sie möglicherweise nicht, wo der Codec zum Decodieren des Codecs zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="3405d-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="3405d-129">Aufgrund dieses Problems bietet Windows eine einfachere Möglichkeit für Benutzer Ihres Bildformats, ihren Codec zu finden und auf Ihren Computer herunterzuladen, beginnend mit Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3405d-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="3405d-130">Wenn die Windows-Fotogalerie eine Dateinamenerweiterung als Bildformat erkennt und der Codec für dieses Format nicht installiert ist, wird dem Benutzer in einem Dialogfeld mitgeteilt, dass das Foto nicht angezeigt werden kann, und es wird gefragt, ob der Benutzer die für die Anzeige erforderliche Software herunterladen möchte.</span><span class="sxs-lookup"><span data-stu-id="3405d-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="3405d-131">Wenn der Benutzer akzeptiert, wird eine von Microsoft gehostete Website mit einem Link zur Download Site des Codec-Herstellers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3405d-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="3405d-132">(Optional können Sie anfordern, dass Benutzer direkt zu Ihrer Download Site gelangen.)</span><span class="sxs-lookup"><span data-stu-id="3405d-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="3405d-133">Wenn Sie möchten, dass die Dateinamen Erweiterungen Ihres Bildformats von der Windows-Fotogalerie erkannt werden, damit Benutzer zu Ihrer Download Website weitergeleitet werden können, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="3405d-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="3405d-134">Stellen Sie eine Download Site für Ihren Codec bereit.</span><span class="sxs-lookup"><span data-stu-id="3405d-134">Provide a download site for your codec.</span></span> <span data-ttu-id="3405d-135">(Sie können für jeden von Ihnen bereitgestellten CODEC eine separate Seite oder eine Seite mit Downloads für alle Ihre Codecs bereitstellen.)</span><span class="sxs-lookup"><span data-stu-id="3405d-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="3405d-136">Die Download Site sollte lokalisiert und problemlos nach Kameramodell durchsuchbar sein.</span><span class="sxs-lookup"><span data-stu-id="3405d-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="3405d-137">Geben Sie Microsoft eine Liste mit Erweiterungen für Ihre Bildformate und die URLs für die Download Websites.</span><span class="sxs-lookup"><span data-stu-id="3405d-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="3405d-138">Sie müssen Microsoft über die Erweiterungen für alle neuen Codecs informieren, die Sie in Zukunft entwickeln, und über alle Änderungen an den URLs Ihrer Download Websites, damit die neuen Informationen der Windows-Fotogalerie hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="3405d-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3405d-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3405d-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3405d-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3405d-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3405d-141">Implementieren von IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="3405d-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="3405d-142">Schlussfolgerung (Schreiben eines WIC-Enabled Codecs)</span><span class="sxs-lookup"><span data-stu-id="3405d-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="3405d-143">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="3405d-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="3405d-144">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="3405d-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



