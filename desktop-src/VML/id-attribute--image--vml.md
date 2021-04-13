---
title: ID-Attribut (Image) (VML)
description: ID-Attribut (Image) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390974"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="a6073-103">ID-Attribut (Image) (VML)</span><span class="sxs-lookup"><span data-stu-id="a6073-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="a6073-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a6073-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6073-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a6073-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6073-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a6073-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6073-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a6073-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6073-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6073-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6073-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6073-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6073-110">Definiert einen Namen, der einen eindeutigen Bezeichner für ein Bild bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a6073-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="a6073-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a6073-111">Read/write.</span></span> <span data-ttu-id="a6073-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="a6073-112">**String**.</span></span>

<span data-ttu-id="a6073-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="a6073-113">**Applies To**</span></span>

[<span data-ttu-id="a6073-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a6073-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a6073-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="a6073-115">**Tag Syntax**</span></span>

<span data-ttu-id="a6073-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="a6073-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="a6073-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="a6073-117">**Script Syntax**</span></span>

<span data-ttu-id="a6073-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="a6073-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="a6073-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="a6073-119">*expression*=*element*.id</span></span>

<span data-ttu-id="a6073-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="a6073-120">**Remarks**</span></span>

<span data-ttu-id="a6073-121">Verwenden Sie **ID** , um auf ein bestimmtes Image zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a6073-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="a6073-122">Nachdem Sie ein Image erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Abbild bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="a6073-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="a6073-123">**VML-Standard Attribut**</span><span class="sxs-lookup"><span data-stu-id="a6073-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="a6073-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a6073-124">**Example**</span></span>

<span data-ttu-id="a6073-125">Die Form hat eine **imagedata** -ID mit dem Namen "MyImage".</span><span class="sxs-lookup"><span data-stu-id="a6073-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 