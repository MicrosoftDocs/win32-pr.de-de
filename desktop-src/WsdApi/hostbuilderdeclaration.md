---
description: Generiert eine Deklaration für eine Funktion, die einen typisierten Host erstellt.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostBuilderDeclaration-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994907"
---
# <a name="hostbuilderdeclaration-element"></a><span data-ttu-id="34a91-103">hostBuilderDeclaration-Element</span><span class="sxs-lookup"><span data-stu-id="34a91-103">hostBuilderDeclaration element</span></span>

<span data-ttu-id="34a91-104">Generiert eine Deklaration für eine Funktion, die einen typisierten Host erstellt.</span><span class="sxs-lookup"><span data-stu-id="34a91-104">Generates a declaration for a function that creates a typed host.</span></span>

## <a name="usage"></a><span data-ttu-id="34a91-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="34a91-105">Usage</span></span>

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a><span data-ttu-id="34a91-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="34a91-106">Attributes</span></span>

<span data-ttu-id="34a91-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="34a91-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="34a91-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34a91-108">Child elements</span></span>



| <span data-ttu-id="34a91-109">Element</span><span class="sxs-lookup"><span data-stu-id="34a91-109">Element</span></span>                                   | <span data-ttu-id="34a91-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34a91-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34a91-111">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="34a91-111">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="34a91-112">Der Name der Dienstschnittstelle, die für den Host eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a91-112">The name of service interface to be included for host.</span></span> <span data-ttu-id="34a91-113">Der Wert dieses Elements muss mit dem Wert des [**untergeordneten Schnittstellenelements**](interface.md) von [**hostedService**](hostedservice.md)übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="34a91-113">The value of this element must match the value of the [**interface**](interface.md) child element of [**hostedService**](hostedservice.md).</span></span> <br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="34a91-114">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="34a91-114">Child element sequence</span></span>

``` syntax
interface+
```

## <a name="parent-elements"></a><span data-ttu-id="34a91-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34a91-115">Parent elements</span></span>



| <span data-ttu-id="34a91-116">Element</span><span class="sxs-lookup"><span data-stu-id="34a91-116">Element</span></span>                         | <span data-ttu-id="34a91-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34a91-117">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="34a91-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="34a91-118">**file**</span></span>](file.md)<br/> | <span data-ttu-id="34a91-119">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="34a91-119">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="34a91-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="34a91-120">Element information</span></span>



| <span data-ttu-id="34a91-121">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="34a91-121">Label</span></span> | <span data-ttu-id="34a91-122">Wert</span><span class="sxs-lookup"><span data-stu-id="34a91-122">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="34a91-123">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="34a91-123">Minimum supported system</span></span><br/> | <span data-ttu-id="34a91-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34a91-124">Windows Vista</span></span> |
| <span data-ttu-id="34a91-125">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="34a91-125">Can be empty</span></span>                        | <span data-ttu-id="34a91-126">Nein</span><span class="sxs-lookup"><span data-stu-id="34a91-126">No</span></span>            |



 

 




