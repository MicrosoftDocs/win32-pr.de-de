---
title: VML-Attribut "fillok"
description: VML-Attribut "fillok"
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316412"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="9ca14-103">VML-Attribut "fillok"</span><span class="sxs-lookup"><span data-stu-id="9ca14-103">VML FillOK Attribute</span></span>

<span data-ttu-id="9ca14-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="9ca14-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9ca14-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9ca14-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9ca14-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="9ca14-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9ca14-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9ca14-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9ca14-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9ca14-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9ca14-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9ca14-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9ca14-110">Bestimmt, ob eine Füllung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ca14-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="9ca14-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9ca14-111">Read/write.</span></span> <span data-ttu-id="9ca14-112">**Vgder State**.</span><span class="sxs-lookup"><span data-stu-id="9ca14-112">**VgTriState**.</span></span>

<span data-ttu-id="9ca14-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="9ca14-113">**Applies To**</span></span>

[<span data-ttu-id="9ca14-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="9ca14-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="9ca14-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="9ca14-115">**Tag Syntax**</span></span>

<span data-ttu-id="9ca14-116"><v: *Element* fillok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9ca14-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="9ca14-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="9ca14-117">**Script Syntax**</span></span>

<span data-ttu-id="9ca14-118">*Element* . fillok = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="9ca14-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="9ca14-119">*Ausdruck* = *Element*. fillok</span><span class="sxs-lookup"><span data-stu-id="9ca14-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="9ca14-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="9ca14-120">**Remarks**</span></span>

<span data-ttu-id="9ca14-121">**False** gibt an, dass der Pfad nicht ausgefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ca14-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="9ca14-122">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="9ca14-122">The default is **True**.</span></span> <span data-ttu-id="9ca14-123">Dieses Attribut überschreibt alle anderen Füll Attribute im übergeordneten Element oder im **Fill** -Element.</span><span class="sxs-lookup"><span data-stu-id="9ca14-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="9ca14-124">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="9ca14-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="9ca14-125">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="9ca14-125">**Example**</span></span>

<span data-ttu-id="9ca14-126">Der Pfad wird nicht ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9ca14-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 