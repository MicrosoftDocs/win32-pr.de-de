---
description: 'Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeimport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863999"
---
# <a name="excludeimport-element"></a><span data-ttu-id="9f9be-103">excludeimport-Element</span><span class="sxs-lookup"><span data-stu-id="9f9be-103">excludeImport element</span></span>

<span data-ttu-id="9f9be-104">Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden.</span><span class="sxs-lookup"><span data-stu-id="9f9be-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="9f9be-105">Dies kann verwendet werden, um zu verhindern, dass wsdcodegen bekannte Ziele importiert, wie z. b. die WS-Addressing-und WS-Eventing Spezifikationen, auch wenn in der WSDL auf diese Ziele verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9f9be-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="9f9be-106">Der Wert dieses Elements muss auf den Namespace festgelegt werden, der im <WSDL: Import>-Elements benannt ist, das ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f9be-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="9f9be-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9f9be-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="9f9be-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9f9be-108">Attributes</span></span>

<span data-ttu-id="9f9be-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="9f9be-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9f9be-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f9be-110">Child elements</span></span>

<span data-ttu-id="9f9be-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="9f9be-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9f9be-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9f9be-112">Parent elements</span></span>



| <span data-ttu-id="9f9be-113">Element</span><span class="sxs-lookup"><span data-stu-id="9f9be-113">Element</span></span>                         | <span data-ttu-id="9f9be-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f9be-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="9f9be-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="9f9be-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="9f9be-116">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f9be-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9f9be-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9f9be-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9f9be-118">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="9f9be-118">Minimum supported system</span></span><br/> | <span data-ttu-id="9f9be-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f9be-119">Windows Vista</span></span> |
| <span data-ttu-id="9f9be-120">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="9f9be-120">Can be empty</span></span>                        | <span data-ttu-id="9f9be-121">Ja</span><span class="sxs-lookup"><span data-stu-id="9f9be-121">Yes</span></span>           |



 

 




