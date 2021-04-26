---
description: Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: messageTypeDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998707"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="57ed9-103">messageTypeDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="57ed9-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="57ed9-104">Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="57ed9-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="57ed9-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="57ed9-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="57ed9-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="57ed9-106">Attributes</span></span>

<span data-ttu-id="57ed9-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="57ed9-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="57ed9-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57ed9-108">Child elements</span></span>



| <span data-ttu-id="57ed9-109">Element</span><span class="sxs-lookup"><span data-stu-id="57ed9-109">Element</span></span>                                   | <span data-ttu-id="57ed9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57ed9-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="57ed9-111">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="57ed9-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="57ed9-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="57ed9-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="57ed9-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="57ed9-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="57ed9-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="57ed9-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="57ed9-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="57ed9-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="57ed9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="57ed9-116">Parent elements</span></span>



| <span data-ttu-id="57ed9-117">Element</span><span class="sxs-lookup"><span data-stu-id="57ed9-117">Element</span></span>                         | <span data-ttu-id="57ed9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57ed9-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="57ed9-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="57ed9-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="57ed9-120">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="57ed9-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="57ed9-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57ed9-121">Remarks</span></span>

<span data-ttu-id="57ed9-122">Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die Schematabellen zur Verfügung zu stellen, die von [**messageTypeDeclarations deklariert werden.**](messagetypedeclarations.md)</span><span class="sxs-lookup"><span data-stu-id="57ed9-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="57ed9-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="57ed9-123">Element information</span></span>



| <span data-ttu-id="57ed9-124">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="57ed9-124">Label</span></span> | <span data-ttu-id="57ed9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="57ed9-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="57ed9-126">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="57ed9-126">Minimum supported system</span></span><br/> | <span data-ttu-id="57ed9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ed9-127">Windows Vista</span></span> |
| <span data-ttu-id="57ed9-128">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="57ed9-128">Can be empty</span></span>                        | <span data-ttu-id="57ed9-129">Ja</span><span class="sxs-lookup"><span data-stu-id="57ed9-129">Yes</span></span>           |



 

 




