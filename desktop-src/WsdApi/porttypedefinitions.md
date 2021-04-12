---
description: Generiert C-Konstanten für Porttypen.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: porttypeer Definitions Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216163"
---
# <a name="porttypedefinitions-element"></a><span data-ttu-id="424a5-103">porttypeer Definitions Element</span><span class="sxs-lookup"><span data-stu-id="424a5-103">portTypeDefinitions element</span></span>

<span data-ttu-id="424a5-104">Generiert C-Konstanten für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="424a5-104">Generates C constants for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="424a5-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="424a5-105">Usage</span></span>

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="424a5-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="424a5-106">Attributes</span></span>

<span data-ttu-id="424a5-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="424a5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="424a5-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="424a5-108">Child elements</span></span>



| <span data-ttu-id="424a5-109">Element</span><span class="sxs-lookup"><span data-stu-id="424a5-109">Element</span></span>                                                   | <span data-ttu-id="424a5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="424a5-110">Description</span></span>                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="424a5-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="424a5-111">**codeName**</span></span>](codename.md)<br/>                   | <span data-ttu-id="424a5-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="424a5-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="424a5-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="424a5-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/>         |
| [<span data-ttu-id="424a5-114">**eventstubfunction**</span><span class="sxs-lookup"><span data-stu-id="424a5-114">**eventStubFunction**</span></span>](eventstubfunction.md)<br/> | <span data-ttu-id="424a5-115">Gibt an, ob Stub-Funktions Verweise in den Vorgangs Strukturen in den Porttyp Definitionen für Benachrichtigungs Vorgänge enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="424a5-115">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span><br/> <br/>        |
| [<span data-ttu-id="424a5-116">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="424a5-116">**operation**</span></span>](operation.md)<br/>                 | <span data-ttu-id="424a5-117">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="424a5-117">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                                  |
| [<span data-ttu-id="424a5-118">**PortType**</span><span class="sxs-lookup"><span data-stu-id="424a5-118">**portType**</span></span>](porttype.md)<br/>                   | <span data-ttu-id="424a5-119">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="424a5-119">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                                 |
| [<span data-ttu-id="424a5-120">**stubfunction**</span><span class="sxs-lookup"><span data-stu-id="424a5-120">**stubFunction**</span></span>](stubfunction.md)<br/>           | <span data-ttu-id="424a5-121">Gibt an, ob stubfunktions Verweise in die Vorgangs Strukturen in den Porttyp Definitionen für unidirektionale und bidirektionale Vorgänge eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="424a5-121">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="424a5-122">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="424a5-122">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="424a5-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="424a5-123">Parent elements</span></span>



| <span data-ttu-id="424a5-124">Element</span><span class="sxs-lookup"><span data-stu-id="424a5-124">Element</span></span>                         | <span data-ttu-id="424a5-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="424a5-125">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="424a5-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="424a5-126">**file**</span></span>](file.md)<br/> | <span data-ttu-id="424a5-127">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="424a5-127">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="424a5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="424a5-128">Remarks</span></span>

<span data-ttu-id="424a5-129">Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die von [**porttypeer Deklarationen deklarierten Porttyp**](porttypedeclarations.md)Konstanten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="424a5-129">This element is generally used in C source files to provide the port type constants declared by [**portTypeDeclarations**](porttypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="424a5-130">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="424a5-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="424a5-131">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="424a5-131">Minimum supported system</span></span><br/> | <span data-ttu-id="424a5-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="424a5-132">Windows Vista</span></span> |
| <span data-ttu-id="424a5-133">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="424a5-133">Can be empty</span></span>                        | <span data-ttu-id="424a5-134">Ja</span><span class="sxs-lookup"><span data-stu-id="424a5-134">Yes</span></span>           |



 

 




