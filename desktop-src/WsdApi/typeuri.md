---
description: Gibt einen Typ an, der aus einer XSD-Datei eingeschlossen werden soll.
ms.assetid: dd3894a8-1848-4ae0-ba6c-42ac4fe36ff3
title: typeUri-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9ef0a2482354fcfd962a7e41a7c2b94b54f5cb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998687"
---
# <a name="typeuri-element"></a><span data-ttu-id="36689-103">typeUri-Element</span><span class="sxs-lookup"><span data-stu-id="36689-103">typeUri element</span></span>

<span data-ttu-id="36689-104">Gibt einen Typ an, der aus einer XSD-Datei eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="36689-104">Specifies a type to include from an XSD file.</span></span>

## <a name="usage"></a><span data-ttu-id="36689-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="36689-105">Usage</span></span>

``` syntax
<typeUri
  type = "character_string"
  uri = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="36689-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="36689-106">Attributes</span></span>



| <span data-ttu-id="36689-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="36689-107">Attribute</span></span>           | <span data-ttu-id="36689-108">type</span><span class="sxs-lookup"><span data-stu-id="36689-108">Type</span></span>                         | <span data-ttu-id="36689-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="36689-109">Required</span></span>       | <span data-ttu-id="36689-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36689-110">Description</span></span>                                                            |
|---------------------|------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="36689-111">**type**</span><span class="sxs-lookup"><span data-stu-id="36689-111">**type**</span></span><br/> | <span data-ttu-id="36689-112">Zeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="36689-112">character\_string</span></span><br/> | <span data-ttu-id="36689-113">Ja</span><span class="sxs-lookup"><span data-stu-id="36689-113">Yes</span></span><br/> | <span data-ttu-id="36689-114">Der Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="36689-114">The name of the type.</span></span><br/> <br/>                           |
| <span data-ttu-id="36689-115">**uri**</span><span class="sxs-lookup"><span data-stu-id="36689-115">**uri**</span></span><br/>  | <span data-ttu-id="36689-116">Zeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="36689-116">character\_string</span></span><br/> | <span data-ttu-id="36689-117">Ja</span><span class="sxs-lookup"><span data-stu-id="36689-117">Yes</span></span><br/> | <span data-ttu-id="36689-118">Der Namespace des Typs.</span><span class="sxs-lookup"><span data-stu-id="36689-118">The namespace of the type.</span></span> <span data-ttu-id="36689-119">Muss ein gültiger URI sein.</span><span class="sxs-lookup"><span data-stu-id="36689-119">Must be a valid URI.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="36689-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36689-120">Child elements</span></span>

<span data-ttu-id="36689-121">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="36689-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="36689-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36689-122">Parent elements</span></span>



| <span data-ttu-id="36689-123">Element</span><span class="sxs-lookup"><span data-stu-id="36689-123">Element</span></span>                       | <span data-ttu-id="36689-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36689-124">Description</span></span>                                                                       |
|-------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="36689-125">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="36689-125">**xsd**</span></span>](xsd.md)<br/> | <span data-ttu-id="36689-126">Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="36689-126">Specifies an XSD file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="36689-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="36689-127">Element information</span></span>



| <span data-ttu-id="36689-128">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="36689-128">Label</span></span> | <span data-ttu-id="36689-129">Wert</span><span class="sxs-lookup"><span data-stu-id="36689-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="36689-130">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="36689-130">Minimum supported system</span></span><br/> | <span data-ttu-id="36689-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36689-131">Windows Vista</span></span> |
| <span data-ttu-id="36689-132">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="36689-132">Can be empty</span></span>                        | <span data-ttu-id="36689-133">Ja</span><span class="sxs-lookup"><span data-stu-id="36689-133">Yes</span></span>           |



 

 




