---
title: Hinzufügen von Metadaten zu konvertierten Dateien
description: Hinzufügen von Metadaten zu konvertierten Dateien
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, Konvertierungsprozess
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Hinzufügen von Metadaten zu konvertierten Dateien
- Hinzufügen von Metadaten zu konvertierten Dateien
- Metadaten, hinzufügen zu konvertierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727736"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="3fb22-109">Hinzufügen von Metadaten zu konvertierten Dateien</span><span class="sxs-lookup"><span data-stu-id="3fb22-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="3fb22-110">Konvertierte Dateien müssen bestimmte Metadaten enthalten, um eine gute Benutzer Leistung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3fb22-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="3fb22-111">Konvertierte Dateien müssen mindestens die in den [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10))aufgeführten primären Attribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="3fb22-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="3fb22-112">Legen Sie für Musikdateien den Wert für **WM/mediaclassprimaryid** auf D1607DBC-E323-4BE2-86A1-48A42A28441E fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="3fb22-113">Legen Sie für Voicemaildateien den Wert für **WM/mediaclassprimaryid** auf 01cd0f29-da4e-4157-897b-6275d50c4f11 fest. Hierbei handelt es sich um die primäre Klassen-GUID für Audiodateien.</span><span class="sxs-lookup"><span data-stu-id="3fb22-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="3fb22-114">Legen Sie den Wert für **WM/MediaClassSecondaryID** auf 193c8824-4d52-4178-90bd-305240b04636 fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="3fb22-115">Legen Sie für Sprachnotizen den Wert für **WM/mediaclassprimaryid** auf 01cd0f29-da4e-4157-897b-6275d50c4f11 fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="3fb22-116">Legen Sie den Wert für **WM/MediaClassSecondaryID** auf 3a172 A13-2bd9-4831-835b-114f6a95943f fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="3fb22-117">Legen Sie den Wert für **WM/contentdistributor** auf den Schlüsselnamen für den Musikdienst fest, der den Inhalt bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="3fb22-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="3fb22-118">Legen Sie den Wert für **WM/UniqueFileIdentifier** auf die Inhalts-ID fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="3fb22-119">Auf diese Weise können Sie bestimmte Inhaltselemente zu einem späteren Zeitpunkt abrufen.</span><span class="sxs-lookup"><span data-stu-id="3fb22-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="3fb22-120">Legen Sie einen Wert für **WM/wmshadowfilesourcefiletype** fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="3fb22-121">Verwenden Sie für geschützten Inhalt das SDK für das Windows Media-Format, um das DRM-Attribut " **\_ drmHeader \_ contentid** " auf die Inhalts-ID festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3fb22-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="3fb22-122">Legen Sie für geschützten Inhalt einen Wert für **WM/wmshadowfilesourcedrmtype** fest.</span><span class="sxs-lookup"><span data-stu-id="3fb22-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fb22-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3fb22-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb22-124">**Informationen zu Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="3fb22-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="3fb22-125">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="3fb22-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 