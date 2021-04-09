---
title: VML-Master Attribut
description: VML-Master Attribut
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102315"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="6ac3c-103">VML-Master Attribut</span><span class="sxs-lookup"><span data-stu-id="6ac3c-103">VML Master Attribute</span></span>

<span data-ttu-id="6ac3c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6ac3c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6ac3c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6ac3c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6ac3c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6ac3c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6ac3c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6ac3c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6ac3c-110">Bestimmt, ob ein **ShapeType** -Element ein Master Element ist.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="6ac3c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-111">Read/write.</span></span> <span data-ttu-id="6ac3c-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-112">**VgTriState**.</span></span>

<span data-ttu-id="6ac3c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="6ac3c-113">**Applies To**</span></span>

[<span data-ttu-id="6ac3c-114">ShapeType</span><span class="sxs-lookup"><span data-stu-id="6ac3c-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="6ac3c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="6ac3c-115">**Tag Syntax**</span></span>

<span data-ttu-id="6ac3c-116"><v: *Element* o:Master = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="6ac3c-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="6ac3c-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="6ac3c-117">**Remarks**</span></span>

<span data-ttu-id="6ac3c-118">**True** gibt an, dass die Form **ShapeType** von der Rendering-Engine gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="6ac3c-119">Der Standardwert ist **False**.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-119">The default value is **False**.</span></span>

<span data-ttu-id="6ac3c-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="6ac3c-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="6ac3c-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="6ac3c-121">**Example**</span></span>

<span data-ttu-id="6ac3c-122">Das **ShapeType** -Element ist eine masterform.</span><span class="sxs-lookup"><span data-stu-id="6ac3c-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 