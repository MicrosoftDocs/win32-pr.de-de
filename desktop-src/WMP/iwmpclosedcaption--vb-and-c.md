---
title: Iwmpclosedcaption (VB und C)-Schnittstelle (WMP. h)
description: Bietet eine Möglichkeit zum Einschließen von Untertiteln in eine digitale Mediendatei. Der Beschriftungs Text befindet sich in einer synchronisierten, zugänglichen Medienaustausch Datei (Sami).
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- Iwmpclosedcaption (VB und C) Interface Windows Media Player
- Iwmpclosedcaption (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351324"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="82aaf-106">Iwmpclosedcaption-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="82aaf-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="82aaf-107">Bietet eine Möglichkeit zum Einschließen von Untertiteln in eine digitale Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="82aaf-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="82aaf-108">Der Beschriftungs Text befindet sich in einer synchronisierten, zugänglichen Medienaustausch Datei (Sami).</span><span class="sxs-lookup"><span data-stu-id="82aaf-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="82aaf-109">Member</span><span class="sxs-lookup"><span data-stu-id="82aaf-109">Members</span></span>

<span data-ttu-id="82aaf-110">Die **iwmpclosedcaption (VB und c#)** -Schnittstelle definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="82aaf-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="82aaf-111">Die **iwmpclosedcaption** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82aaf-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="82aaf-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82aaf-112">Property</span></span>                                                                             | <span data-ttu-id="82aaf-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82aaf-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82aaf-114">captioningid</span><span class="sxs-lookup"><span data-stu-id="82aaf-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="82aaf-115">Ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="82aaf-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="82aaf-116">Samifilename</span><span class="sxs-lookup"><span data-stu-id="82aaf-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="82aaf-117">Ruft den Namen der Datei ab, die die für den Untertitel erforderlichen Informationen enthält, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="82aaf-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="82aaf-118">Samilang</span><span class="sxs-lookup"><span data-stu-id="82aaf-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="82aaf-119">Ruft die für Untertitel angezeigte Sprache ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="82aaf-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="82aaf-120">Samistyle</span><span class="sxs-lookup"><span data-stu-id="82aaf-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="82aaf-121">Ruft den Untertitel Stil ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="82aaf-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="82aaf-122">Verwenden Sie die folgende Eigenschaft, um eine **iwmpclosedcaption** -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="82aaf-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="82aaf-123">Object</span><span class="sxs-lookup"><span data-stu-id="82aaf-123">Object</span></span>                                                            | <span data-ttu-id="82aaf-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82aaf-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="82aaf-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="82aaf-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="82aaf-126">closedcaption</span><span class="sxs-lookup"><span data-stu-id="82aaf-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="82aaf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82aaf-127">Requirements</span></span>



| <span data-ttu-id="82aaf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82aaf-128">Requirement</span></span> | <span data-ttu-id="82aaf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="82aaf-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="82aaf-130">Header</span><span class="sxs-lookup"><span data-stu-id="82aaf-130">Header</span></span><br/> | <dl> <span data-ttu-id="82aaf-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="82aaf-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82aaf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82aaf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82aaf-133">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="82aaf-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="82aaf-134">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="82aaf-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="82aaf-135">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="82aaf-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





