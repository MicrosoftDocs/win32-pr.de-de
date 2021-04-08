---
description: Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: MessageType-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960433"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="7aa1d-103">MessageType-Deklarations Element</span><span class="sxs-lookup"><span data-stu-id="7aa1d-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="7aa1d-104">Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="7aa1d-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7aa1d-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="7aa1d-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="7aa1d-106">Attributes</span></span>

<span data-ttu-id="7aa1d-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7aa1d-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7aa1d-108">Child elements</span></span>



| <span data-ttu-id="7aa1d-109">Element</span><span class="sxs-lookup"><span data-stu-id="7aa1d-109">Element</span></span>                                   | <span data-ttu-id="7aa1d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aa1d-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="7aa1d-111">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="7aa1d-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="7aa1d-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="7aa1d-113">**PortType**</span><span class="sxs-lookup"><span data-stu-id="7aa1d-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="7aa1d-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="7aa1d-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="7aa1d-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="7aa1d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7aa1d-116">Parent elements</span></span>



| <span data-ttu-id="7aa1d-117">Element</span><span class="sxs-lookup"><span data-stu-id="7aa1d-117">Element</span></span>                         | <span data-ttu-id="7aa1d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aa1d-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7aa1d-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7aa1d-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7aa1d-120">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7aa1d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aa1d-121">Remarks</span></span>

<span data-ttu-id="7aa1d-122">Auf Schema Tabellen wird durch Porttyp Definitionen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="7aa1d-123">Dieses Element wird daher in der Regel direkt vor [**porttypeer Definitions**](porttypedefinitions.md) Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aa1d-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="7aa1d-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7aa1d-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7aa1d-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="7aa1d-125">Minimum supported system</span></span><br/> | <span data-ttu-id="7aa1d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7aa1d-126">Windows Vista</span></span> |
| <span data-ttu-id="7aa1d-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="7aa1d-127">Can be empty</span></span>                        | <span data-ttu-id="7aa1d-128">Ja</span><span class="sxs-lookup"><span data-stu-id="7aa1d-128">Yes</span></span>           |



 

 




