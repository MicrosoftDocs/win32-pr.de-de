---
description: Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: WSDL-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216151"
---
# <a name="wsdl-element"></a><span data-ttu-id="49f57-103">WSDL-Element</span><span class="sxs-lookup"><span data-stu-id="49f57-103">wsdl element</span></span>

<span data-ttu-id="49f57-104">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49f57-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="49f57-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="49f57-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="49f57-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="49f57-106">Attributes</span></span>

<span data-ttu-id="49f57-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="49f57-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="49f57-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49f57-108">Child elements</span></span>



| <span data-ttu-id="49f57-109">Element</span><span class="sxs-lookup"><span data-stu-id="49f57-109">Element</span></span>                                           | <span data-ttu-id="49f57-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49f57-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49f57-111">**excludeimport**</span><span class="sxs-lookup"><span data-stu-id="49f57-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="49f57-112">Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden.</span><span class="sxs-lookup"><span data-stu-id="49f57-112">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="49f57-113">**importhint**</span><span class="sxs-lookup"><span data-stu-id="49f57-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="49f57-114">Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.</span><span class="sxs-lookup"><span data-stu-id="49f57-114">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="49f57-115">**path**</span><span class="sxs-lookup"><span data-stu-id="49f57-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="49f57-116">Die Datei und der Pfad der WSDL-Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="49f57-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="49f57-117">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="49f57-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="49f57-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="49f57-118">Parent elements</span></span>



| <span data-ttu-id="49f57-119">Element</span><span class="sxs-lookup"><span data-stu-id="49f57-119">Element</span></span>                                     | <span data-ttu-id="49f57-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49f57-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="49f57-121">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="49f57-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="49f57-122">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="49f57-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="49f57-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49f57-123">Remarks</span></span>

<span data-ttu-id="49f57-124">Alle [**importhint**](importhint.md) -oder [**excludeimport**](excludeimport.md) -Elemente, die nach dem [**path**](path.md) -Element in einer XML-Konfigurationsdatei angezeigt werden, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="49f57-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="49f57-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="49f57-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="49f57-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="49f57-126">Minimum supported system</span></span><br/> | <span data-ttu-id="49f57-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49f57-127">Windows Vista</span></span> |
| <span data-ttu-id="49f57-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="49f57-128">Can be empty</span></span>                        | <span data-ttu-id="49f57-129">Nein</span><span class="sxs-lookup"><span data-stu-id="49f57-129">No</span></span>            |



 

 




