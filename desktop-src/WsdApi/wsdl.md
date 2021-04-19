---
description: Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: wsdl-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcb96e063a289e16d5e459b59cb8808a763618a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380734"
---
# <a name="wsdl-element"></a><span data-ttu-id="df57f-103">wsdl-Element</span><span class="sxs-lookup"><span data-stu-id="df57f-103">wsdl element</span></span>

<span data-ttu-id="df57f-104">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="df57f-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="df57f-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="df57f-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="df57f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="df57f-106">Attributes</span></span>

<span data-ttu-id="df57f-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="df57f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="df57f-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df57f-108">Child elements</span></span>



| <span data-ttu-id="df57f-109">Element</span><span class="sxs-lookup"><span data-stu-id="df57f-109">Element</span></span>                                           | <span data-ttu-id="df57f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df57f-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df57f-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="df57f-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="df57f-112">Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind.</span><span class="sxs-lookup"><span data-stu-id="df57f-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="df57f-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="df57f-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="df57f-114">Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="df57f-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="df57f-115">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="df57f-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="df57f-116">Datei und Pfad der WSDL-Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="df57f-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="df57f-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="df57f-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="df57f-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df57f-118">Parent elements</span></span>



| <span data-ttu-id="df57f-119">Element</span><span class="sxs-lookup"><span data-stu-id="df57f-119">Element</span></span>                                     | <span data-ttu-id="df57f-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df57f-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="df57f-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="df57f-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="df57f-122">Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="df57f-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="df57f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df57f-123">Remarks</span></span>

<span data-ttu-id="df57f-124">Alle [**importHint-**](importhint.md) oder [**excludeImport-Elemente,**](excludeimport.md) die nach dem [**Path-Element**](path.md) in einer XML-Konfigurationsdatei angezeigt werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="df57f-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="df57f-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="df57f-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="df57f-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="df57f-126">Minimum supported system</span></span><br/> | <span data-ttu-id="df57f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df57f-127">Windows Vista</span></span> |
| <span data-ttu-id="df57f-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="df57f-128">Can be empty</span></span>                        | <span data-ttu-id="df57f-129">Nein</span><span class="sxs-lookup"><span data-stu-id="df57f-129">No</span></span>            |



 

 




