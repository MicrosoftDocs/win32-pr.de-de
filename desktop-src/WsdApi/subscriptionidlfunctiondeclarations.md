---
description: Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: abonnemenidlfunctiondeklarationselement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867603"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="9cbed-103">abonnemenidlfunctiondeklarationselement</span><span class="sxs-lookup"><span data-stu-id="9cbed-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="9cbed-104">Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9cbed-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="9cbed-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9cbed-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="9cbed-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="9cbed-106">Attributes</span></span>



| <span data-ttu-id="9cbed-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="9cbed-107">Attribute</span></span>                 | <span data-ttu-id="9cbed-108">type</span><span class="sxs-lookup"><span data-stu-id="9cbed-108">Type</span></span>               | <span data-ttu-id="9cbed-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9cbed-109">Required</span></span>      | <span data-ttu-id="9cbed-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cbed-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbed-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="9cbed-111">**extensible**</span></span><br/> | <span data-ttu-id="9cbed-112">boolean</span><span class="sxs-lookup"><span data-stu-id="9cbed-112">boolean</span></span><br/> | <span data-ttu-id="9cbed-113">Nein</span><span class="sxs-lookup"><span data-stu-id="9cbed-113">No</span></span><br/> | <span data-ttu-id="9cbed-114">Die Möglichkeit, Erweiterbarkeits Punkte Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9cbed-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="9cbed-115">Dieser Wert ist immer auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9cbed-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="9cbed-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cbed-116">Child elements</span></span>



| <span data-ttu-id="9cbed-117">Element</span><span class="sxs-lookup"><span data-stu-id="9cbed-117">Element</span></span>                                                           | <span data-ttu-id="9cbed-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cbed-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cbed-119">**notificationinterface**</span><span class="sxs-lookup"><span data-stu-id="9cbed-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="9cbed-120">Gibt den Namen der Benachrichtigungs Schnittstelle an, die mit Ereignis Abonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cbed-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="9cbed-121">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="9cbed-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="9cbed-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cbed-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="9cbed-123">**PortType**</span><span class="sxs-lookup"><span data-stu-id="9cbed-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="9cbed-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cbed-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="9cbed-125">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="9cbed-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="9cbed-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cbed-126">Parent elements</span></span>



| <span data-ttu-id="9cbed-127">Element</span><span class="sxs-lookup"><span data-stu-id="9cbed-127">Element</span></span>                         | <span data-ttu-id="9cbed-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cbed-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9cbed-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="9cbed-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9cbed-130">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="9cbed-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9cbed-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9cbed-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9cbed-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="9cbed-132">Minimum supported system</span></span><br/> | <span data-ttu-id="9cbed-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cbed-133">Windows Vista</span></span> |
| <span data-ttu-id="9cbed-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="9cbed-134">Can be empty</span></span>                        | <span data-ttu-id="9cbed-135">Ja</span><span class="sxs-lookup"><span data-stu-id="9cbed-135">Yes</span></span>           |



 

 




