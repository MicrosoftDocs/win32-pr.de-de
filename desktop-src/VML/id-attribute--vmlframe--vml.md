---
title: ID-Attribut (vmlframe) (VML)
description: ID-Attribut (vmlframe) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039204"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="1c7e8-103">ID-Attribut (vmlframe) (VML)</span><span class="sxs-lookup"><span data-stu-id="1c7e8-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="1c7e8-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c7e8-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c7e8-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c7e8-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c7e8-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1c7e8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c7e8-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1c7e8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c7e8-110">Definiert einen eindeutigen Bezeichner für den Frame.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="1c7e8-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-111">Read/write.</span></span> <span data-ttu-id="1c7e8-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-112">**String**.</span></span>

<span data-ttu-id="1c7e8-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="1c7e8-113">**Applies To**</span></span>

[<span data-ttu-id="1c7e8-114">Vmlframe</span><span class="sxs-lookup"><span data-stu-id="1c7e8-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="1c7e8-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="1c7e8-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c7e8-116"><v: *Element* -ID = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="1c7e8-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="1c7e8-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="1c7e8-117">**Script Syntax**</span></span>

<span data-ttu-id="1c7e8-118">*Element* . ID = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="1c7e8-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="1c7e8-119">*Ausdruck* = *Element*. ID</span><span class="sxs-lookup"><span data-stu-id="1c7e8-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="1c7e8-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="1c7e8-120">**Remarks**</span></span>

<span data-ttu-id="1c7e8-121">Verwenden Sie die **ID** , um auf einen Frame zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="1c7e8-122">Beispielsweise können Sie den Frame auf der Seite bewegen, indem Sie die Frame Position ändern, auf die die **ID** verweist.</span><span class="sxs-lookup"><span data-stu-id="1c7e8-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="1c7e8-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="1c7e8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1c7e8-124">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="1c7e8-124">**Example**</span></span>

<span data-ttu-id="1c7e8-125">Die **ID** des Frames ist "frame01".</span><span class="sxs-lookup"><span data-stu-id="1c7e8-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 