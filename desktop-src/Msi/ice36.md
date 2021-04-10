---
description: ICE36 überprüft, ob jedes Symbol in der Symboltabelle mindestens ein Mal in der arpproducticon-Eigenschaft oder in der Klassen-, ProgID-oder Verknüpfungs Tabelle aufgeführt ist.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042536"
---
# <a name="ice36"></a><span data-ttu-id="e90d5-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="e90d5-103">ICE36</span></span>

<span data-ttu-id="e90d5-104">ICE36 überprüft, ob jedes Symbol in der Symboltabelle mindestens ein Mal in der [**arpproducticon**](arpproducticon.md) -Eigenschaft oder in der [Klassen](class-table.md)-, [ProgID](progid-table.md)- [oder Verknüpfungs Tabelle aufgeführt](shortcut-table.md) ist.</span><span class="sxs-lookup"><span data-stu-id="e90d5-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="e90d5-105">Während der Ankündigung werden alle in der [Symboltabelle](icon-table.md) aufgeführten Symbole auf dem Computer des Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="e90d5-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="e90d5-106">Wenn nicht verwendete Symbole in der Symboltabelle vorhanden sind, kann die Installation nicht ausgeführt werden. es wird jedoch die Größe der MSI-Datei und die Zeit und den Speicherplatz, die für die Ankündigung einer Funktion erforderlich sind, unnötig vergrößert.</span><span class="sxs-lookup"><span data-stu-id="e90d5-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="e90d5-107">Wenn in der Eigenschaft oder Tabelle nicht auf ein Symbol verwiesen wird und keine Benutzeroberfläche zum Erstellen eines Verweises zur Laufzeit bereitgestellt wird, sollten Sie das Symbol entfernen, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="e90d5-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="e90d5-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e90d5-108">Result</span></span>

<span data-ttu-id="e90d5-109">ICE36 sendet eine Meldung, wenn ein Symbol in der Symboltabelle vorhanden ist, auf das in der [Klasse](class-table.md), der [ProgID](progid-table.md)oder [der Verknüpfungs Tabelle nicht](shortcut-table.md) verwiesen wird, und wenn keine Benutzeroberfläche bereitgestellt wird, um einen solchen Verweis zur Laufzeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e90d5-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="e90d5-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e90d5-110">Example</span></span>

<span data-ttu-id="e90d5-111">ICE36 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e90d5-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="e90d5-112">[Symboltabelle](icon-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e90d5-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="e90d5-113">Name</span><span class="sxs-lookup"><span data-stu-id="e90d5-113">Name</span></span>  | <span data-ttu-id="e90d5-114">Daten</span><span class="sxs-lookup"><span data-stu-id="e90d5-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="e90d5-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="e90d5-115">Icon1</span></span> | <span data-ttu-id="e90d5-116">Control1</span><span class="sxs-lookup"><span data-stu-id="e90d5-116">Control1</span></span> |
| <span data-ttu-id="e90d5-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="e90d5-117">Icon2</span></span> | <span data-ttu-id="e90d5-118">Control2</span><span class="sxs-lookup"><span data-stu-id="e90d5-118">Control2</span></span> |
| <span data-ttu-id="e90d5-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="e90d5-119">Icon3</span></span> | <span data-ttu-id="e90d5-120">Control3</span><span class="sxs-lookup"><span data-stu-id="e90d5-120">Control3</span></span> |
| <span data-ttu-id="e90d5-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="e90d5-121">Icon4</span></span> | <span data-ttu-id="e90d5-122">Control4</span><span class="sxs-lookup"><span data-stu-id="e90d5-122">Control4</span></span> |



 

<span data-ttu-id="e90d5-123">[ProgID-Tabelle](progid-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e90d5-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="e90d5-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="e90d5-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="e90d5-125">Property1</span><span class="sxs-lookup"><span data-stu-id="e90d5-125">Property1</span></span> |



 

<span data-ttu-id="e90d5-126">[Klassen Tabelle](class-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e90d5-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="e90d5-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="e90d5-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="e90d5-128">{3e469aba-3644-11d2-8892-00a0c981b015}</span><span class="sxs-lookup"><span data-stu-id="e90d5-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="e90d5-129">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e90d5-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="e90d5-130">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="e90d5-130">Shortcut</span></span>  | <span data-ttu-id="e90d5-131">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="e90d5-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="e90d5-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="e90d5-132">Shortcut1</span></span> | <span data-ttu-id="e90d5-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="e90d5-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="e90d5-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e90d5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e90d5-135">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e90d5-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



