---
title: ID-Attribut (Strich) (VML)
description: ID-Attribut (Strich) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728337"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="cea2c-103">ID-Attribut (Strich) (VML)</span><span class="sxs-lookup"><span data-stu-id="cea2c-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="cea2c-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="cea2c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cea2c-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="cea2c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cea2c-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="cea2c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cea2c-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cea2c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cea2c-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cea2c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cea2c-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cea2c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cea2c-110">Ein Name, der einen eindeutigen Bezeichner für einen Strich bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cea2c-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="cea2c-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cea2c-111">Read/write.</span></span> <span data-ttu-id="cea2c-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="cea2c-112">**String**.</span></span>

<span data-ttu-id="cea2c-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="cea2c-113">**Applies To**</span></span>

[<span data-ttu-id="cea2c-114">Stellung</span><span class="sxs-lookup"><span data-stu-id="cea2c-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="cea2c-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="cea2c-115">**Tag Syntax**</span></span>

<span data-ttu-id="cea2c-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="cea2c-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="cea2c-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="cea2c-117">**Script Syntax**</span></span>

<span data-ttu-id="cea2c-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="cea2c-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="cea2c-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="cea2c-119">*expression*=*element*.id</span></span>

<span data-ttu-id="cea2c-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="cea2c-120">**Remarks**</span></span>

<span data-ttu-id="cea2c-121">Verwenden Sie **ID** , um auf einen bestimmten Strich zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="cea2c-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="cea2c-122">Nachdem Sie einen Strich erstellt und ihm eine ID zugewiesen haben, können Sie den ID-Namen verwenden, wenn Sie den Strich bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="cea2c-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="cea2c-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="cea2c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cea2c-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="cea2c-124">**Example**</span></span>

<span data-ttu-id="cea2c-125">Die Form hat eine Strich-ID mit dem Namen "myStroke".</span><span class="sxs-lookup"><span data-stu-id="cea2c-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 