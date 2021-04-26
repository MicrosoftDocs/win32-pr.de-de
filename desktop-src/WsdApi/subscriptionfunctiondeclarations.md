---
description: Generiert Implementierungsdeklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: subscriptionFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995457"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="44c79-103">subscriptionFunctionDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="44c79-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="44c79-104">Generiert Implementierungsdeklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="44c79-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="44c79-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="44c79-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="44c79-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="44c79-106">Attributes</span></span>



| <span data-ttu-id="44c79-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="44c79-107">Attribute</span></span>                 | <span data-ttu-id="44c79-108">type</span><span class="sxs-lookup"><span data-stu-id="44c79-108">Type</span></span>               | <span data-ttu-id="44c79-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="44c79-109">Required</span></span>      | <span data-ttu-id="44c79-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44c79-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c79-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="44c79-111">**extensible**</span></span><br/> | <span data-ttu-id="44c79-112">boolean</span><span class="sxs-lookup"><span data-stu-id="44c79-112">boolean</span></span><br/> | <span data-ttu-id="44c79-113">Nein</span><span class="sxs-lookup"><span data-stu-id="44c79-113">No</span></span><br/> | <span data-ttu-id="44c79-114">Die Möglichkeit, Erweiterungspunkte zu Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="44c79-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="44c79-115">Dieser Wert ist immer auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44c79-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="44c79-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44c79-116">Child elements</span></span>



| <span data-ttu-id="44c79-117">Element</span><span class="sxs-lookup"><span data-stu-id="44c79-117">Element</span></span>                                                           | <span data-ttu-id="44c79-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44c79-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44c79-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="44c79-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="44c79-120">Gibt den Namen der Benachrichtigungsschnittstelle an, die mit Ereignisabonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44c79-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="44c79-121">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="44c79-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="44c79-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44c79-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="44c79-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="44c79-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="44c79-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44c79-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="44c79-125">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="44c79-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="44c79-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44c79-126">Parent elements</span></span>



| <span data-ttu-id="44c79-127">Element</span><span class="sxs-lookup"><span data-stu-id="44c79-127">Element</span></span>                         | <span data-ttu-id="44c79-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44c79-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="44c79-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="44c79-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="44c79-130">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="44c79-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="44c79-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="44c79-131">Element information</span></span>



| <span data-ttu-id="44c79-132">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="44c79-132">Label</span></span> | <span data-ttu-id="44c79-133">Wert</span><span class="sxs-lookup"><span data-stu-id="44c79-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="44c79-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="44c79-134">Minimum supported system</span></span><br/> | <span data-ttu-id="44c79-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44c79-135">Windows Vista</span></span> |
| <span data-ttu-id="44c79-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="44c79-136">Can be empty</span></span>                        | <span data-ttu-id="44c79-137">Ja</span><span class="sxs-lookup"><span data-stu-id="44c79-137">Yes</span></span>           |



 

 




