---
description: Definiert die Anzahl der zu generierenden Code Schicht.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layernumber-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216311"
---
# <a name="layernumber-element"></a><span data-ttu-id="7db9c-103">layernumber-Element</span><span class="sxs-lookup"><span data-stu-id="7db9c-103">layerNumber element</span></span>

<span data-ttu-id="7db9c-104">Definiert die Anzahl der zu generierenden Code Schicht.</span><span class="sxs-lookup"><span data-stu-id="7db9c-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="7db9c-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7db9c-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="7db9c-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="7db9c-106">Attributes</span></span>

<span data-ttu-id="7db9c-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7db9c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7db9c-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7db9c-108">Child elements</span></span>

<span data-ttu-id="7db9c-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="7db9c-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7db9c-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7db9c-110">Parent elements</span></span>



| <span data-ttu-id="7db9c-111">Element</span><span class="sxs-lookup"><span data-stu-id="7db9c-111">Element</span></span>                                     | <span data-ttu-id="7db9c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7db9c-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7db9c-113">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="7db9c-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="7db9c-114">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="7db9c-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7db9c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7db9c-115">Remarks</span></span>

<span data-ttu-id="7db9c-116">Ebenennummern werden in Lauf Zeit Tabellen verwendet, um eine Codeebene für eine andere zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7db9c-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="7db9c-117">WSDAPI selbst verwendet generierten Code mit einer Ebenennummer von 0.</span><span class="sxs-lookup"><span data-stu-id="7db9c-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="7db9c-118">Normalerweise ist dieser Wert 1, was darauf hinweist, dass der generierte Code über WSDAPI und keine andere Ebene geschichtet ist.</span><span class="sxs-lookup"><span data-stu-id="7db9c-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="7db9c-119">In einigen Fällen können höhere Zahlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7db9c-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="7db9c-120">Wenn ein Unternehmen z. b. Code für eine Geräteklasse (nummerierte Schicht 1) erstellt, möchte ein bestimmter Hardwarehersteller möglicherweise eine weitere Ebene mit der nummerierten Ebene 2 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7db9c-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="7db9c-121">Zulässige Werte, außer im Fall von WSDAPI, sind größer als 0 und kleiner als 16.</span><span class="sxs-lookup"><span data-stu-id="7db9c-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="7db9c-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7db9c-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7db9c-123">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="7db9c-123">Minimum supported system</span></span><br/> | <span data-ttu-id="7db9c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7db9c-124">Windows Vista</span></span> |
| <span data-ttu-id="7db9c-125">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="7db9c-125">Can be empty</span></span>                        | <span data-ttu-id="7db9c-126">Ja</span><span class="sxs-lookup"><span data-stu-id="7db9c-126">Yes</span></span>           |



 

 




