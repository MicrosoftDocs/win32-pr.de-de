---
description: Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autoStatic-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994927"
---
# <a name="autostatic-element"></a><span data-ttu-id="0d836-103">autoStatic-Element</span><span class="sxs-lookup"><span data-stu-id="0d836-103">autoStatic element</span></span>

<span data-ttu-id="0d836-104">Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0d836-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="0d836-105">Dieses Verhalten ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0d836-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="0d836-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0d836-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="0d836-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d836-107">Attributes</span></span>

<span data-ttu-id="0d836-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="0d836-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0d836-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d836-109">Child elements</span></span>

<span data-ttu-id="0d836-110">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0d836-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0d836-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d836-111">Parent elements</span></span>



| <span data-ttu-id="0d836-112">Element</span><span class="sxs-lookup"><span data-stu-id="0d836-112">Element</span></span>                                     | <span data-ttu-id="0d836-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d836-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d836-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0d836-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0d836-115">Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.</span><span class="sxs-lookup"><span data-stu-id="0d836-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0d836-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d836-116">Remarks</span></span>

<span data-ttu-id="0d836-117">Das **autoStatic-Element** ist nicht erforderlich und kann in der XML-Konfigurationsdatei ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0d836-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="0d836-118">Das -Element kann verwendet werden, um das Kennzeichnen von generierten Feldern als statisch zu deaktivieren oder das Kennzeichnen bestimmter generierter Felder explizit als statisch zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="0d836-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="0d836-119">Mögliche Werte sind 1 (aktiviert, Standard) und 0 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="0d836-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="0d836-120">Die Aktivierung **von autoStatic** kann zu Kompilierungsproblemen führen, je nachdem, wie der Codegenerator an Ausgabedaten geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0d836-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="0d836-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0d836-121">Element information</span></span>



| <span data-ttu-id="0d836-122">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="0d836-122">Label</span></span> | <span data-ttu-id="0d836-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0d836-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0d836-124">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0d836-124">Minimum supported system</span></span><br/> | <span data-ttu-id="0d836-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d836-125">Windows Vista</span></span> |
| <span data-ttu-id="0d836-126">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0d836-126">Can be empty</span></span>                        | <span data-ttu-id="0d836-127">Ja</span><span class="sxs-lookup"><span data-stu-id="0d836-127">Yes</span></span>           |



 

 




