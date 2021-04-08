---
title: VML-bwmode-Attribut
description: VML-bwmode-Attribut
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728296"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="07e52-103">VML-bwmode-Attribut</span><span class="sxs-lookup"><span data-stu-id="07e52-103">VML BWMode Attribute</span></span>

<span data-ttu-id="07e52-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="07e52-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="07e52-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="07e52-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="07e52-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="07e52-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="07e52-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="07e52-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="07e52-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="07e52-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="07e52-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="07e52-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="07e52-110">Bestimmt, wie eine Form für schwarze und weiße Ausgabegeräte dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="07e52-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="07e52-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="07e52-111">Read/write.</span></span> <span data-ttu-id="07e52-112">[Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="07e52-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="07e52-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="07e52-113">**Applies To**</span></span>

[<span data-ttu-id="07e52-114">Form</span><span class="sxs-lookup"><span data-stu-id="07e52-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="07e52-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="07e52-115">**Tag Syntax**</span></span>

<span data-ttu-id="07e52-116"><v: *Element* o:bwmode = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="07e52-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="07e52-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="07e52-117">**Remarks**</span></span>

<span data-ttu-id="07e52-118">Wenn eine Form auf einem schwarzen und weißen Drucker gedruckt oder in einer schwarzen und weißen Ansicht in einer Anwendung angezeigt wird, sind mehrere Optionen möglich.</span><span class="sxs-lookup"><span data-stu-id="07e52-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="07e52-119">Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="07e52-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="07e52-120">Der Standardwert ist " **Auto**".</span><span class="sxs-lookup"><span data-stu-id="07e52-120">The default value is **auto**.</span></span>

<span data-ttu-id="07e52-121">Wenn **Auto** angegeben ist, wird [bwnormal](msdn-online-vml-bwnormal-attribute.md) verwendet, um das Verhalten für die normale schwarz-und weiße Ausgabe zu bestimmen, und [bwpure](msdn-online-vml-bwpure-attribute.md) wird verwendet, um das Verhalten für die reine schwarz-und weiße Ausgabe zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="07e52-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="07e52-122">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="07e52-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="07e52-123">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="07e52-123">**Example**</span></span>

<span data-ttu-id="07e52-124">Der schwarze und weiße Modus der Form ist " **Auto**".</span><span class="sxs-lookup"><span data-stu-id="07e52-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 