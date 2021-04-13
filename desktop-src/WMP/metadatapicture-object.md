---
title: MetadataPicture-Objekt
description: Das MetadataPicture-Objekt bietet eine Möglichkeit zum Abrufen der Werte des WM/Bild-metadatenattributs. Dieses Attribut entspricht der in einer digitalen Mediendatei enthaltenen Albumkunst, nicht der über das Internet heruntergeladenen Albumkunst.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473933"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="c131d-105">MetadataPicture-Objekt</span><span class="sxs-lookup"><span data-stu-id="c131d-105">MetadataPicture Object</span></span>

<span data-ttu-id="c131d-106">Das **MetadataPicture** -Objekt bietet eine Möglichkeit zum Abrufen der Werte des [**WM/Bild-**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadatenattributs.</span><span class="sxs-lookup"><span data-stu-id="c131d-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="c131d-107">Dieses Attribut entspricht der in einer digitalen Mediendatei enthaltenen Albumkunst, nicht der über das Internet heruntergeladenen Albumkunst.</span><span class="sxs-lookup"><span data-stu-id="c131d-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="c131d-108">Das **MetadataPicture** -Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c131d-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="c131d-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c131d-109">Property</span></span>                                           | <span data-ttu-id="c131d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c131d-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="c131d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c131d-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="c131d-112">Ruft eine Beschreibung des metadatenbilds ab.</span><span class="sxs-lookup"><span data-stu-id="c131d-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="c131d-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="c131d-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="c131d-114">Ruft den MIME-Typ des metadatenbilds ab.</span><span class="sxs-lookup"><span data-stu-id="c131d-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="c131d-115">**PictureType**</span><span class="sxs-lookup"><span data-stu-id="c131d-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="c131d-116">Ruft den Bildtyp des metadatenbilds ab.</span><span class="sxs-lookup"><span data-stu-id="c131d-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="c131d-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="c131d-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="c131d-118">Nur interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c131d-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="c131d-119">Der Zugriff auf das **MetadataPicture** -Objekt erfolgt über die folgende Methode.</span><span class="sxs-lookup"><span data-stu-id="c131d-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="c131d-120">Object</span><span class="sxs-lookup"><span data-stu-id="c131d-120">Object</span></span>                        | <span data-ttu-id="c131d-121">Methode</span><span class="sxs-lookup"><span data-stu-id="c131d-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="c131d-122">**Medien**</span><span class="sxs-lookup"><span data-stu-id="c131d-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="c131d-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="c131d-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="c131d-124">Zur Veranschaulichung `player.currentMedia.getItemInfoByType(name, language, index)` wird in den Abschnitten der Verweis Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="c131d-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="c131d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c131d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c131d-126">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="c131d-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 