---
description: Enthält den Inhalt für eine Journal Seite.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content-Element [Journal Reader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349975"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="24814-103">Inhalts Element- \[ Journal Leser\]</span><span class="sxs-lookup"><span data-stu-id="24814-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="24814-104">Enthält den Inhalt für eine Journal Seite.</span><span class="sxs-lookup"><span data-stu-id="24814-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="24814-105">Definition</span><span class="sxs-lookup"><span data-stu-id="24814-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="24814-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24814-106">Parent Elements</span></span>

[<span data-ttu-id="24814-107">**Journalpage**</span><span class="sxs-lookup"><span data-stu-id="24814-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="24814-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24814-108">Child Elements</span></span>

[<span data-ttu-id="24814-109">**-Gruppenknoten**</span><span class="sxs-lookup"><span data-stu-id="24814-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="24814-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="24814-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="24814-111">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="24814-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="24814-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="24814-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="24814-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="24814-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="24814-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="24814-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="24814-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="24814-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24814-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="24814-116">Attribute</span></span></th>
<th><span data-ttu-id="24814-117">type</span><span class="sxs-lookup"><span data-stu-id="24814-117">Type</span></span></th>
<th><span data-ttu-id="24814-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="24814-118">Required</span></span></th>
<th><span data-ttu-id="24814-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24814-119">Description</span></span></th>
<th><span data-ttu-id="24814-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="24814-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24814-121"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="24814-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="24814-122"><a href="contenttype-complex-type.md"><strong>ComplexType für ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="24814-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="24814-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="24814-123">Required</span></span></td>
<td><span data-ttu-id="24814-124">Wenn der Typ " &quot; inert" ist &quot; , kann der Inhalt nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="24814-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="24814-125">Normal</span><span class="sxs-lookup"><span data-stu-id="24814-125">Normal</span></span></li>
<li><span data-ttu-id="24814-126">Schwei</span><span class="sxs-lookup"><span data-stu-id="24814-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="24814-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="24814-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="24814-128">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="24814-128">Element type</span></span> | <span data-ttu-id="24814-129">ComplexType für [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="24814-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="24814-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="24814-130">Namespace</span></span>    | <span data-ttu-id="24814-131">urn: Schemas-Microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="24814-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="24814-132">Schemaname</span><span class="sxs-lookup"><span data-stu-id="24814-132">Schema name</span></span>  | <span data-ttu-id="24814-133">Journal Leser</span><span class="sxs-lookup"><span data-stu-id="24814-133">Journal Reader</span></span>                                              |



 

 

 




