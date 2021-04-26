---
description: Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: subscriptionIdlFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d738dd06ccbf034702cbb7d6494a28a229d07
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995367"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="47593-103">subscriptionIdlFunctionDeclarations-Element</span><span class="sxs-lookup"><span data-stu-id="47593-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="47593-104">Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="47593-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="47593-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="47593-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="47593-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="47593-106">Attributes</span></span>



| <span data-ttu-id="47593-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="47593-107">Attribute</span></span>                 | <span data-ttu-id="47593-108">type</span><span class="sxs-lookup"><span data-stu-id="47593-108">Type</span></span>               | <span data-ttu-id="47593-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47593-109">Required</span></span>      | <span data-ttu-id="47593-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47593-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47593-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="47593-111">**extensible**</span></span><br/> | <span data-ttu-id="47593-112">boolean</span><span class="sxs-lookup"><span data-stu-id="47593-112">boolean</span></span><br/> | <span data-ttu-id="47593-113">Nein</span><span class="sxs-lookup"><span data-stu-id="47593-113">No</span></span><br/> | <span data-ttu-id="47593-114">Die Möglichkeit, Erweiterungspunkte zu Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="47593-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="47593-115">Dieser Wert ist immer auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47593-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="47593-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47593-116">Child elements</span></span>



| <span data-ttu-id="47593-117">Element</span><span class="sxs-lookup"><span data-stu-id="47593-117">Element</span></span>                                                           | <span data-ttu-id="47593-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47593-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47593-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="47593-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="47593-120">Gibt den Namen der Benachrichtigungsschnittstelle an, die mit Ereignisabonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47593-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="47593-121">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="47593-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="47593-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="47593-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="47593-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="47593-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="47593-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="47593-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="47593-125">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="47593-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="47593-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47593-126">Parent elements</span></span>



| <span data-ttu-id="47593-127">Element</span><span class="sxs-lookup"><span data-stu-id="47593-127">Element</span></span>                         | <span data-ttu-id="47593-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47593-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="47593-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="47593-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="47593-130">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="47593-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="47593-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="47593-131">Element information</span></span>



| <span data-ttu-id="47593-132">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="47593-132">Label</span></span> | <span data-ttu-id="47593-133">Wert</span><span class="sxs-lookup"><span data-stu-id="47593-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="47593-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="47593-134">Minimum supported system</span></span><br/> | <span data-ttu-id="47593-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47593-135">Windows Vista</span></span> |
| <span data-ttu-id="47593-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="47593-136">Can be empty</span></span>                        | <span data-ttu-id="47593-137">Ja</span><span class="sxs-lookup"><span data-stu-id="47593-137">Yes</span></span>           |



 

 




