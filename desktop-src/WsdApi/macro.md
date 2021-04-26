---
description: Definiert Text oder CDATA, der vom include-Element wiederverwendet werden soll.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994327"
---
# <a name="macro-element"></a><span data-ttu-id="9a4f7-103">macro-Element</span><span class="sxs-lookup"><span data-stu-id="9a4f7-103">macro element</span></span>

<span data-ttu-id="9a4f7-104">Definiert Text oder CDATA, der vom [**include-Element**](include.md) wiederverwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="9a4f7-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9a4f7-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="9a4f7-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a4f7-106">Attributes</span></span>



| <span data-ttu-id="9a4f7-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="9a4f7-107">Attribute</span></span>           | <span data-ttu-id="9a4f7-108">type</span><span class="sxs-lookup"><span data-stu-id="9a4f7-108">Type</span></span>                         | <span data-ttu-id="9a4f7-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9a4f7-109">Required</span></span>       | <span data-ttu-id="9a4f7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a4f7-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="9a4f7-111">**name**</span><span class="sxs-lookup"><span data-stu-id="9a4f7-111">**name**</span></span><br/> | <span data-ttu-id="9a4f7-112">Zeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="9a4f7-112">character\_string</span></span><br/> | <span data-ttu-id="9a4f7-113">Ja</span><span class="sxs-lookup"><span data-stu-id="9a4f7-113">Yes</span></span><br/> | <span data-ttu-id="9a4f7-114">Der Name des Makros.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="9a4f7-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a4f7-115">Child elements</span></span>

<span data-ttu-id="9a4f7-116">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9a4f7-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a4f7-117">Parent elements</span></span>



| <span data-ttu-id="9a4f7-118">Element</span><span class="sxs-lookup"><span data-stu-id="9a4f7-118">Element</span></span>                                     | <span data-ttu-id="9a4f7-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a4f7-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a4f7-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="9a4f7-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="9a4f7-121">Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9a4f7-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a4f7-122">Remarks</span></span>

<span data-ttu-id="9a4f7-123">WsdCodeGen definiert ein Makro namens **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="9a4f7-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="9a4f7-124">Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweist, den generierten Code nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="9a4f7-125">Der folgende XML-Code zeigt, wie das **DoNotModify-Makro** eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="9a4f7-126">Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9a4f7-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="9a4f7-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9a4f7-127">Element information</span></span>



| <span data-ttu-id="9a4f7-128">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="9a4f7-128">Label</span></span> | <span data-ttu-id="9a4f7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9a4f7-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9a4f7-130">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="9a4f7-130">Minimum supported system</span></span><br/> | <span data-ttu-id="9a4f7-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a4f7-131">Windows Vista</span></span> |
| <span data-ttu-id="9a4f7-132">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="9a4f7-132">Can be empty</span></span>                        | <span data-ttu-id="9a4f7-133">Ja</span><span class="sxs-lookup"><span data-stu-id="9a4f7-133">Yes</span></span>           |



 

 




