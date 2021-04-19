---
description: Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem wsdl:import-Element in einer WSDL-Datei benannt sind.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380774"
---
# <a name="excludeimport-element"></a><span data-ttu-id="eca8d-103">excludeImport-Element</span><span class="sxs-lookup"><span data-stu-id="eca8d-103">excludeImport element</span></span>

<span data-ttu-id="eca8d-104">Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind.</span><span class="sxs-lookup"><span data-stu-id="eca8d-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="eca8d-105">Dies kann verwendet werden, um zu halten, dass WsdCodeGen bekannte Ziele wie die WS-Addressing- und WS-Eventing-Spezifikationen importiert, obwohl in der WSDL auf diese Ziele verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eca8d-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="eca8d-106">Der Wert dieses Elements muss auf den Namespace mit dem Namen im \<wsdl:import> auszuschließenden Element festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eca8d-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="eca8d-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="eca8d-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="eca8d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eca8d-108">Attributes</span></span>

<span data-ttu-id="eca8d-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="eca8d-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eca8d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eca8d-110">Child elements</span></span>

<span data-ttu-id="eca8d-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="eca8d-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="eca8d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eca8d-112">Parent elements</span></span>



| <span data-ttu-id="eca8d-113">Element</span><span class="sxs-lookup"><span data-stu-id="eca8d-113">Element</span></span>                         | <span data-ttu-id="eca8d-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eca8d-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="eca8d-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="eca8d-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="eca8d-116">Gibt eine WSDL-Datei an, die für Vertragsinformationen zu verarbeiten ist.</span><span class="sxs-lookup"><span data-stu-id="eca8d-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="eca8d-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="eca8d-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="eca8d-118">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="eca8d-118">Minimum supported system</span></span><br/> | <span data-ttu-id="eca8d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eca8d-119">Windows Vista</span></span> |
| <span data-ttu-id="eca8d-120">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="eca8d-120">Can be empty</span></span>                        | <span data-ttu-id="eca8d-121">Ja</span><span class="sxs-lookup"><span data-stu-id="eca8d-121">Yes</span></span>           |



 

 




