---
description: Generiert Implementierungen für die Funktionen QueryInterface, adressf und Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Iunknowndefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348912"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="2c10d-103">Iunknowndefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="2c10d-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="2c10d-104">Generiert Implementierungen für die Funktionen QueryInterface, adressf und Release.</span><span class="sxs-lookup"><span data-stu-id="2c10d-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="2c10d-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="2c10d-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="2c10d-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c10d-106">Attributes</span></span>



| <span data-ttu-id="2c10d-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="2c10d-107">Attribute</span></span>                  | <span data-ttu-id="2c10d-108">type</span><span class="sxs-lookup"><span data-stu-id="2c10d-108">Type</span></span>                         | <span data-ttu-id="2c10d-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2c10d-109">Required</span></span>       | <span data-ttu-id="2c10d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c10d-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="2c10d-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="2c10d-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="2c10d-112">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="2c10d-112">character\_string</span></span><br/> | <span data-ttu-id="2c10d-113">Ja</span><span class="sxs-lookup"><span data-stu-id="2c10d-113">Yes</span></span><br/> | <span data-ttu-id="2c10d-114">Der Name der implementierenden Klasse.</span><span class="sxs-lookup"><span data-stu-id="2c10d-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="2c10d-115">**Ref-Datei**</span><span class="sxs-lookup"><span data-stu-id="2c10d-115">**refCountVar**</span></span><br/> | <span data-ttu-id="2c10d-116">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="2c10d-116">character\_string</span></span><br/> | <span data-ttu-id="2c10d-117">Ja</span><span class="sxs-lookup"><span data-stu-id="2c10d-117">Yes</span></span><br/> | <span data-ttu-id="2c10d-118">Der Verweis Zähler-Variablenname.</span><span class="sxs-lookup"><span data-stu-id="2c10d-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="2c10d-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c10d-119">Child elements</span></span>



| <span data-ttu-id="2c10d-120">Element</span><span class="sxs-lookup"><span data-stu-id="2c10d-120">Element</span></span>                                   | <span data-ttu-id="2c10d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c10d-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c10d-122">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2c10d-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="2c10d-123">Der Name der Schnittstelle, die von QueryInterface zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c10d-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="2c10d-124">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="2c10d-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="2c10d-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c10d-125">Parent elements</span></span>



| <span data-ttu-id="2c10d-126">Element</span><span class="sxs-lookup"><span data-stu-id="2c10d-126">Element</span></span>                         | <span data-ttu-id="2c10d-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c10d-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2c10d-128">**Datei**</span><span class="sxs-lookup"><span data-stu-id="2c10d-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="2c10d-129">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="2c10d-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="2c10d-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2c10d-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2c10d-131">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="2c10d-131">Minimum supported system</span></span><br/> | <span data-ttu-id="2c10d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c10d-132">Windows Vista</span></span> |
| <span data-ttu-id="2c10d-133">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="2c10d-133">Can be empty</span></span>                        | <span data-ttu-id="2c10d-134">Nein</span><span class="sxs-lookup"><span data-stu-id="2c10d-134">No</span></span>            |



 

 




