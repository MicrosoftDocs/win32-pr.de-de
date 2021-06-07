---
description: Enthält den Inhalt für eine Journalseite.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content-Element [JournalReader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432152"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="0eff2-103">Content Element \[ Journal Reader\]</span><span class="sxs-lookup"><span data-stu-id="0eff2-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="0eff2-104">Enthält den Inhalt für eine Journalseite.</span><span class="sxs-lookup"><span data-stu-id="0eff2-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="0eff2-105">Definition</span><span class="sxs-lookup"><span data-stu-id="0eff2-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="0eff2-106">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0eff2-106">Parent Elements</span></span>

[<span data-ttu-id="0eff2-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="0eff2-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="0eff2-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0eff2-108">Child Elements</span></span>

[<span data-ttu-id="0eff2-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="0eff2-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="0eff2-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="0eff2-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="0eff2-111">**Zeichnung**</span><span class="sxs-lookup"><span data-stu-id="0eff2-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="0eff2-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="0eff2-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="0eff2-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="0eff2-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="0eff2-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="0eff2-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="0eff2-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="0eff2-115">Attributes</span></span>



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
<th><span data-ttu-id="0eff2-116">attribute</span><span class="sxs-lookup"><span data-stu-id="0eff2-116">Attribute</span></span></th>
<th><span data-ttu-id="0eff2-117">Typ</span><span class="sxs-lookup"><span data-stu-id="0eff2-117">Type</span></span></th>
<th><span data-ttu-id="0eff2-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0eff2-118">Required</span></span></th>
<th><span data-ttu-id="0eff2-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eff2-119">Description</span></span></th>
<th><span data-ttu-id="0eff2-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="0eff2-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0eff2-121"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="0eff2-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="0eff2-122"><a href="contenttype-complex-type.md"><strong>complexType: ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0eff2-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="0eff2-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0eff2-123">Required</span></span></td>
<td><span data-ttu-id="0eff2-124">Wenn der Typ &quot; Inert &quot; ist, kann der Inhalt nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0eff2-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="0eff2-125">Normal</span><span class="sxs-lookup"><span data-stu-id="0eff2-125">Normal</span></span></li>
<li><span data-ttu-id="0eff2-126">Inert</span><span class="sxs-lookup"><span data-stu-id="0eff2-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="0eff2-127">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0eff2-127">Element Information</span></span>



|  <span data-ttu-id="0eff2-128">Element</span><span class="sxs-lookup"><span data-stu-id="0eff2-128">Element</span></span>     | <span data-ttu-id="0eff2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0eff2-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="0eff2-130">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="0eff2-130">Element type</span></span> | <span data-ttu-id="0eff2-131">[**complexType: ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="0eff2-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="0eff2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0eff2-132">Namespace</span></span>    | <span data-ttu-id="0eff2-133">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="0eff2-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="0eff2-134">Schemaname</span><span class="sxs-lookup"><span data-stu-id="0eff2-134">Schema name</span></span>  | <span data-ttu-id="0eff2-135">Journalreader</span><span class="sxs-lookup"><span data-stu-id="0eff2-135">Journal Reader</span></span>                                              |



 

 

 




