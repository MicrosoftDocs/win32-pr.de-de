---
description: Weist Enumerationstext einem Wertebereich zu. Jedes enumrange-Element gibt einen Minimalwert an und erstreckt sich bis zum nächsten Element Minimalwert oder bis keine weiteren enumrange-Elemente vorhanden sind.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959359"
---
# <a name="enumrange"></a><span data-ttu-id="64e75-104">enumbereich</span><span class="sxs-lookup"><span data-stu-id="64e75-104">enumRange</span></span>

<span data-ttu-id="64e75-105">Weist Enumerationstext einem Wertebereich zu.</span><span class="sxs-lookup"><span data-stu-id="64e75-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="64e75-106">Jedes [enumrange]() -Element gibt einen Minimalwert an und erstreckt sich bis zum nächsten Element Minimalwert oder bis keine weiteren enumrange-Elemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="64e75-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e75-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64e75-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="64e75-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="64e75-108">Element Information</span></span>



| <span data-ttu-id="64e75-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="64e75-109">Parent Element</span></span>                                         | <span data-ttu-id="64e75-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64e75-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="64e75-111">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="64e75-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="64e75-112">none</span><span class="sxs-lookup"><span data-stu-id="64e75-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="64e75-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="64e75-113">Attributes</span></span>



| <span data-ttu-id="64e75-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="64e75-114">Attribute</span></span> | <span data-ttu-id="64e75-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64e75-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e75-116">minValue</span><span class="sxs-lookup"><span data-stu-id="64e75-116">minValue</span></span>  | <span data-ttu-id="64e75-117">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-117">Public.</span></span> <span data-ttu-id="64e75-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-118">Required.</span></span> <span data-ttu-id="64e75-119">Der Minimalwert im Bereich.</span><span class="sxs-lookup"><span data-stu-id="64e75-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="64e75-120">setValue</span><span class="sxs-lookup"><span data-stu-id="64e75-120">setValue</span></span>  | <span data-ttu-id="64e75-121">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-121">Public.</span></span> <span data-ttu-id="64e75-122">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="64e75-122">Optional.</span></span> <span data-ttu-id="64e75-123">Wenn ein Benutzer diese Enumeration aus einem ListBox-Eigenschaften Steuerelement auswählt, wird dieser diskrete Wert als Eigenschafts Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="64e75-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="64e75-124">text</span><span class="sxs-lookup"><span data-stu-id="64e75-124">text</span></span>      | <span data-ttu-id="64e75-125">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-125">Public.</span></span> <span data-ttu-id="64e75-126">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="64e75-126">Optional.</span></span> <span data-ttu-id="64e75-127">Der Text, der verwendet wird, um den Enumerationswert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64e75-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="64e75-128">Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, damit Sie lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="64e75-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="64e75-129">Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="64e75-129">mnemonics</span></span> | <span data-ttu-id="64e75-130">**Windows 7 und höher.**</span><span class="sxs-lookup"><span data-stu-id="64e75-130">**Windows 7 and later.**</span></span> <span data-ttu-id="64e75-131">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-131">Public.</span></span> <span data-ttu-id="64e75-132">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="64e75-132">Optional.</span></span> <span data-ttu-id="64e75-133">Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="64e75-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="64e75-134">Die Liste wird durch das \| Zeichen "" getrennt.</span><span class="sxs-lookup"><span data-stu-id="64e75-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="64e75-135">name</span><span class="sxs-lookup"><span data-stu-id="64e75-135">name</span></span>      | <span data-ttu-id="64e75-136">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64e75-136">Required.</span></span> <span data-ttu-id="64e75-137">Der kanonische Eigenschaftsname, der für das System eindeutig ist. Beispiel: System. Rating.</span><span class="sxs-lookup"><span data-stu-id="64e75-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="64e75-138">Dieses Attribut ist auf 64 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="64e75-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="64e75-139">Beim Namen wird die Groß-/Kleinschreibung beachtet, und es sollte die folgende Syntax verwendet werden: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="64e75-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="64e75-140">Die folgenden Methoden geben diesen Wert zurück: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**ipropertydescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)und [**ipropertyui:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64e75-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
