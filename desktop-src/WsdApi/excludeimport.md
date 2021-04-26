---
description: Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem wsdl:import-Element in einer WSDL-Datei benannt sind.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995877"
---
# <a name="excludeimport-element"></a><span data-ttu-id="c7245-103">excludeImport-Element</span><span class="sxs-lookup"><span data-stu-id="c7245-103">excludeImport element</span></span>

<span data-ttu-id="c7245-104">Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind.</span><span class="sxs-lookup"><span data-stu-id="c7245-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="c7245-105">Dadurch kann verhindert werden, dass WsdCodeGen bekannte Ziele importiert, z. B. die WS-Addressing und WS-Eventing Spezifikationen, obwohl auf diese Ziele in der WSDL verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c7245-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="c7245-106">Der Wert dieses Elements muss auf den Namespace mit dem Namen im auszuschließenden Element festgelegt \<wsdl:import> werden.</span><span class="sxs-lookup"><span data-stu-id="c7245-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="c7245-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c7245-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="c7245-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c7245-108">Attributes</span></span>

<span data-ttu-id="c7245-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="c7245-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7245-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7245-110">Child elements</span></span>

<span data-ttu-id="c7245-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c7245-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c7245-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7245-112">Parent elements</span></span>



| <span data-ttu-id="c7245-113">Element</span><span class="sxs-lookup"><span data-stu-id="c7245-113">Element</span></span>                         | <span data-ttu-id="c7245-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7245-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c7245-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="c7245-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="c7245-116">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7245-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c7245-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c7245-117">Element information</span></span>



| <span data-ttu-id="c7245-118">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="c7245-118">Label</span></span> | <span data-ttu-id="c7245-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c7245-119">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c7245-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c7245-120">Minimum supported system</span></span><br/> | <span data-ttu-id="c7245-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7245-121">Windows Vista</span></span> |
| <span data-ttu-id="c7245-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c7245-122">Can be empty</span></span>                        | <span data-ttu-id="c7245-123">Ja</span><span class="sxs-lookup"><span data-stu-id="c7245-123">Yes</span></span>           |



 

 




