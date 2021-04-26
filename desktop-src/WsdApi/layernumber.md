---
description: Definiert die Anzahl der zu erstellenden Codeebenen.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layerNumber-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995487"
---
# <a name="layernumber-element"></a><span data-ttu-id="58c9b-103">layerNumber-Element</span><span class="sxs-lookup"><span data-stu-id="58c9b-103">layerNumber element</span></span>

<span data-ttu-id="58c9b-104">Definiert die Anzahl der zu erstellenden Codeebenen.</span><span class="sxs-lookup"><span data-stu-id="58c9b-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="58c9b-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="58c9b-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="58c9b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="58c9b-106">Attributes</span></span>

<span data-ttu-id="58c9b-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="58c9b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="58c9b-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58c9b-108">Child elements</span></span>

<span data-ttu-id="58c9b-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="58c9b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="58c9b-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58c9b-110">Parent elements</span></span>



| <span data-ttu-id="58c9b-111">Element</span><span class="sxs-lookup"><span data-stu-id="58c9b-111">Element</span></span>                                     | <span data-ttu-id="58c9b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c9b-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="58c9b-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="58c9b-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="58c9b-114">Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.</span><span class="sxs-lookup"><span data-stu-id="58c9b-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="58c9b-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58c9b-115">Remarks</span></span>

<span data-ttu-id="58c9b-116">Ebenennummern werden in Laufzeittabellen verwendet, um eine Codeebene für eine andere zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="58c9b-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="58c9b-117">WSDAPI selbst verwendet generierten Code mit der Ebenennummer 0.</span><span class="sxs-lookup"><span data-stu-id="58c9b-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="58c9b-118">In der Regel ist dieser Wert 1, was angibt, dass der generierte Code über WSDAPI und keiner anderen Ebene liegt.</span><span class="sxs-lookup"><span data-stu-id="58c9b-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="58c9b-119">In einigen Fällen können höhere Zahlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c9b-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="58c9b-120">Wenn beispielsweise ein Unternehmen Code für eine Geräteklasse (nummerierte Ebene 1) erzeugt, möchte ein bestimmter Hardwareanbieter möglicherweise eine zusätzliche ebene nummerierte Ebene 2 hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58c9b-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="58c9b-121">Rechtliche Werte, mit Ausnahme von WSDAPI selbst, sind größer als 0 und kleiner als 16.</span><span class="sxs-lookup"><span data-stu-id="58c9b-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="58c9b-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="58c9b-122">Element information</span></span>



| <span data-ttu-id="58c9b-123">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="58c9b-123">Label</span></span> | <span data-ttu-id="58c9b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="58c9b-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="58c9b-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="58c9b-125">Minimum supported system</span></span><br/> | <span data-ttu-id="58c9b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58c9b-126">Windows Vista</span></span> |
| <span data-ttu-id="58c9b-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="58c9b-127">Can be empty</span></span>                        | <span data-ttu-id="58c9b-128">Ja</span><span class="sxs-lookup"><span data-stu-id="58c9b-128">Yes</span></span>           |



 

 




