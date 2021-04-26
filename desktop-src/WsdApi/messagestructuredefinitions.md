---
description: Generiert C-Strukturdefinitionen für Nachrichtentypen.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: messageStructureDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993667"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="77ce5-103">messageStructureDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="77ce5-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="77ce5-104">Generiert C-Strukturdefinitionen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="77ce5-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="77ce5-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="77ce5-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="77ce5-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="77ce5-106">Attributes</span></span>

<span data-ttu-id="77ce5-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="77ce5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="77ce5-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77ce5-108">Child elements</span></span>



| <span data-ttu-id="77ce5-109">Element</span><span class="sxs-lookup"><span data-stu-id="77ce5-109">Element</span></span>                                   | <span data-ttu-id="77ce5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77ce5-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="77ce5-111">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="77ce5-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="77ce5-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77ce5-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="77ce5-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="77ce5-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="77ce5-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77ce5-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="77ce5-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="77ce5-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="77ce5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77ce5-116">Parent elements</span></span>



| <span data-ttu-id="77ce5-117">Element</span><span class="sxs-lookup"><span data-stu-id="77ce5-117">Element</span></span>                         | <span data-ttu-id="77ce5-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77ce5-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="77ce5-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="77ce5-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="77ce5-120">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="77ce5-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="77ce5-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77ce5-121">Remarks</span></span>

<span data-ttu-id="77ce5-122">Auf Nachrichtenstrukturen wird durch generierten Proxy- und Stubcode verwiesen.</span><span class="sxs-lookup"><span data-stu-id="77ce5-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="77ce5-123">Dieses Element wird verwendet, um Includedateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="77ce5-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="77ce5-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="77ce5-124">Element information</span></span>



| <span data-ttu-id="77ce5-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="77ce5-125">Label</span></span> | <span data-ttu-id="77ce5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="77ce5-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="77ce5-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="77ce5-127">Minimum supported system</span></span><br/> | <span data-ttu-id="77ce5-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77ce5-128">Windows Vista</span></span> |
| <span data-ttu-id="77ce5-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="77ce5-129">Can be empty</span></span>                        | <span data-ttu-id="77ce5-130">Ja</span><span class="sxs-lookup"><span data-stu-id="77ce5-130">Yes</span></span>           |



 

 




