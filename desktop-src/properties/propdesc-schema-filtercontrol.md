---
description: Gibt an, welches Steuerelement im Header Filter Menü verwendet werden soll.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: FilterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343418"
---
# <a name="filtercontrol"></a><span data-ttu-id="28801-103">FilterControl</span><span class="sxs-lookup"><span data-stu-id="28801-103">filterControl</span></span>

<span data-ttu-id="28801-104">Gibt an, welches Steuerelement im Header Filter Menü verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="28801-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="28801-105">Es darf nur ein [FilterControl]() -Element für jedes [DisplayInfo](./propdesc-schema-displayinfo.md) -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="28801-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="28801-106">Wenn mehrere Elemente vorhanden sind, wird der letzte verwendet.</span><span class="sxs-lookup"><span data-stu-id="28801-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="28801-107">Wenn kein [FilterControl]() -Element bereitgestellt wird, werden die Standard Attribut Einstellungen auf die Eigenschafts Beschreibung angewendet.</span><span class="sxs-lookup"><span data-stu-id="28801-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="28801-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="28801-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="28801-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="28801-109">Element Information</span></span>



| <span data-ttu-id="28801-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="28801-110">Parent Element</span></span>                                   | <span data-ttu-id="28801-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28801-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="28801-112">Display Info</span><span class="sxs-lookup"><span data-stu-id="28801-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="28801-113">Keine</span><span class="sxs-lookup"><span data-stu-id="28801-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="28801-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="28801-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28801-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="28801-115">Attribute</span></span></th>
<th><span data-ttu-id="28801-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28801-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28801-117">Steuerung</span><span class="sxs-lookup"><span data-stu-id="28801-117">control</span></span></td>
<td><span data-ttu-id="28801-118">Öffentlich.</span><span class="sxs-lookup"><span data-stu-id="28801-118">Public.</span></span> <span data-ttu-id="28801-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="28801-119">Optional.</span></span> <span data-ttu-id="28801-120">Der Standardwert ist Default &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="28801-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="28801-121">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="28801-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="28801-122">Wert</span><span class="sxs-lookup"><span data-stu-id="28801-122">Value</span></span></th>
<th><span data-ttu-id="28801-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="28801-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28801-124">Standard</span><span class="sxs-lookup"><span data-stu-id="28801-124">Default</span></span></td>
<td><span data-ttu-id="28801-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="28801-125">Default.</span></span> <span data-ttu-id="28801-126">Verwendet das Standard Steuerelement auf Grundlage des- <typeInfo type=&quot;&quot;> Attributs.</span><span class="sxs-lookup"><span data-stu-id="28801-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="28801-127">Der Standardtyp ist &quot; DateTime, &quot; und das Standard Steuerelement ist &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="28801-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="28801-128">Alle anderen Typen führen zu keinem speziellen Filter Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="28801-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28801-129">Kalender</span><span class="sxs-lookup"><span data-stu-id="28801-129">Calendar</span></span></td>
<td><span data-ttu-id="28801-130">Verwendet das Kalender Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="28801-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28801-131">Rating</span><span class="sxs-lookup"><span data-stu-id="28801-131">Rating</span></span></td>
<td><span data-ttu-id="28801-132">Verwendet das 5-Sterne-Bewertungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="28801-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
