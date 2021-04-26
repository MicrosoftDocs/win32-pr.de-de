---
description: Definiert das Präfix, das im generierten Code für Die Namen von Makros im Namespace verwendet werden soll.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998747"
---
# <a name="macroprefix-element"></a><span data-ttu-id="ecf2a-103">macroPrefix-Element</span><span class="sxs-lookup"><span data-stu-id="ecf2a-103">macroPrefix element</span></span>

<span data-ttu-id="ecf2a-104">Definiert das Präfix, das im generierten Code für Die Namen von Makros im Namespace verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="ecf2a-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ecf2a-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="ecf2a-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="ecf2a-106">Attributes</span></span>

<span data-ttu-id="ecf2a-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ecf2a-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ecf2a-108">Child elements</span></span>

<span data-ttu-id="ecf2a-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ecf2a-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ecf2a-110">Parent elements</span></span>



| <span data-ttu-id="ecf2a-111">Element</span><span class="sxs-lookup"><span data-stu-id="ecf2a-111">Element</span></span>                                   | <span data-ttu-id="ecf2a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecf2a-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ecf2a-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ecf2a-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="ecf2a-114">Ein Namespace, der für die Codegenerierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ecf2a-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecf2a-115">Remarks</span></span>

<span data-ttu-id="ecf2a-116">Dieses Element überschreibt das Standard-URI-Präfix, das für generierte Makros verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="ecf2a-117">Wenn das Makropräfix beispielsweise "AV" und der Name "Tuner" ist, ist das für den qualifizierten Namen generierte Makro \_ "AV \_ Tuner".</span><span class="sxs-lookup"><span data-stu-id="ecf2a-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="ecf2a-118">Standardmäßig erstellt der generierte Code ein bevorzugtes Makropräfix aus dem URI.</span><span class="sxs-lookup"><span data-stu-id="ecf2a-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="ecf2a-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ecf2a-119">Element information</span></span>



| <span data-ttu-id="ecf2a-120">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ecf2a-120">Label</span></span> | <span data-ttu-id="ecf2a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf2a-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ecf2a-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="ecf2a-122">Minimum supported system</span></span><br/> | <span data-ttu-id="ecf2a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecf2a-123">Windows Vista</span></span> |
| <span data-ttu-id="ecf2a-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="ecf2a-124">Can be empty</span></span>                        | <span data-ttu-id="ecf2a-125">Ja</span><span class="sxs-lookup"><span data-stu-id="ecf2a-125">Yes</span></span>           |



 

 




