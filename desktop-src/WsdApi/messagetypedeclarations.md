---
description: Generiert C-Konstantendeklarationen für XML-Schematabellen für Nachrichtentypen.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: messageTypeDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998727"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="d0503-103">messageTypeDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="d0503-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="d0503-104">Generiert C-Konstantendeklarationen für XML-Schematabellen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="d0503-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="d0503-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d0503-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="d0503-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0503-106">Attributes</span></span>

<span data-ttu-id="d0503-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="d0503-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d0503-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0503-108">Child elements</span></span>



| <span data-ttu-id="d0503-109">Element</span><span class="sxs-lookup"><span data-stu-id="d0503-109">Element</span></span>                                   | <span data-ttu-id="d0503-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0503-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d0503-111">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="d0503-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="d0503-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0503-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="d0503-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="d0503-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="d0503-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0503-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="d0503-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d0503-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="d0503-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0503-116">Parent elements</span></span>



| <span data-ttu-id="d0503-117">Element</span><span class="sxs-lookup"><span data-stu-id="d0503-117">Element</span></span>                         | <span data-ttu-id="d0503-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0503-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d0503-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d0503-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d0503-120">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="d0503-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d0503-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0503-121">Remarks</span></span>

<span data-ttu-id="d0503-122">Auf Schematabellen wird durch Porttypdefinitionen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d0503-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="d0503-123">Dieses Element wird daher in der Regel direkt vor [**portTypeDefinitions-Elementen**](porttypedefinitions.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0503-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="d0503-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d0503-124">Element information</span></span>



| <span data-ttu-id="d0503-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d0503-125">Label</span></span> | <span data-ttu-id="d0503-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d0503-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d0503-127">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d0503-127">Minimum supported system</span></span><br/> | <span data-ttu-id="d0503-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0503-128">Windows Vista</span></span> |
| <span data-ttu-id="d0503-129">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d0503-129">Can be empty</span></span>                        | <span data-ttu-id="d0503-130">Ja</span><span class="sxs-lookup"><span data-stu-id="d0503-130">Yes</span></span>           |



 

 




