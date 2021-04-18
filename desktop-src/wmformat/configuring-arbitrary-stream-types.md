---
title: Konfigurieren beliebiger Streamtypen
description: Konfigurieren beliebiger Streamtypen
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- Streams, konfigurieren beliebiger Streamtypen
- Codecs, konfigurieren beliebiger Streamtypen
- Streams, genprofile
- Codecs, genprofile
- Genprofile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340621"
---
# <a name="configuring-arbitrary-stream-types"></a><span data-ttu-id="56858-108">Konfigurieren beliebiger Streamtypen</span><span class="sxs-lookup"><span data-stu-id="56858-108">Configuring Arbitrary Stream Types</span></span>

<span data-ttu-id="56858-109">Die meisten willkürlichen Streamtypen benötigen nur eine Bitrate, ein Puffer Fenster und einen richtigen großen Medientyp in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="56858-109">Most arbitrary stream types just need a bit rate, a buffer window, and a proper major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="56858-110">Für einige beliebige Typen ist jedoch eine zusätzliche Konfiguration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="56858-110">However, some arbitrary types require additional configuration.</span></span>

<span data-ttu-id="56858-111">Wenn Sie Probleme beim Konfigurieren eines Streams haben, finden Sie weitere Informationen in der Beispielanwendung genprofile, die in diesem SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="56858-111">If you have trouble configuring a stream, refer to the sample application called GenProfile, which is included with this SDK.</span></span> <span data-ttu-id="56858-112">Die in genprofile definierte Bibliothek enthält Code zum Einschließen aller Arten von Streams.</span><span class="sxs-lookup"><span data-stu-id="56858-112">The library defined in GenProfile contains code for including all types of streams.</span></span> <span data-ttu-id="56858-113">Weitere Informationen zu genprofile und den anderen Beispielen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="56858-113">For more information about GenProfile and the other samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="56858-114">In den folgenden Abschnitten wird beschrieben, wie beliebige Streamtypen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="56858-114">The following sections describe how to configure arbitrary stream types.</span></span>



| <span data-ttu-id="56858-115">`Section`</span><span class="sxs-lookup"><span data-stu-id="56858-115">Section</span></span>                                                                                                                                        | <span data-ttu-id="56858-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56858-116">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56858-117">Konfigurieren von Skript Datenströmen</span><span class="sxs-lookup"><span data-stu-id="56858-117">Configuring Script Streams</span></span>](configuring-script-streams.md)                                                                                   | <span data-ttu-id="56858-118">Beschreibt das Konfigurieren von Skript Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="56858-118">Describes how to configure script streams.</span></span>                                                  |
| [<span data-ttu-id="56858-119">Konfigurieren von Datei Übertragungsdaten strömen</span><span class="sxs-lookup"><span data-stu-id="56858-119">Configuring File Transfer Streams</span></span>](configuring-file-transfer-streams.md)                                                                     | <span data-ttu-id="56858-120">Beschreibt, wie Datei Übertragungsdaten Ströme konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="56858-120">Describes how to configure file transfer streams.</span></span>                                           |
| [<span data-ttu-id="56858-121">Konfigurieren von Webstreams</span><span class="sxs-lookup"><span data-stu-id="56858-121">Configuring Web Streams</span></span>](configuring-web-streams.md)                                                                                         | <span data-ttu-id="56858-122">Beschreibt, wie Webstreams konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="56858-122">Describes how to configure Web streams.</span></span>                                                     |
| [<span data-ttu-id="56858-123">Konfigurieren von Textstreams</span><span class="sxs-lookup"><span data-stu-id="56858-123">Configuring Text Streams</span></span>](configuring-text-streams.md)                                                                                       | <span data-ttu-id="56858-124">Beschreibt das Konfigurieren von Textstreams.</span><span class="sxs-lookup"><span data-stu-id="56858-124">Describes how to configure text streams.</span></span>                                                    |
| [<span data-ttu-id="56858-125">Konfigurieren von benutzerdefinierten beliebigen Streams</span><span class="sxs-lookup"><span data-stu-id="56858-125">Configuring Custom Arbitrary Streams</span></span>](configuring-custom-arbitrary-streams.md)                                                               | <span data-ttu-id="56858-126">Beschreibt, wie Streams für benutzerdefinierte beliebige Streamtypen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="56858-126">Describes how to configure streams for custom arbitrary stream types.</span></span>                       |
| [<span data-ttu-id="56858-127">Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams</span><span class="sxs-lookup"><span data-stu-id="56858-127">Calculating Bit Rate and Buffer Window Values for Arbitrary Streams</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | <span data-ttu-id="56858-128">Beschreibt, wie die Bitraten-und Puffer Fenster Einstellungen für einen beliebigen Datenstrom berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="56858-128">Describes how to calculate the bit rate and buffer window settings for an arbitrary stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="56858-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56858-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56858-130">**Beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="56858-130">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="56858-131">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="56858-131">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




