---
description: Generiert C-Konstantendeklarationen für Porttypen.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: portTypeDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996557"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="d02aa-103">portTypeDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="d02aa-103">portTypeDeclarations element</span></span>

<span data-ttu-id="d02aa-104">Generiert C-Konstantendeklarationen für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="d02aa-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="d02aa-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d02aa-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="d02aa-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d02aa-106">Attributes</span></span>

<span data-ttu-id="d02aa-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d02aa-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d02aa-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d02aa-108">Child elements</span></span>



| <span data-ttu-id="d02aa-109">Element</span><span class="sxs-lookup"><span data-stu-id="d02aa-109">Element</span></span>                                   | <span data-ttu-id="d02aa-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d02aa-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d02aa-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="d02aa-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="d02aa-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d02aa-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="d02aa-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="d02aa-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="d02aa-114">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="d02aa-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="d02aa-115">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d02aa-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="d02aa-116">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="d02aa-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="d02aa-117">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d02aa-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="d02aa-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d02aa-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="d02aa-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d02aa-119">Parent elements</span></span>



| <span data-ttu-id="d02aa-120">Element</span><span class="sxs-lookup"><span data-stu-id="d02aa-120">Element</span></span>                         | <span data-ttu-id="d02aa-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d02aa-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d02aa-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d02aa-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d02aa-123">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="d02aa-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d02aa-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d02aa-124">Remarks</span></span>

<span data-ttu-id="d02aa-125">Auf Porttypdeklarationen wird von der Anwendung und einem großen Teil des generierten Codes verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d02aa-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="d02aa-126">Dieses Element wird verwendet, um Includedateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d02aa-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="d02aa-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d02aa-127">Element information</span></span>



| <span data-ttu-id="d02aa-128">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d02aa-128">Label</span></span> | <span data-ttu-id="d02aa-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d02aa-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d02aa-130">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d02aa-130">Minimum supported system</span></span><br/> | <span data-ttu-id="d02aa-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d02aa-131">Windows Vista</span></span> |
| <span data-ttu-id="d02aa-132">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d02aa-132">Can be empty</span></span>                        | <span data-ttu-id="d02aa-133">Ja</span><span class="sxs-lookup"><span data-stu-id="d02aa-133">Yes</span></span>           |



 

 




