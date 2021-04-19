---
description: ASF-Attribute
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: ASF-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345642"
---
# <a name="asf-attributes"></a><span data-ttu-id="e4f66-103">ASF-Attribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="e4f66-104">Profil Attribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-104">Profile Attributes</span></span>

<span data-ttu-id="e4f66-105">Die folgenden Attribute gelten für ASF-Profile.</span><span class="sxs-lookup"><span data-stu-id="e4f66-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="e4f66-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="e4f66-106">Attribute</span></span>                                                                      | <span data-ttu-id="e4f66-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f66-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e4f66-108">**MF \_ asfprofile \_ MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="e4f66-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="e4f66-109">Gibt die maximale Paketgröße für eine ASF-Datei in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="e4f66-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="e4f66-110">**MF \_ asfprofile \_ MinPacketSize**</span><span class="sxs-lookup"><span data-stu-id="e4f66-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="e4f66-111">Gibt die minimale Paketgröße für eine ASF-Datei in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="e4f66-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="e4f66-112">Stream-Konfigurations Attribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="e4f66-113">Die folgenden Attribute gelten für das Konfigurationsobjekt des ASF-Streams.</span><span class="sxs-lookup"><span data-stu-id="e4f66-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="e4f66-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="e4f66-114">Attribute</span></span>                                                                              | <span data-ttu-id="e4f66-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f66-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f66-116">**MF \_ asfstreamconfig \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="e4f66-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="e4f66-117">Legt die durchschnittlichen "Leaky Bucket"-Parameter für das Codieren einer Windows-Mediendatei fest.</span><span class="sxs-lookup"><span data-stu-id="e4f66-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="e4f66-118">**MF \_ asfstreamconfig \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="e4f66-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="e4f66-119">Legt die Spitzen Parameter "Leaky Bucket" für das Codieren einer Windows-Mediendatei fest.</span><span class="sxs-lookup"><span data-stu-id="e4f66-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="e4f66-120">Medien Puffer Attribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-120">Media Buffer Attributes</span></span>

<span data-ttu-id="e4f66-121">Die folgenden Attribute gelten für Medien Puffer für ASF-Pakete.</span><span class="sxs-lookup"><span data-stu-id="e4f66-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="e4f66-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="e4f66-122">Attribute</span></span>                                                                          | <span data-ttu-id="e4f66-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4f66-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f66-124">**mfastsplitter- \_ Paket \_ Grenze**</span><span class="sxs-lookup"><span data-stu-id="e4f66-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="e4f66-125">Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält.</span><span class="sxs-lookup"><span data-stu-id="e4f66-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="e4f66-126">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="e4f66-127">Eine Liste der Attribute, die für die ASF-Präsentations Deskriptoren gelten, finden Sie unter [Präsentations deskriptorattribute](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e4f66-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4f66-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4f66-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f66-129">**Imfasf profile**</span><span class="sxs-lookup"><span data-stu-id="e4f66-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="e4f66-130">**Imfasf streamconfig**</span><span class="sxs-lookup"><span data-stu-id="e4f66-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="e4f66-131">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e4f66-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



