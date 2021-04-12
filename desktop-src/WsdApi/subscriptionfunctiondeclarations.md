---
description: Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: abonnemenfunctiondeklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218811"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="e97a6-103">abonnemenfunctiondeklarationen-Element</span><span class="sxs-lookup"><span data-stu-id="e97a6-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="e97a6-104">Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e97a6-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="e97a6-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e97a6-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="e97a6-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="e97a6-106">Attributes</span></span>



| <span data-ttu-id="e97a6-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="e97a6-107">Attribute</span></span>                 | <span data-ttu-id="e97a6-108">type</span><span class="sxs-lookup"><span data-stu-id="e97a6-108">Type</span></span>               | <span data-ttu-id="e97a6-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e97a6-109">Required</span></span>      | <span data-ttu-id="e97a6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e97a6-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e97a6-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="e97a6-111">**extensible**</span></span><br/> | <span data-ttu-id="e97a6-112">boolean</span><span class="sxs-lookup"><span data-stu-id="e97a6-112">boolean</span></span><br/> | <span data-ttu-id="e97a6-113">Nein</span><span class="sxs-lookup"><span data-stu-id="e97a6-113">No</span></span><br/> | <span data-ttu-id="e97a6-114">Die Möglichkeit, Erweiterbarkeits Punkte Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e97a6-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="e97a6-115">Dieser Wert ist immer auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e97a6-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="e97a6-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e97a6-116">Child elements</span></span>



| <span data-ttu-id="e97a6-117">Element</span><span class="sxs-lookup"><span data-stu-id="e97a6-117">Element</span></span>                                                           | <span data-ttu-id="e97a6-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e97a6-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e97a6-119">**notificationinterface**</span><span class="sxs-lookup"><span data-stu-id="e97a6-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="e97a6-120">Gibt den Namen der Benachrichtigungs Schnittstelle an, die mit Ereignis Abonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e97a6-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="e97a6-121">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="e97a6-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="e97a6-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e97a6-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="e97a6-123">**PortType**</span><span class="sxs-lookup"><span data-stu-id="e97a6-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="e97a6-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e97a6-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="e97a6-125">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="e97a6-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e97a6-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e97a6-126">Parent elements</span></span>



| <span data-ttu-id="e97a6-127">Element</span><span class="sxs-lookup"><span data-stu-id="e97a6-127">Element</span></span>                         | <span data-ttu-id="e97a6-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e97a6-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e97a6-129">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e97a6-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e97a6-130">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="e97a6-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e97a6-131">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e97a6-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e97a6-132">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="e97a6-132">Minimum supported system</span></span><br/> | <span data-ttu-id="e97a6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e97a6-133">Windows Vista</span></span> |
| <span data-ttu-id="e97a6-134">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="e97a6-134">Can be empty</span></span>                        | <span data-ttu-id="e97a6-135">Ja</span><span class="sxs-lookup"><span data-stu-id="e97a6-135">Yes</span></span>           |



 

 




