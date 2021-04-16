---
title: Title-Attribut (Form) (VML)
description: Title-Attribut (Form) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474156"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="86b0f-103">Title-Attribut (Form) (VML)</span><span class="sxs-lookup"><span data-stu-id="86b0f-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="86b0f-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="86b0f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86b0f-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="86b0f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86b0f-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="86b0f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86b0f-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="86b0f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86b0f-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="86b0f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86b0f-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="86b0f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86b0f-110">Definiert den Text, der angezeigt wird, wenn der Mauszeiger über der Form bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="86b0f-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="86b0f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="86b0f-111">Read/write.</span></span> <span data-ttu-id="86b0f-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="86b0f-112">**String**.</span></span>

<span data-ttu-id="86b0f-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="86b0f-113">**Applies To**</span></span>

[<span data-ttu-id="86b0f-114">Form</span><span class="sxs-lookup"><span data-stu-id="86b0f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="86b0f-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="86b0f-115">**Tag Syntax**</span></span>

<span data-ttu-id="86b0f-116"><v: *Element* Title = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="86b0f-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="86b0f-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="86b0f-117">**Script Syntax**</span></span>

<span data-ttu-id="86b0f-118">*Element* . Title = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="86b0f-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="86b0f-119">*Ausdruck* = *Element*. Title</span><span class="sxs-lookup"><span data-stu-id="86b0f-119">*expression*=*element*.title</span></span>

<span data-ttu-id="86b0f-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="86b0f-120">**Remarks**</span></span>

<span data-ttu-id="86b0f-121">Das **Title** -Attribut ähnelt dem Standard-HTML- **Titel** Attribut.</span><span class="sxs-lookup"><span data-stu-id="86b0f-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="86b0f-122">Das Verhalten eines Titels ähnelt einer Microsoft Windows-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="86b0f-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="86b0f-123">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="86b0f-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="86b0f-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="86b0f-124">**Example**</span></span>

<span data-ttu-id="86b0f-125">Der Titel der Form ist "QuickInfo Display" und wird angezeigt, wenn der Mauszeiger über der Form bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="86b0f-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="86b0f-126">[Beispiel für das Titel Attribut](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86b0f-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="86b0f-127">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="86b0f-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 