---
title: QuickAccessToolbar-Element
description: Stellt die Schnellzugriffssymbolleiste (Quick Access Toolbar, QAT) dar, eine kleine Symbolleiste, die Verknüpfungen zu Menübandbefehlen anzeigt.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- QuickAccessToolbar-Element Windows-Menüband
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443301"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="ed084-104">QuickAccessToolbar-Element</span><span class="sxs-lookup"><span data-stu-id="ed084-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="ed084-105">Stellt die [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md)dar, eine kleine Symbolleiste, die Verknüpfungen zu Menübandbefehlen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ed084-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="ed084-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ed084-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="ed084-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed084-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed084-108">attribute</span><span class="sxs-lookup"><span data-stu-id="ed084-108">Attribute</span></span></th>
<th><span data-ttu-id="ed084-109">Typ</span><span class="sxs-lookup"><span data-stu-id="ed084-109">Type</span></span></th>
<th><span data-ttu-id="ed084-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ed084-110">Required</span></span></th>
<th><span data-ttu-id="ed084-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed084-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed084-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ed084-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ed084-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="ed084-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ed084-114">Nein</span><span class="sxs-lookup"><span data-stu-id="ed084-114">No</span></span><br/></td>
<td><span data-ttu-id="ed084-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed084-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ed084-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="ed084-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ed084-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ed084-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ed084-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ed084-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ed084-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed084-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed084-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ed084-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ed084-121">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="ed084-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ed084-122">Nein</span><span class="sxs-lookup"><span data-stu-id="ed084-122">No</span></span><br/></td>
<td><span data-ttu-id="ed084-123">Fügt ein zusätzliches Befehlselement in das QAT-Menü ein.</span><span class="sxs-lookup"><span data-stu-id="ed084-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="ed084-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="ed084-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="ed084-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ed084-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ed084-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ed084-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ed084-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed084-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ed084-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed084-128">Child elements</span></span>



| <span data-ttu-id="ed084-129">Element</span><span class="sxs-lookup"><span data-stu-id="ed084-129">Element</span></span>                                                                                                                   | <span data-ttu-id="ed084-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed084-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ed084-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="ed084-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="ed084-132">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="ed084-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ed084-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed084-133">Parent elements</span></span>



| <span data-ttu-id="ed084-134">Element</span><span class="sxs-lookup"><span data-stu-id="ed084-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed084-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="ed084-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ed084-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed084-136">Remarks</span></span>

<span data-ttu-id="ed084-137">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ed084-137">Required.</span></span>

<span data-ttu-id="ed084-138">Muss genau einmal für jede [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="ed084-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="ed084-139">Elemente in der QAT können zur Laufzeit hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ed084-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="ed084-140">Aus Gründen der Konsistenz zwischen Menübandanwendungen wird empfohlen, dass der *Befehlshandler CustomizeCommandName* ein QAT-Anpassungsdialogfeld startet.</span><span class="sxs-lookup"><span data-stu-id="ed084-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="ed084-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed084-141">Examples</span></span>

<span data-ttu-id="ed084-142">Im folgenden Beispiel wird das grundlegende Markup für **quickAccessToolbar** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ed084-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="ed084-143">Dieser Codeabschnitt zeigt die **QuickAccessToolbar-Befehlsdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="ed084-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="ed084-144">Dieser Codeabschnitt zeigt die **QuickAccessToolbar-Steuerelementdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="ed084-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="ed084-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ed084-145">Element information</span></span>

* <span data-ttu-id="ed084-146">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed084-146">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="ed084-147">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="ed084-147">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ed084-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed084-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed084-149">Symbolleisten-Steuerelement für den Schnellzugriff</span><span class="sxs-lookup"><span data-stu-id="ed084-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





