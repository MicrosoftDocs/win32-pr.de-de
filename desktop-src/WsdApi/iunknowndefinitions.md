---
description: Generiert Implementierungen für die Funktionen QueryInterface, AddRef und Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: IUnknownDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995147"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="07b92-103">IUnknownDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="07b92-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="07b92-104">Generiert Implementierungen für die Funktionen QueryInterface, AddRef und Release.</span><span class="sxs-lookup"><span data-stu-id="07b92-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="07b92-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="07b92-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="07b92-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="07b92-106">Attributes</span></span>



| <span data-ttu-id="07b92-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="07b92-107">Attribute</span></span>                  | <span data-ttu-id="07b92-108">type</span><span class="sxs-lookup"><span data-stu-id="07b92-108">Type</span></span>                         | <span data-ttu-id="07b92-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="07b92-109">Required</span></span>       | <span data-ttu-id="07b92-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07b92-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="07b92-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="07b92-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="07b92-112">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="07b92-112">character\_string</span></span><br/> | <span data-ttu-id="07b92-113">Ja</span><span class="sxs-lookup"><span data-stu-id="07b92-113">Yes</span></span><br/> | <span data-ttu-id="07b92-114">Der Name der implementierenden Klasse.</span><span class="sxs-lookup"><span data-stu-id="07b92-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="07b92-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="07b92-115">**refCountVar**</span></span><br/> | <span data-ttu-id="07b92-116">\_Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="07b92-116">character\_string</span></span><br/> | <span data-ttu-id="07b92-117">Ja</span><span class="sxs-lookup"><span data-stu-id="07b92-117">Yes</span></span><br/> | <span data-ttu-id="07b92-118">Der Name der Verweisanzahlvariablen.</span><span class="sxs-lookup"><span data-stu-id="07b92-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="07b92-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07b92-119">Child elements</span></span>



| <span data-ttu-id="07b92-120">Element</span><span class="sxs-lookup"><span data-stu-id="07b92-120">Element</span></span>                                   | <span data-ttu-id="07b92-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07b92-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b92-122">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="07b92-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="07b92-123">Der Name der Schnittstelle, die von QueryInterface zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="07b92-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="07b92-124">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="07b92-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="07b92-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="07b92-125">Parent elements</span></span>



| <span data-ttu-id="07b92-126">Element</span><span class="sxs-lookup"><span data-stu-id="07b92-126">Element</span></span>                         | <span data-ttu-id="07b92-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07b92-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="07b92-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="07b92-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="07b92-129">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="07b92-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="07b92-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="07b92-130">Element information</span></span>



| <span data-ttu-id="07b92-131">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="07b92-131">Label</span></span> | <span data-ttu-id="07b92-132">Wert</span><span class="sxs-lookup"><span data-stu-id="07b92-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="07b92-133">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="07b92-133">Minimum supported system</span></span><br/> | <span data-ttu-id="07b92-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07b92-134">Windows Vista</span></span> |
| <span data-ttu-id="07b92-135">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="07b92-135">Can be empty</span></span>                        | <span data-ttu-id="07b92-136">Nein</span><span class="sxs-lookup"><span data-stu-id="07b92-136">No</span></span>            |



 

 




