---
title: ID-Attribut (VML)
description: ID-Attribut (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473477"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="10777-103">ID-Attribut (VML)</span><span class="sxs-lookup"><span data-stu-id="10777-103">ID Attribute (VML)</span></span>

<span data-ttu-id="10777-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="10777-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="10777-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="10777-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="10777-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="10777-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="10777-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="10777-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="10777-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="10777-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="10777-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="10777-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="10777-110">Stellt einen eindeutigen Bezeichner für ein Element bereit.</span><span class="sxs-lookup"><span data-stu-id="10777-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="10777-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="10777-111">Read/write.</span></span> <span data-ttu-id="10777-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="10777-112">**String**.</span></span>

<span data-ttu-id="10777-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="10777-113">**Applies To**</span></span>

<span data-ttu-id="10777-114">Alle VML-Elemente.</span><span class="sxs-lookup"><span data-stu-id="10777-114">All VML elements.</span></span>

<span data-ttu-id="10777-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="10777-115">**Tag Syntax**</span></span>

<span data-ttu-id="10777-116"><v: *ElementName* ID = " *IDName* " ></span><span class="sxs-lookup"><span data-stu-id="10777-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="10777-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="10777-117">**Script Syntax**</span></span>

<span data-ttu-id="10777-118">*ElementName* . ID = " *IDName* "</span><span class="sxs-lookup"><span data-stu-id="10777-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="10777-119">*Ausdruck* = *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="10777-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="10777-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="10777-120">**Remarks**</span></span>

<span data-ttu-id="10777-121">Verwenden Sie **ID** , um auf ein bestimmtes Element zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="10777-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="10777-122">Nachdem Sie eine Form erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Element bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="10777-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="10777-123">**ID** ist erforderlich, um das [ShapeType](msdn-online-vml-shapetype-element.md) -Element zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="10777-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="10777-124">Wenn VML durch Microsoft Office generiert wird, wird die **ID** auf diesen Namen festgelegt, wenn der Form ein Objektmodell Name zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="10777-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="10777-125">Wenn der Objektmodell Name nicht festgelegt ist, wird der Name mit der *SPID* (Internal Shape ID) und einem Präfix (en für Shape, M für die Master-Form, T für ShapeType) generiert.</span><span class="sxs-lookup"><span data-stu-id="10777-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="10777-126">*VML-Standard Attribut*.</span><span class="sxs-lookup"><span data-stu-id="10777-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="10777-127">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="10777-127">**Example**</span></span>

<span data-ttu-id="10777-128">Um die Attribute einer Form zu ändern, müssen Sie der Form zuerst eine ID zuordnen. Beispiel: "myRect".</span><span class="sxs-lookup"><span data-stu-id="10777-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="10777-129">[ID-Attribut Beispiel](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="10777-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="10777-130">(Erfordert Microsoft Internet Explorer 5 oder höher.)</span><span class="sxs-lookup"><span data-stu-id="10777-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 