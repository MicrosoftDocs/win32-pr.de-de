---
title: ID-Attribut (Pfad) (VML)
description: ID-Attribut (Pfad) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101666"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="334ba-103">ID-Attribut (Pfad) (VML)</span><span class="sxs-lookup"><span data-stu-id="334ba-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="334ba-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="334ba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="334ba-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="334ba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="334ba-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="334ba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="334ba-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="334ba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="334ba-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="334ba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="334ba-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="334ba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="334ba-110">Ein Name, der einen eindeutigen Bezeichner für einen Pfad bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="334ba-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="334ba-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="334ba-111">Read/write.</span></span> <span data-ttu-id="334ba-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="334ba-112">**String**.</span></span>

<span data-ttu-id="334ba-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="334ba-113">**Applies To**</span></span>

[<span data-ttu-id="334ba-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="334ba-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="334ba-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="334ba-115">**Tag Syntax**</span></span>

<span data-ttu-id="334ba-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="334ba-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="334ba-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="334ba-117">**Script Syntax**</span></span>

<span data-ttu-id="334ba-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="334ba-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="334ba-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="334ba-119">*expression*=*element*.id</span></span>

<span data-ttu-id="334ba-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="334ba-120">**Remarks**</span></span>

<span data-ttu-id="334ba-121">Verwenden Sie **ID** , um auf einen bestimmten Pfad zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="334ba-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="334ba-122">Nachdem Sie einen Pfad erstellt und ihm eine ID zugewiesen haben, können Sie den ID-Namen verwenden, wenn Sie den Pfad bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="334ba-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="334ba-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="334ba-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="334ba-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="334ba-124">**Example**</span></span>

<span data-ttu-id="334ba-125">Die Form hat eine Pfad-ID mit dem Namen "myPath".</span><span class="sxs-lookup"><span data-stu-id="334ba-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 