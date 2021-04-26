---
description: Generiert C-Konstanten für Porttypen.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: portTypeDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff073eb7b0f9cbc4b0b6df87c8f9fc84d4f62882
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996547"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="8c735-103">portTypeDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="8c735-103">portTypeDefinitions element</span></span>

<span data-ttu-id="8c735-104">Generiert C-Konstanten für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="8c735-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="8c735-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8c735-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="8c735-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="8c735-106">Attributes</span></span>

<span data-ttu-id="8c735-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="8c735-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8c735-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c735-108">Child elements</span></span>



| <span data-ttu-id="8c735-109">Element</span><span class="sxs-lookup"><span data-stu-id="8c735-109">Element</span></span>                                                   | <span data-ttu-id="8c735-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c735-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c735-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="8c735-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="8c735-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c735-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="8c735-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="8c735-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="8c735-114">**eventStubFunction**</span><span class="sxs-lookup"><span data-stu-id="8c735-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="8c735-115">Gibt an, ob Stubfunktionsverweise in den Vorgangsstrukturen in den Porttypdefinitionen für Benachrichtigungsvorgänge enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8c735-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="8c735-116">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="8c735-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="8c735-117">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c735-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="8c735-118">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="8c735-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="8c735-119">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c735-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="8c735-120">**stubFunction**</span><span class="sxs-lookup"><span data-stu-id="8c735-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="8c735-121">Gibt an, ob Stubfunktionsverweise in den Vorgangsstrukturen in den Porttypdefinitionen für ein- und zweiseitige Vorgänge enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8c735-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="8c735-122">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="8c735-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="8c735-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c735-123">Parent elements</span></span>



| <span data-ttu-id="8c735-124">Element</span><span class="sxs-lookup"><span data-stu-id="8c735-124">Element</span></span>                         | <span data-ttu-id="8c735-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c735-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8c735-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8c735-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="8c735-127">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="8c735-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8c735-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c735-128">Remarks</span></span>

<span data-ttu-id="8c735-129">Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die von [**portTypeDeclarations deklarierten**](porttypedeclarations.md)Porttypkonstanten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c735-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="8c735-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8c735-130">Element information</span></span>



| <span data-ttu-id="8c735-131">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="8c735-131">Label</span></span> | <span data-ttu-id="8c735-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8c735-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8c735-133">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="8c735-133">Minimum supported system</span></span><br/> | <span data-ttu-id="8c735-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c735-134">Windows Vista</span></span> |
| <span data-ttu-id="8c735-135">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="8c735-135">Can be empty</span></span>                        | <span data-ttu-id="8c735-136">Ja</span><span class="sxs-lookup"><span data-stu-id="8c735-136">Yes</span></span>           |



 

 




