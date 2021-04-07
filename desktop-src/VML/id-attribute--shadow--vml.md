---
title: ID-Attribut (Schatten) (VML)
description: ID-Attribut (Schatten) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728344"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="5f7ba-103">ID-Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="5f7ba-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="5f7ba-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f7ba-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f7ba-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f7ba-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f7ba-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5f7ba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f7ba-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5f7ba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f7ba-110">Gibt einen Namen an, der einen eindeutigen Bezeichner für einen Schatten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="5f7ba-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-111">Read/write.</span></span> <span data-ttu-id="5f7ba-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-112">**String**.</span></span>

<span data-ttu-id="5f7ba-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="5f7ba-113">**Applies To**</span></span>

[<span data-ttu-id="5f7ba-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="5f7ba-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="5f7ba-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="5f7ba-115">**Tag Syntax**</span></span>

<span data-ttu-id="5f7ba-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="5f7ba-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="5f7ba-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="5f7ba-117">**Script Syntax**</span></span>

<span data-ttu-id="5f7ba-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="5f7ba-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="5f7ba-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="5f7ba-119">*expression*=*element*.id</span></span>

<span data-ttu-id="5f7ba-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="5f7ba-120">**Remarks**</span></span>

<span data-ttu-id="5f7ba-121">Verwenden Sie **ID** , um auf einen bestimmten Schatten zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="5f7ba-122">Nachdem Sie einen Schatten erstellt und ihm eine ID zugewiesen haben, können Sie den ID-Namen verwenden, wenn Sie den Schatten bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="5f7ba-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="5f7ba-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="5f7ba-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5f7ba-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="5f7ba-124">**Example**</span></span>

<span data-ttu-id="5f7ba-125">Die Form hat eine Schatten-ID namens "MyShadow".</span><span class="sxs-lookup"><span data-stu-id="5f7ba-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 