---
title: ADJ-Attribut
description: ADJ-Attribut
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339496"
---
# <a name="adj-attribute"></a><span data-ttu-id="ec258-103">ADJ-Attribut</span><span class="sxs-lookup"><span data-stu-id="ec258-103">Adj Attribute</span></span>

<span data-ttu-id="ec258-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="ec258-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec258-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="ec258-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec258-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="ec258-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec258-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ec258-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec258-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ec258-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec258-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ec258-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec258-110">Gibt einen Anpassungswert an, der verwendet wird, um Werte für eine Formel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ec258-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="ec258-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ec258-111">Read/write.</span></span> <span data-ttu-id="ec258-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="ec258-112">**String**.</span></span>

<span data-ttu-id="ec258-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ec258-113">**Applies To**</span></span>

[<span data-ttu-id="ec258-114">Form</span><span class="sxs-lookup"><span data-stu-id="ec258-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ec258-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="ec258-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec258-116"><v: *Element* adj = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ec258-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="ec258-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="ec258-117">**Script Syntax**</span></span>

<span data-ttu-id="ec258-118">*Element* . adj = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="ec258-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="ec258-119">*Ausdruck* = *Element*. ADJ</span><span class="sxs-lookup"><span data-stu-id="ec258-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="ec258-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ec258-120">**Remarks**</span></span>

<span data-ttu-id="ec258-121">**ADJ** dient zum Bereitstellen von anpassbaren Punkten für eine Formel.</span><span class="sxs-lookup"><span data-stu-id="ec258-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="ec258-122">Bei Verwendung in Tags ist **ADJ** eine durch Trennzeichen getrennte Zeichenfolge mit bis zu acht Werten.</span><span class="sxs-lookup"><span data-stu-id="ec258-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="ec258-123">Einige Werte werden möglicherweise ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="ec258-123">Some values may be omitted.</span></span> <span data-ttu-id="ec258-124">Beispielsweise ist "0, 1, 2,, 4, 5,, 7" eine gültige Zeichenfolge, aber das vierte und das siebte Element enthalten keine Werte (Elemente werden beginnend mit 0 gezählt).</span><span class="sxs-lookup"><span data-stu-id="ec258-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="ec258-125">Bei der Skripterstellung verwendet **ADJ** den [ivganpassungen](msdn-online-vml-ivgadjustments-data-type.md) -Datentyp.</span><span class="sxs-lookup"><span data-stu-id="ec258-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="ec258-126">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="ec258-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec258-127">**Siehe auch**</span><span class="sxs-lookup"><span data-stu-id="ec258-127">**See Also**</span></span>

[<span data-ttu-id="ec258-128">Formel</span><span class="sxs-lookup"><span data-stu-id="ec258-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="ec258-129">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="ec258-129">**Example**</span></span>

<span data-ttu-id="ec258-130">Ein einfaches Quadrat wird mit Anpassungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec258-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="ec258-131">Zuerst wird die **ADJ** -Zeichenfolge erstellt, um acht Anpassungs Werte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ec258-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="ec258-132">Dann wird auf jeden Anpassungswert durch eine der acht Formeln verwiesen, wobei jeder Anpassungswert durch ein Nummern Zeichen () vorangestellt wird \# .</span><span class="sxs-lookup"><span data-stu-id="ec258-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="ec258-133">Schließlich wird ein Pfad durch eine Zeichenfolge definiert, die auf die Formeln verweist, wobei jeder Formel das Zeichen "at" (@) vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="ec258-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="ec258-134">[ADJ-Attribut Beispiel](/previous-versions/bb229662(v=vs.85)) (erfordert Microsoft Internet Explorer 5 oder höher)</span><span class="sxs-lookup"><span data-stu-id="ec258-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 