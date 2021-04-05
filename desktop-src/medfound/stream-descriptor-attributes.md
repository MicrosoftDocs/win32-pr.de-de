---
description: Streamdeskriptorattribute
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Streamdeskriptorattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753841"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="5ed10-103">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="5ed10-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="5ed10-104">Allgemeine streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="5ed10-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="5ed10-105">Die folgenden Attribute gelten für streamdeskriptoren.</span><span class="sxs-lookup"><span data-stu-id="5ed10-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="5ed10-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ed10-106">Attribute</span></span>                                                   | <span data-ttu-id="5ed10-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ed10-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed10-108">**MF \_ SD- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="5ed10-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="5ed10-109">Gibt die Sprache für einen Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="5ed10-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="5ed10-110">MF- \_ SD \_ gegenseitig \_ ausschließen</span><span class="sxs-lookup"><span data-stu-id="5ed10-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="5ed10-111">Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt.</span><span class="sxs-lookup"><span data-stu-id="5ed10-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="5ed10-112">**MF \_ SD- \_ geschützt**</span><span class="sxs-lookup"><span data-stu-id="5ed10-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="5ed10-113">Gibt an, ob ein Stream geschützte Inhalte enthält.</span><span class="sxs-lookup"><span data-stu-id="5ed10-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="5ed10-114">MF-SD-Daten \_ \_ Strom \_ Name</span><span class="sxs-lookup"><span data-stu-id="5ed10-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="5ed10-115">Enthält den Namen eines Streams.</span><span class="sxs-lookup"><span data-stu-id="5ed10-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="5ed10-116">Attribute des ASF-Specific Stream-Deskriptors</span><span class="sxs-lookup"><span data-stu-id="5ed10-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="5ed10-117">Die folgenden Attribute gelten für streamdeskriptoren für ASF-Dateien (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5ed10-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="5ed10-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ed10-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="5ed10-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ed10-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed10-120">**MF \_ SD \_ ASF \_ extstraumprop \_ AVG \_ bufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ed10-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="5ed10-121">Gibt die durchschnittliche Puffergröße an, die für einen Datenstrom in einer ASF-Datei (in Bytes) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5ed10-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="5ed10-122">**MF SD-Datei (in Bytes) \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ed10-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="5ed10-123">Gibt die durchschnittliche Daten Bitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="5ed10-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="5ed10-124">**MF \_ SD \_ - \_ Datei-ID der extstrinmprop- \_ Sprache \_ ID \_ Index**</span><span class="sxs-lookup"><span data-stu-id="5ed10-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="5ed10-125">Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ed10-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="5ed10-126">**MF \_ SD. \_ ASF \_ extstraumprop \_ Max \_ bufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ed10-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="5ed10-127">Gibt die maximale Puffergröße an, die für einen Datenstrom in einer ASF-Datei (in Bytes) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5ed10-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="5ed10-128">**MF \_ SD \_ , \_ \_ maximal zulässige \_ Daten \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="5ed10-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="5ed10-129">Gibt die maximale datenbitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="5ed10-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="5ed10-130">**Vorlage für die \_ Geräte Konformität der MF SD- \_ \_ \_ metadatengeräte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ed10-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="5ed10-131">Gibt die Geräte Konformitäts Vorlage für einen Datenstrom in einer ASF-Datei in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="5ed10-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="5ed10-132">**MF \_ SD, \_ ASF \_ streambitraten \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="5ed10-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="5ed10-133">Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="5ed10-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="5ed10-134">Deskriptorattribute des Sami-Medien-Quelldaten Stroms</span><span class="sxs-lookup"><span data-stu-id="5ed10-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="5ed10-135">Das folgende Attribut gilt für den Datenstrom Deskriptor für die Sami Media-Quelle.</span><span class="sxs-lookup"><span data-stu-id="5ed10-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="5ed10-136">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ed10-136">Attribute</span></span>                                                       | <span data-ttu-id="5ed10-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ed10-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ed10-138">**MF, \_ SD, \_ Samisch \_**</span><span class="sxs-lookup"><span data-stu-id="5ed10-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="5ed10-139">Enthält den für den Stream definierten Sami-Sprachnamen (für den verfügbaren Medienaustausch).</span><span class="sxs-lookup"><span data-stu-id="5ed10-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5ed10-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ed10-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed10-141">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="5ed10-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="5ed10-142">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5ed10-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



