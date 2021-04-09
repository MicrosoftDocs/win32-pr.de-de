---
description: Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: abonnemenproxyfunctionimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129100"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="1e514-103">abonnemenproxyfunctionimplementierungen-Element</span><span class="sxs-lookup"><span data-stu-id="1e514-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="1e514-104">Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1e514-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="1e514-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="1e514-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="1e514-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e514-106">Attributes</span></span>



| <span data-ttu-id="1e514-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="1e514-107">Attribute</span></span>                 | <span data-ttu-id="1e514-108">type</span><span class="sxs-lookup"><span data-stu-id="1e514-108">Type</span></span>               | <span data-ttu-id="1e514-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1e514-109">Required</span></span>      | <span data-ttu-id="1e514-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e514-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e514-111">**Extensible**</span><span class="sxs-lookup"><span data-stu-id="1e514-111">**extensible**</span></span><br/> | <span data-ttu-id="1e514-112">boolean</span><span class="sxs-lookup"><span data-stu-id="1e514-112">boolean</span></span><br/> | <span data-ttu-id="1e514-113">Nein</span><span class="sxs-lookup"><span data-stu-id="1e514-113">No</span></span><br/> | <span data-ttu-id="1e514-114">Die Möglichkeit, Erweiterbarkeits Punkte Funktionen und Schnittstellen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1e514-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="1e514-115">Dieser Wert ist immer auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1e514-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="1e514-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e514-116">Child elements</span></span>



| <span data-ttu-id="1e514-117">Element</span><span class="sxs-lookup"><span data-stu-id="1e514-117">Element</span></span>                                                           | <span data-ttu-id="1e514-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e514-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e514-119">**notificationinterface**</span><span class="sxs-lookup"><span data-stu-id="1e514-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="1e514-120">Gibt den Namen der Benachrichtigungs Schnittstelle an, die mit Ereignis Abonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e514-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="1e514-121">**Betriebs**</span><span class="sxs-lookup"><span data-stu-id="1e514-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="1e514-122">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e514-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="1e514-123">**PortType**</span><span class="sxs-lookup"><span data-stu-id="1e514-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="1e514-124">Gibt den Porttyp an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e514-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="1e514-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="1e514-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="1e514-126">Gibt den Namen der Client seitigen Proxy Klasse an.</span><span class="sxs-lookup"><span data-stu-id="1e514-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="1e514-127">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="1e514-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="1e514-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e514-128">Parent elements</span></span>



| <span data-ttu-id="1e514-129">Element</span><span class="sxs-lookup"><span data-stu-id="1e514-129">Element</span></span>                         | <span data-ttu-id="1e514-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e514-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1e514-131">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1e514-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="1e514-132">Gibt eine Datei aus dem Code-Generator aus.</span><span class="sxs-lookup"><span data-stu-id="1e514-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1e514-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1e514-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1e514-134">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="1e514-134">Minimum supported system</span></span><br/> | <span data-ttu-id="1e514-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e514-135">Windows Vista</span></span> |
| <span data-ttu-id="1e514-136">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="1e514-136">Can be empty</span></span>                        | <span data-ttu-id="1e514-137">Ja</span><span class="sxs-lookup"><span data-stu-id="1e514-137">Yes</span></span>           |



 

 




