---
description: Generiert C-Konstante Deklarationen für Porttypen.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: porttypeer-Deklarations Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345865"
---
# <a name="porttypedeclarations-element"></a><span data-ttu-id="62b00-103">porttypeer-Deklarations Element</span><span class="sxs-lookup"><span data-stu-id="62b00-103">portTypeDeclarations element</span></span>

<span data-ttu-id="62b00-104">Generiert C-Konstante Deklarationen für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="62b00-104">Generates C constant declarations for port types.</span></span>

## <a name="usage"></a><span data-ttu-id="62b00-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="62b00-105">Usage</span></span>

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="62b00-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="62b00-106">Attributes</span></span>

<span data-ttu-id="62b00-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="62b00-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="62b00-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62b00-108">Child elements</span></span>



| <span data-ttu-id="62b00-109">Element</span><span class="sxs-lookup"><span data-stu-id="62b00-109">Element</span></span>                                   | <span data-ttu-id="62b00-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62b00-110">Description</span></span>                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62b00-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="62b00-111">**codeName**</span></span>](codename.md)<br/>   | <span data-ttu-id="62b00-112">Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62b00-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="62b00-113">Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.</span><span class="sxs-lookup"><span data-stu-id="62b00-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="62b00-114">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="62b00-114">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="62b00-115">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="62b00-115">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                                                                          |
| [<span data-ttu-id="62b00-116">**PortType**</span><span class="sxs-lookup"><span data-stu-id="62b00-116">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="62b00-117">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="62b00-117">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a><span data-ttu-id="62b00-118">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="62b00-118">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a><span data-ttu-id="62b00-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="62b00-119">Parent elements</span></span>



| <span data-ttu-id="62b00-120">Element</span><span class="sxs-lookup"><span data-stu-id="62b00-120">Element</span></span>                         | <span data-ttu-id="62b00-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62b00-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="62b00-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="62b00-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="62b00-123">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="62b00-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="62b00-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62b00-124">Remarks</span></span>

<span data-ttu-id="62b00-125">Auf Porttyp Deklarationen wird von der Anwendung und einem Großteil des generierten Codes verwiesen.</span><span class="sxs-lookup"><span data-stu-id="62b00-125">Port type declarations are referenced by the application and much of the generated code.</span></span> <span data-ttu-id="62b00-126">Dieses Element wird zum Generieren von Include-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="62b00-126">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="62b00-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="62b00-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="62b00-128">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="62b00-128">Minimum supported system</span></span><br/> | <span data-ttu-id="62b00-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62b00-129">Windows Vista</span></span> |
| <span data-ttu-id="62b00-130">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="62b00-130">Can be empty</span></span>                        | <span data-ttu-id="62b00-131">Ja</span><span class="sxs-lookup"><span data-stu-id="62b00-131">Yes</span></span>           |



 

 




