---
title: ID-Attribut (Textfeld) (VML)
description: ID-Attribut (Textfeld) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858332"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="0c9f2-103">ID-Attribut (Textfeld) (VML)</span><span class="sxs-lookup"><span data-stu-id="0c9f2-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="0c9f2-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0c9f2-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0c9f2-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0c9f2-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0c9f2-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0c9f2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0c9f2-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0c9f2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0c9f2-110">Ein Name, der einen eindeutigen Bezeichner für ein TextBox-Steuer Tool bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="0c9f2-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-111">Read/write.</span></span> <span data-ttu-id="0c9f2-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-112">**String**.</span></span>

<span data-ttu-id="0c9f2-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="0c9f2-113">**Applies To**</span></span>

[<span data-ttu-id="0c9f2-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="0c9f2-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="0c9f2-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="0c9f2-115">**Tag Syntax**</span></span>

<span data-ttu-id="0c9f2-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="0c9f2-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="0c9f2-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="0c9f2-117">**Script Syntax**</span></span>

<span data-ttu-id="0c9f2-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="0c9f2-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="0c9f2-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="0c9f2-119">*expression*=*element*.id</span></span>

<span data-ttu-id="0c9f2-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="0c9f2-120">**Remarks**</span></span>

<span data-ttu-id="0c9f2-121">Verwenden Sie **ID** , um auf ein bestimmtes Textfeld zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="0c9f2-122">Nachdem Sie ein Textfeld erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Textfeld bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="0c9f2-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="0c9f2-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="0c9f2-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0c9f2-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="0c9f2-124">**Example**</span></span>

<span data-ttu-id="0c9f2-125">Die Form hat eine Textfeld-ID mit dem Namen "MyTextBox".</span><span class="sxs-lookup"><span data-stu-id="0c9f2-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 