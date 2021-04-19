---
title: IWMPMetadataPicture-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften bereit, mit denen Informationen zu dem Bild, das in einer digitalen Mediendatei enthalten ist, die durch ein WM/picturemetadata-Attribut dargestellt wird, erhalten.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB und C) Interface Windows Media Player
- IWMPMetadataPicture (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352067"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="55fbf-105">IWMPMetadataPicture-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="55fbf-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="55fbf-106">Stellt Eigenschaften bereit, mit denen Informationen zu dem Bild, das in einer digitalen Mediendatei enthalten ist, die durch ein [**WM/Bild-**](/windows/desktop/wmformat/wmpicture)Metadatenattribut dargestellt wird, erhalten</span><span class="sxs-lookup"><span data-stu-id="55fbf-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="55fbf-107">Dieses Attribut entspricht Albumkunst Bildern, die in einer digitalen Mediendatei enthalten sind, und nicht in albumgrafiken, die über das Internet heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="55fbf-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="55fbf-108">Die **IWMPMetadataPicture** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="55fbf-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="55fbf-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55fbf-109">Property</span></span>                                                                                   | <span data-ttu-id="55fbf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55fbf-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="55fbf-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55fbf-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="55fbf-112">Ruft die Beschreibung des Bilds ab, das durch das Metadatenattribut dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55fbf-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="55fbf-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="55fbf-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="55fbf-114">Ruft den MIME-Typ des Bilds ab, das durch das Metadatenattribut dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55fbf-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="55fbf-115">**PictureType**</span><span class="sxs-lookup"><span data-stu-id="55fbf-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="55fbf-116">Ruft den Bildtyp des Bilds ab, das durch das Metadatenattribut dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55fbf-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="55fbf-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="55fbf-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="55fbf-118">Nur interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="55fbf-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="55fbf-119">Sie erhalten eine **IWMPMetadataPicture** -Schnittstelle, indem Sie den Attributnamen [**WM/Bild**](/windows/desktop/wmformat/wmpicture) an die folgende Methode übergeben und das zurückgegebene Objekt umwandeln.</span><span class="sxs-lookup"><span data-stu-id="55fbf-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="55fbf-120">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="55fbf-120">Interface</span></span>                                  | <span data-ttu-id="55fbf-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55fbf-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="55fbf-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="55fbf-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="55fbf-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="55fbf-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="55fbf-124">Member</span><span class="sxs-lookup"><span data-stu-id="55fbf-124">Members</span></span>

<span data-ttu-id="55fbf-125">Die **IWMPMetadataPicture-Schnittstelle (VB und c#)** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="55fbf-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="55fbf-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55fbf-126">Requirements</span></span>



| <span data-ttu-id="55fbf-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55fbf-127">Requirement</span></span> | <span data-ttu-id="55fbf-128">Wert</span><span class="sxs-lookup"><span data-stu-id="55fbf-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55fbf-129">Header</span><span class="sxs-lookup"><span data-stu-id="55fbf-129">Header</span></span><br/> | <dl> <span data-ttu-id="55fbf-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="55fbf-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55fbf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55fbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55fbf-132">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="55fbf-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

