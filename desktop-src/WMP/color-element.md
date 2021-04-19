---
title: Color-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Color-Element
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Farb Element Fenster Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362071"
---
# <a name="color-element"></a><span data-ttu-id="a35cc-105">Color-Element</span><span class="sxs-lookup"><span data-stu-id="a35cc-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="a35cc-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="a35cc-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a35cc-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a35cc-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a35cc-108">Das Color-Element gibt die Hintergrundfarbe für die Navigations Schaltflächen des Online Stores, den Schaltflächen Text und die Features-Taskleiste an.</span><span class="sxs-lookup"><span data-stu-id="a35cc-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="a35cc-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="a35cc-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="a35cc-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**Media Player** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="a35cc-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="a35cc-111">Hexadezimal-RGB-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="a35cc-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="a35cc-112">Gibt die Hintergrundfarbe für Schaltflächen und die Taskleiste an.</span><span class="sxs-lookup"><span data-stu-id="a35cc-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="a35cc-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**Mediaplayertext** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="a35cc-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="a35cc-114">Hexadezimal-RGB-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="a35cc-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="a35cc-115">Gibt die Farbe für den Schaltflächen Text an.</span><span class="sxs-lookup"><span data-stu-id="a35cc-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="a35cc-116">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="a35cc-116">Parent/Child Elements</span></span>



| <span data-ttu-id="a35cc-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a35cc-117">Hierarchy</span></span>       | <span data-ttu-id="a35cc-118">Element</span><span class="sxs-lookup"><span data-stu-id="a35cc-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="a35cc-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a35cc-119">Parent elements</span></span> | <span data-ttu-id="a35cc-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a35cc-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="a35cc-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a35cc-121">Child elements</span></span>  | <span data-ttu-id="a35cc-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a35cc-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="a35cc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a35cc-123">Remarks</span></span>

<span data-ttu-id="a35cc-124">Der Standardwert für **Media Player** ist \# 7c9ad6.</span><span class="sxs-lookup"><span data-stu-id="a35cc-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="a35cc-125">Der Standardwert für **mediaplayertext** ist \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a35cc-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="a35cc-126">Achten Sie darauf, Farben zu verwenden, die es dem Benutzer erleichtern, den Schaltflächen Text zu lesen.</span><span class="sxs-lookup"><span data-stu-id="a35cc-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="a35cc-127">Sie sollten z. b. die Verwendung von weißem Schaltflächen Text auf hellfarbigen Schaltflächen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a35cc-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35cc-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a35cc-128">Requirements</span></span>



| <span data-ttu-id="a35cc-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a35cc-129">Requirement</span></span> | <span data-ttu-id="a35cc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a35cc-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="a35cc-131">Version</span><span class="sxs-lookup"><span data-stu-id="a35cc-131">Version</span></span><br/> | <span data-ttu-id="a35cc-132">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a35cc-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a35cc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a35cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35cc-134">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="a35cc-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="a35cc-135">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="a35cc-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a35cc-136">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="a35cc-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





