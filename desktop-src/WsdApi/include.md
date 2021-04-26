---
description: Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995777"
---
# <a name="include-element"></a><span data-ttu-id="f3042-103">include-Element</span><span class="sxs-lookup"><span data-stu-id="f3042-103">include element</span></span>

<span data-ttu-id="f3042-104">Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.</span><span class="sxs-lookup"><span data-stu-id="f3042-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="f3042-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f3042-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="f3042-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3042-106">Attributes</span></span>



| <span data-ttu-id="f3042-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3042-107">Attribute</span></span>            | <span data-ttu-id="f3042-108">type</span><span class="sxs-lookup"><span data-stu-id="f3042-108">Type</span></span>                         | <span data-ttu-id="f3042-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f3042-109">Required</span></span>      | <span data-ttu-id="f3042-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3042-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="f3042-111">**datei**</span><span class="sxs-lookup"><span data-stu-id="f3042-111">**file**</span></span><br/>  | <span data-ttu-id="f3042-112">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f3042-112">character\_string</span></span><br/> | <span data-ttu-id="f3042-113">Nein</span><span class="sxs-lookup"><span data-stu-id="f3042-113">No</span></span><br/> | <span data-ttu-id="f3042-114">Der Pfad zu der datei, die enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="f3042-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="f3042-115">**Makro**</span><span class="sxs-lookup"><span data-stu-id="f3042-115">**macro**</span></span><br/> | <span data-ttu-id="f3042-116">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f3042-116">character\_string</span></span><br/> | <span data-ttu-id="f3042-117">Nein</span><span class="sxs-lookup"><span data-stu-id="f3042-117">No</span></span><br/> | <span data-ttu-id="f3042-118">Der Name des makros, das enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="f3042-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="f3042-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3042-119">Child elements</span></span>

<span data-ttu-id="f3042-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="f3042-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f3042-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3042-121">Parent elements</span></span>



| <span data-ttu-id="f3042-122">Element</span><span class="sxs-lookup"><span data-stu-id="f3042-122">Element</span></span>                         | <span data-ttu-id="f3042-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3042-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3042-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f3042-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f3042-125">Leitet den Codegenerator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.</span><span class="sxs-lookup"><span data-stu-id="f3042-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f3042-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3042-126">Remarks</span></span>

<span data-ttu-id="f3042-127">Entweder das **Makroattribut** oder **das Dateiattribut** muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3042-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="f3042-128">Geben Sie nicht beide Attribute an.</span><span class="sxs-lookup"><span data-stu-id="f3042-128">Do not specify both attributes.</span></span>

<span data-ttu-id="f3042-129">WsdCodeGen definiert ein Makro mit dem Namen **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="f3042-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="f3042-130">Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweisen soll, den generierten Code nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f3042-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="f3042-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3042-131">Examples</span></span>

<span data-ttu-id="f3042-132">Der folgende XML-Code zeigt, wie das **DoNotModify-Makro enthalten** ist.</span><span class="sxs-lookup"><span data-stu-id="f3042-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="f3042-133">Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3042-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="f3042-134">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f3042-134">Element information</span></span>



| <span data-ttu-id="f3042-135">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f3042-135">Label</span></span> | <span data-ttu-id="f3042-136">Wert</span><span class="sxs-lookup"><span data-stu-id="f3042-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f3042-137">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="f3042-137">Minimum supported system</span></span><br/> | <span data-ttu-id="f3042-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3042-138">Windows Vista</span></span> |
| <span data-ttu-id="f3042-139">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="f3042-139">Can be empty</span></span>                        | <span data-ttu-id="f3042-140">Ja</span><span class="sxs-lookup"><span data-stu-id="f3042-140">Yes</span></span>           |



 

 




