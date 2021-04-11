---
description: Generiert C-Konstanten für XML-Schema Tabellen für Nachrichten Typen.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: messagetypedefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215427"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="894ad-103">messagetypedefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="894ad-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="894ad-104">Generiert C-Konstanten für XML-Schema Tabellen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="894ad-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="894ad-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="894ad-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="894ad-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="894ad-106">Attributes</span></span>

<span data-ttu-id="894ad-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="894ad-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="894ad-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="894ad-108">Child elements</span></span>



| <span data-ttu-id="894ad-109">Element</span><span class="sxs-lookup"><span data-stu-id="894ad-109">Element</span></span>                                   | <span data-ttu-id="894ad-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="894ad-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="894ad-111">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="894ad-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="894ad-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="894ad-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="894ad-113">**PortType**</span><span class="sxs-lookup"><span data-stu-id="894ad-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="894ad-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="894ad-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="894ad-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="894ad-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="894ad-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="894ad-116">Parent elements</span></span>



| <span data-ttu-id="894ad-117">Element</span><span class="sxs-lookup"><span data-stu-id="894ad-117">Element</span></span>                         | <span data-ttu-id="894ad-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="894ad-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="894ad-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="894ad-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="894ad-120">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="894ad-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="894ad-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="894ad-121">Remarks</span></span>

<span data-ttu-id="894ad-122">Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die von [**messagetypedeklarationen**](messagetypedeclarations.md)deklarierten Schema Tabellen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="894ad-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="894ad-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="894ad-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="894ad-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="894ad-124">Minimum supported system</span></span><br/> | <span data-ttu-id="894ad-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="894ad-125">Windows Vista</span></span> |
| <span data-ttu-id="894ad-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="894ad-126">Can be empty</span></span>                        | <span data-ttu-id="894ad-127">Ja</span><span class="sxs-lookup"><span data-stu-id="894ad-127">Yes</span></span>           |



 

 




