---
description: Definiert das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroprefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345269"
---
# <a name="macroprefix-element"></a><span data-ttu-id="7503e-103">macroprefix-Element</span><span class="sxs-lookup"><span data-stu-id="7503e-103">macroPrefix element</span></span>

<span data-ttu-id="7503e-104">Definiert das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7503e-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="7503e-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7503e-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="7503e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="7503e-106">Attributes</span></span>

<span data-ttu-id="7503e-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7503e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7503e-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7503e-108">Child elements</span></span>

<span data-ttu-id="7503e-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="7503e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7503e-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7503e-110">Parent elements</span></span>



| <span data-ttu-id="7503e-111">Element</span><span class="sxs-lookup"><span data-stu-id="7503e-111">Element</span></span>                                   | <span data-ttu-id="7503e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7503e-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="7503e-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7503e-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="7503e-114">Ein Namespace, der für die Codegenerierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7503e-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7503e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7503e-115">Remarks</span></span>

<span data-ttu-id="7503e-116">Dieses Element überschreibt das Standard-URI-Präfix, das für generierte Makros verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7503e-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="7503e-117">Wenn das Makro Präfix z. b. "AV \_ " lautet und der Name "Tuner" lautet, ist das für den qualifizierten Namen generierte Makro "AV- \_ Tuner".</span><span class="sxs-lookup"><span data-stu-id="7503e-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="7503e-118">Standardmäßig erstellt der generierte Code ein bevorzugtes Makro Präfix aus dem URI.</span><span class="sxs-lookup"><span data-stu-id="7503e-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="7503e-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7503e-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7503e-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="7503e-120">Minimum supported system</span></span><br/> | <span data-ttu-id="7503e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7503e-121">Windows Vista</span></span> |
| <span data-ttu-id="7503e-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="7503e-122">Can be empty</span></span>                        | <span data-ttu-id="7503e-123">Ja</span><span class="sxs-lookup"><span data-stu-id="7503e-123">Yes</span></span>           |



 

 




