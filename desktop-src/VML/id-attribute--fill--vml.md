---
title: ID-Attribut (Fill) (VML)
description: ID-Attribut (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039264"
---
# <a name="id-attribute-fillvml"></a><span data-ttu-id="229ed-103">ID-Attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="229ed-103">ID Attribute (Fill)(VML)</span></span>

<span data-ttu-id="229ed-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="229ed-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="229ed-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="229ed-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="229ed-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="229ed-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="229ed-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="229ed-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="229ed-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="229ed-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="229ed-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="229ed-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="229ed-110">Ein Name, der einen eindeutigen Bezeichner für eine Füllung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="229ed-110">A name that provides a unique identifier for a fill.</span></span> <span data-ttu-id="229ed-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="229ed-111">Read/write.</span></span> <span data-ttu-id="229ed-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="229ed-112">**String**.</span></span>

<span data-ttu-id="229ed-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="229ed-113">**Applies To**</span></span>

[<span data-ttu-id="229ed-114">Ausfüllen</span><span class="sxs-lookup"><span data-stu-id="229ed-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="229ed-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="229ed-115">**Tag Syntax**</span></span>

<span data-ttu-id="229ed-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="229ed-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="229ed-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="229ed-117">**Script Syntax**</span></span>

<span data-ttu-id="229ed-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="229ed-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="229ed-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="229ed-119">*expression*=*element*.id</span></span>

<span data-ttu-id="229ed-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="229ed-120">**Remarks**</span></span>

<span data-ttu-id="229ed-121">Verwenden Sie **ID** , um auf eine bestimmte Füllung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="229ed-121">Use **ID** to refer to a specific fill.</span></span> <span data-ttu-id="229ed-122">Nachdem Sie eine Füllung erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie die Füllung bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="229ed-122">Once you have created a fill and given it an ID, you can use the ID name when you want to manipulate the fill.</span></span>

<span data-ttu-id="229ed-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="229ed-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="229ed-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="229ed-124">**Example**</span></span>

<span data-ttu-id="229ed-125">Die Form hat eine Fill-ID mit dem Namen "myfill".</span><span class="sxs-lookup"><span data-stu-id="229ed-125">The shape has a fill ID called "myfill".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 