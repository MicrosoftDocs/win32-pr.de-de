---
description: Definiert Text oder CDATA, der vom Include-Element wieder verwendet werden soll.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: Macro-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216310"
---
# <a name="macro-element"></a><span data-ttu-id="0128e-103">Macro-Element</span><span class="sxs-lookup"><span data-stu-id="0128e-103">macro element</span></span>

<span data-ttu-id="0128e-104">Definiert Text oder CDATA, der vom [**include**](include.md) -Element wieder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0128e-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="0128e-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0128e-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="0128e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="0128e-106">Attributes</span></span>



| <span data-ttu-id="0128e-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="0128e-107">Attribute</span></span>           | <span data-ttu-id="0128e-108">type</span><span class="sxs-lookup"><span data-stu-id="0128e-108">Type</span></span>                         | <span data-ttu-id="0128e-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0128e-109">Required</span></span>       | <span data-ttu-id="0128e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0128e-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="0128e-111">**name**</span><span class="sxs-lookup"><span data-stu-id="0128e-111">**name**</span></span><br/> | <span data-ttu-id="0128e-112">Zeichen \_ Folge</span><span class="sxs-lookup"><span data-stu-id="0128e-112">character\_string</span></span><br/> | <span data-ttu-id="0128e-113">Ja</span><span class="sxs-lookup"><span data-stu-id="0128e-113">Yes</span></span><br/> | <span data-ttu-id="0128e-114">Der Name des Makros.</span><span class="sxs-lookup"><span data-stu-id="0128e-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0128e-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0128e-115">Child elements</span></span>

<span data-ttu-id="0128e-116">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0128e-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0128e-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0128e-117">Parent elements</span></span>



| <span data-ttu-id="0128e-118">Element</span><span class="sxs-lookup"><span data-stu-id="0128e-118">Element</span></span>                                     | <span data-ttu-id="0128e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0128e-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="0128e-120">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="0128e-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0128e-121">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="0128e-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0128e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0128e-122">Remarks</span></span>

<span data-ttu-id="0128e-123">Wsdcodegen definiert ein Makro mit dem Namen " **donotmodify**".</span><span class="sxs-lookup"><span data-stu-id="0128e-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="0128e-124">Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentar Block mit hoher Sichtbarkeit, der Entwicklern anweist, den generierten Code nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0128e-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="0128e-125">Der folgende XML-Code zeigt, wie das **donotmodify** -Makro eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0128e-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="0128e-126">Diese XML-Datei kann einer XML-Konfigurationsdatei für wsdcodegen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0128e-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="0128e-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0128e-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0128e-128">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0128e-128">Minimum supported system</span></span><br/> | <span data-ttu-id="0128e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0128e-129">Windows Vista</span></span> |
| <span data-ttu-id="0128e-130">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0128e-130">Can be empty</span></span>                        | <span data-ttu-id="0128e-131">Ja</span><span class="sxs-lookup"><span data-stu-id="0128e-131">Yes</span></span>           |



 

 




