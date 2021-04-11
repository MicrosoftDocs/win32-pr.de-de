---
description: Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042679"
---
# <a name="include-element"></a><span data-ttu-id="d07d6-103">include-Element</span><span class="sxs-lookup"><span data-stu-id="d07d6-103">include element</span></span>

<span data-ttu-id="d07d6-104">Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.</span><span class="sxs-lookup"><span data-stu-id="d07d6-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="d07d6-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d07d6-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="d07d6-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d07d6-106">Attributes</span></span>



| <span data-ttu-id="d07d6-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="d07d6-107">Attribute</span></span>            | <span data-ttu-id="d07d6-108">type</span><span class="sxs-lookup"><span data-stu-id="d07d6-108">Type</span></span>                         | <span data-ttu-id="d07d6-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d07d6-109">Required</span></span>      | <span data-ttu-id="d07d6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d07d6-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="d07d6-111">**datei**</span><span class="sxs-lookup"><span data-stu-id="d07d6-111">**file**</span></span><br/>  | <span data-ttu-id="d07d6-112">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="d07d6-112">character\_string</span></span><br/> | <span data-ttu-id="d07d6-113">Nein</span><span class="sxs-lookup"><span data-stu-id="d07d6-113">No</span></span><br/> | <span data-ttu-id="d07d6-114">Der Pfad zu der Datei, die eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d07d6-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="d07d6-115">**Hilfen**</span><span class="sxs-lookup"><span data-stu-id="d07d6-115">**macro**</span></span><br/> | <span data-ttu-id="d07d6-116">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="d07d6-116">character\_string</span></span><br/> | <span data-ttu-id="d07d6-117">Nein</span><span class="sxs-lookup"><span data-stu-id="d07d6-117">No</span></span><br/> | <span data-ttu-id="d07d6-118">Der Name des einzuschließenden Makros.</span><span class="sxs-lookup"><span data-stu-id="d07d6-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="d07d6-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d07d6-119">Child elements</span></span>

<span data-ttu-id="d07d6-120">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d07d6-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d07d6-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d07d6-121">Parent elements</span></span>



| <span data-ttu-id="d07d6-122">Element</span><span class="sxs-lookup"><span data-stu-id="d07d6-122">Element</span></span>                         | <span data-ttu-id="d07d6-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d07d6-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d07d6-124">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d07d6-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d07d6-125">Weist den Code Generator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.</span><span class="sxs-lookup"><span data-stu-id="d07d6-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d07d6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d07d6-126">Remarks</span></span>

<span data-ttu-id="d07d6-127">Es muss entweder das **Macro** -Attribut oder das **File** -Attribut angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d07d6-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="d07d6-128">Geben Sie nicht beide Attribute an.</span><span class="sxs-lookup"><span data-stu-id="d07d6-128">Do not specify both attributes.</span></span>

<span data-ttu-id="d07d6-129">Wsdcodegen definiert ein Makro mit dem Namen " **donotmodify**".</span><span class="sxs-lookup"><span data-stu-id="d07d6-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="d07d6-130">Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentar Block mit hoher Sichtbarkeit, der Entwicklern anweist, den generierten Code nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d07d6-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="d07d6-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d07d6-131">Examples</span></span>

<span data-ttu-id="d07d6-132">Der folgende XML-Code zeigt, wie das **donotmodify** -Makro eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d07d6-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="d07d6-133">Diese XML-Datei kann einer XML-Konfigurationsdatei für wsdcodegen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d07d6-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="d07d6-134">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d07d6-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d07d6-135">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d07d6-135">Minimum supported system</span></span><br/> | <span data-ttu-id="d07d6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d07d6-136">Windows Vista</span></span> |
| <span data-ttu-id="d07d6-137">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d07d6-137">Can be empty</span></span>                        | <span data-ttu-id="d07d6-138">Ja</span><span class="sxs-lookup"><span data-stu-id="d07d6-138">Yes</span></span>           |



 

 




