---
description: Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: AUTOSTATIC-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348914"
---
# <a name="autostatic-element"></a><span data-ttu-id="0af73-103">AUTOSTATIC-Element</span><span class="sxs-lookup"><span data-stu-id="0af73-103">autoStatic element</span></span>

<span data-ttu-id="0af73-104">Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0af73-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="0af73-105">Dieses Verhalten ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0af73-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="0af73-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0af73-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="0af73-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="0af73-107">Attributes</span></span>

<span data-ttu-id="0af73-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="0af73-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0af73-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0af73-109">Child elements</span></span>

<span data-ttu-id="0af73-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0af73-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0af73-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0af73-111">Parent elements</span></span>



| <span data-ttu-id="0af73-112">Element</span><span class="sxs-lookup"><span data-stu-id="0af73-112">Element</span></span>                                     | <span data-ttu-id="0af73-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0af73-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0af73-114">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="0af73-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0af73-115">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="0af73-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0af73-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af73-116">Remarks</span></span>

<span data-ttu-id="0af73-117">Das **AUTOSTATIC** -Element ist nicht erforderlich und kann in der XML-Konfigurationsdatei weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0af73-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="0af73-118">Das-Element kann verwendet werden, um die Kennzeichnung generierter Felder als statisch zu deaktivieren oder um explizit das kennzeichnen bestimmter generierter Felder als statisch zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0af73-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="0af73-119">Mögliche Werte sind 1 (aktiviert, Standard) und 0 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="0af73-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="0af73-120">Das Aktivieren von **AUTOSTATIC** kann Kompilierungs Probleme verursachen, abhängig davon, wie der Code Generator an Ausgabedaten weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0af73-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="0af73-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0af73-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0af73-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0af73-122">Minimum supported system</span></span><br/> | <span data-ttu-id="0af73-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0af73-123">Windows Vista</span></span> |
| <span data-ttu-id="0af73-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0af73-124">Can be empty</span></span>                        | <span data-ttu-id="0af73-125">Ja</span><span class="sxs-lookup"><span data-stu-id="0af73-125">Yes</span></span>           |



 

 




