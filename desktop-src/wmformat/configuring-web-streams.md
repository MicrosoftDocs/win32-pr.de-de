---
title: Konfigurieren von Webstreams
description: Konfigurieren von Webstreams
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- Streams, Konfigurieren von Webstreams
- Codecs, Konfigurieren von Webstreams
- Webstreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311012"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="388e0-106">Konfigurieren von Webstreams</span><span class="sxs-lookup"><span data-stu-id="388e0-106">Configuring Web Streams</span></span>

<span data-ttu-id="388e0-107">Webstreams sind ein spezieller Typ von Datei Übertragungsdaten Strom, der verwendet wird, um die einer Website zugeordneten Dateien in einem einzigen Stream bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="388e0-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="388e0-108">Die Webstream-Konfiguration ist in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="388e0-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="388e0-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="388e0-109">Setting</span></span>                                            | <span data-ttu-id="388e0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="388e0-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="388e0-111">**WM \_ - \_ Medientyp. majortype**</span><span class="sxs-lookup"><span data-stu-id="388e0-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="388e0-112">Legen Sie auf wmmediatype \_ Filetransfer fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="388e0-113">**WM \_ - \_ Medientyp. Untertyp**</span><span class="sxs-lookup"><span data-stu-id="388e0-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="388e0-114">Legen Sie auf wmmediasubtype \_ Webstream fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="388e0-115">**WM \_ - \_ Medientyp. bfixedsizesamples**</span><span class="sxs-lookup"><span data-stu-id="388e0-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="388e0-116">Legen Sie auf false fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="388e0-117">**WM \_ - \_ Medientyp. btemporalcompression**</span><span class="sxs-lookup"><span data-stu-id="388e0-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="388e0-118">Legen Sie den Wert auf True fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="388e0-119">**WM \_ - \_ Medientyp. lsamplesize**</span><span class="sxs-lookup"><span data-stu-id="388e0-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="388e0-120">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="388e0-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="388e0-121">**WM \_ - \_ Medientyp. formatType**</span><span class="sxs-lookup"><span data-stu-id="388e0-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="388e0-122">Legen Sie auf wmformat \_ Webstream fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="388e0-123">**WM \_ - \_ Medientyp. Punk**</span><span class="sxs-lookup"><span data-stu-id="388e0-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="388e0-124">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="388e0-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="388e0-125">**WM \_ - \_ Medientyp. cbformat**</span><span class="sxs-lookup"><span data-stu-id="388e0-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="388e0-126">Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_FORMAT)` fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="388e0-127">**WM \_ - \_ Medientyp. pbformat**</span><span class="sxs-lookup"><span data-stu-id="388e0-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="388e0-128">Legen Sie die Adresse einer ordnungsgemäß konfigurierten **WMT- \_ Webstream- \_ Format** Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="388e0-129">**WMT- \_ Webstream- \_ Format. cbsampleheaderfixeddata**</span><span class="sxs-lookup"><span data-stu-id="388e0-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="388e0-130">Legen Sie diese Option auf `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)` fest.</span><span class="sxs-lookup"><span data-stu-id="388e0-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="388e0-131">**WMT- \_ Webstream- \_ Format. wversion**</span><span class="sxs-lookup"><span data-stu-id="388e0-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="388e0-132">Auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="388e0-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="388e0-133">**WMT- \_ Webstream- \_ Format. wReserved**</span><span class="sxs-lookup"><span data-stu-id="388e0-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="388e0-134">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="388e0-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="388e0-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="388e0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="388e0-136">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="388e0-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="388e0-137">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="388e0-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="388e0-138">**Webstreams**</span><span class="sxs-lookup"><span data-stu-id="388e0-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




