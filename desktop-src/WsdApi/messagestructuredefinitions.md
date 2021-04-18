---
description: Generiert C-Strukturdefinitionen für Nachrichten Typen.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: messagestructuredefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354627"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="18e74-103">messagestructuredefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="18e74-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="18e74-104">Generiert C-Strukturdefinitionen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="18e74-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="18e74-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="18e74-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="18e74-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="18e74-106">Attributes</span></span>

<span data-ttu-id="18e74-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="18e74-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="18e74-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18e74-108">Child elements</span></span>



| <span data-ttu-id="18e74-109">Element</span><span class="sxs-lookup"><span data-stu-id="18e74-109">Element</span></span>                                   | <span data-ttu-id="18e74-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18e74-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="18e74-111">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="18e74-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="18e74-112">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18e74-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="18e74-113">**PortType**</span><span class="sxs-lookup"><span data-stu-id="18e74-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="18e74-114">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="18e74-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="18e74-115">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="18e74-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="18e74-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18e74-116">Parent elements</span></span>



| <span data-ttu-id="18e74-117">Element</span><span class="sxs-lookup"><span data-stu-id="18e74-117">Element</span></span>                         | <span data-ttu-id="18e74-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18e74-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="18e74-119">**Datei**</span><span class="sxs-lookup"><span data-stu-id="18e74-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="18e74-120">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="18e74-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18e74-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18e74-121">Remarks</span></span>

<span data-ttu-id="18e74-122">Auf Nachrichten Strukturen wird durch generierten Proxy-und Stubcode verwiesen.</span><span class="sxs-lookup"><span data-stu-id="18e74-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="18e74-123">Dieses Element wird zum Generieren von Include-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="18e74-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="18e74-124">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="18e74-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="18e74-125">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="18e74-125">Minimum supported system</span></span><br/> | <span data-ttu-id="18e74-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18e74-126">Windows Vista</span></span> |
| <span data-ttu-id="18e74-127">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="18e74-127">Can be empty</span></span>                        | <span data-ttu-id="18e74-128">Ja</span><span class="sxs-lookup"><span data-stu-id="18e74-128">Yes</span></span>           |



 

 




