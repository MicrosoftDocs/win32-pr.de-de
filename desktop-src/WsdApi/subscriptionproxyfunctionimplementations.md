---
description: Generiert Implementierungen für Abonnieren/Kündigen von Proxyfunktionen für Benachrichtigungsvorgänge für Porttypen.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995317"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="87e92-103">subscriptionProxyFunctionImplementations-Element</span><span class="sxs-lookup"><span data-stu-id="87e92-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="87e92-104">Generiert Implementierungen für Abonnieren/Kündigen von Proxyfunktionen für Benachrichtigungsvorgänge für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="87e92-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="87e92-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="87e92-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="87e92-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="87e92-106">Attributes</span></span>



| <span data-ttu-id="87e92-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="87e92-107">Attribute</span></span>                 | <span data-ttu-id="87e92-108">type</span><span class="sxs-lookup"><span data-stu-id="87e92-108">Type</span></span>               | <span data-ttu-id="87e92-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87e92-109">Required</span></span>      | <span data-ttu-id="87e92-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87e92-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e92-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="87e92-111">**extensible**</span></span><br/> | <span data-ttu-id="87e92-112">boolean</span><span class="sxs-lookup"><span data-stu-id="87e92-112">boolean</span></span><br/> | <span data-ttu-id="87e92-113">Nein</span><span class="sxs-lookup"><span data-stu-id="87e92-113">No</span></span><br/> | <span data-ttu-id="87e92-114">Die Möglichkeit, Erweiterbarkeitspunkte zu Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="87e92-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="87e92-115">Dieser Wert ist immer auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="87e92-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="87e92-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87e92-116">Child elements</span></span>



| <span data-ttu-id="87e92-117">Element</span><span class="sxs-lookup"><span data-stu-id="87e92-117">Element</span></span>                                                           | <span data-ttu-id="87e92-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87e92-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87e92-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="87e92-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="87e92-120">Gibt den Namen der Benachrichtigungsschnittstelle an, die mit Ereignisabonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87e92-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="87e92-121">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="87e92-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="87e92-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87e92-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="87e92-123">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="87e92-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="87e92-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87e92-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="87e92-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="87e92-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="87e92-126">Gibt den Namen der clientseitigen Proxyklasse an.</span><span class="sxs-lookup"><span data-stu-id="87e92-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="87e92-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="87e92-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="87e92-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87e92-128">Parent elements</span></span>



| <span data-ttu-id="87e92-129">Element</span><span class="sxs-lookup"><span data-stu-id="87e92-129">Element</span></span>                         | <span data-ttu-id="87e92-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87e92-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="87e92-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="87e92-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="87e92-132">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="87e92-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="87e92-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="87e92-133">Element information</span></span>



| <span data-ttu-id="87e92-134">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="87e92-134">Label</span></span> | <span data-ttu-id="87e92-135">Wert</span><span class="sxs-lookup"><span data-stu-id="87e92-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="87e92-136">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="87e92-136">Minimum supported system</span></span><br/> | <span data-ttu-id="87e92-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87e92-137">Windows Vista</span></span> |
| <span data-ttu-id="87e92-138">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="87e92-138">Can be empty</span></span>                        | <span data-ttu-id="87e92-139">Ja</span><span class="sxs-lookup"><span data-stu-id="87e92-139">Yes</span></span>           |



 

 




