---
title: Konfigurieren von Textstreams
description: Konfigurieren von Textstreams
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- Streams, Konfigurieren von Textstreams
- Codecs, Konfigurieren von Textstreams
- Textstreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471301"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="7176b-106">Konfigurieren von Textstreams</span><span class="sxs-lookup"><span data-stu-id="7176b-106">Configuring Text Streams</span></span>

<span data-ttu-id="7176b-107">Textstreams entsprechen im Wesentlichen den benutzerdefinierten beliebigen Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="7176b-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="7176b-108">Einem Textstream sind keine Konfigurationsinformationen zugeordnet, um den Typ der Text Codierung zu identifizieren, sodass das Writer-Objekt keine Beispiele überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="7176b-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="7176b-109">Um einen Textstream zu konfigurieren, müssen Sie sicherstellen, dass die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur einen wichtigen Medientyp von wmmediatype \_ Text enthält.</span><span class="sxs-lookup"><span data-stu-id="7176b-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="7176b-110">Außerdem müssen Sie für den Stream eine Bitrate und ein Puffer Fenster festlegen.</span><span class="sxs-lookup"><span data-stu-id="7176b-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7176b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7176b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7176b-112">**Berechnen von Bitraten-und Puffer Fenster Werten für beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="7176b-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="7176b-113">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="7176b-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="7176b-114">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="7176b-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="7176b-115">**Textstreams**</span><span class="sxs-lookup"><span data-stu-id="7176b-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




