---
title: VML-INSET-Attribut
description: VML-INSET-Attribut
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101795"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="3d9ad-103">VML-INSET-Attribut</span><span class="sxs-lookup"><span data-stu-id="3d9ad-103">VML Inset Attribute</span></span>

<span data-ttu-id="3d9ad-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3d9ad-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3d9ad-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3d9ad-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3d9ad-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3d9ad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3d9ad-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3d9ad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3d9ad-110">Gibt die inneren Rand Werte für Text Feld Text an.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="3d9ad-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-111">Read/write.</span></span> <span data-ttu-id="3d9ad-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-112">**String**.</span></span>

<span data-ttu-id="3d9ad-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3d9ad-113">**Applies To**</span></span>

[<span data-ttu-id="3d9ad-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="3d9ad-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="3d9ad-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3d9ad-115">**Tag Syntax**</span></span>

<span data-ttu-id="3d9ad-116"><v: *Element* INSET = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3d9ad-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="3d9ad-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3d9ad-117">**Script Syntax**</span></span>

<span data-ttu-id="3d9ad-118">*Element* . Inset = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3d9ad-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="3d9ad-119">*Ausdruck* = *Element*. Inset</span><span class="sxs-lookup"><span data-stu-id="3d9ad-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="3d9ad-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3d9ad-120">**Remarks**</span></span>

<span data-ttu-id="3d9ad-121">Der Wert für den internen Textrand wird als Zeichenfolge angegeben, die vier Werte enthält, die jeweils durch Kommas oder Leerzeichen voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="3d9ad-122">Die Werte werden vom linken, oberen, rechten und unteren Rand des Felds festgelegt, das durch das [textboxrect](msdn-online-vml-textboxrect-attribute.md) -Attribut von **path** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="3d9ad-123">Fehlende Werte werden auf den Standardwert festgelegt, der "0,1 in, 0,05 in, 0,1 in, 0,05 in" ist.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="3d9ad-124">Für gedrehte Formen in Browsern, die keine Rotation unterstützen, wird das umgebende Feld am nächstgelegenen Vielfachen von 90 Grad ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="3d9ad-125">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3d9ad-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="3d9ad-126">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3d9ad-126">**Example**</span></span>

<span data-ttu-id="3d9ad-127">Das Textfeld enthält einen einsetenrand von 10 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="3d9ad-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 