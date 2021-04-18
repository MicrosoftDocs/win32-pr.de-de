---
description: ICE59 prüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die von der Zielfunktion der Verknüpfung installiert werden.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343847"
---
# <a name="ice59"></a><span data-ttu-id="47da4-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="47da4-103">ICE59</span></span>

<span data-ttu-id="47da4-104">ICE59 prüft, ob angekündigte Verknüpfungen zu Komponenten gehören, die von der Zielfunktion der Verknüpfung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="47da4-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="47da4-105">Von ICE59 gemeldete Fehler führen in der Regel zu folgendem Verhalten:</span><span class="sxs-lookup"><span data-stu-id="47da4-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="47da4-106">Die angekündigte Verknüpfung startet die Windows Installer, um das in der Ziel Spalte aufgelistete Feature zu installieren.</span><span class="sxs-lookup"><span data-stu-id="47da4-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="47da4-107">Da die [FeatureComponents-Tabelle](featurecomponents-table.md) die Zielfunktion jedoch nicht der Komponente zuordnet, die die Verknüpfung enthält, wird die keyfile der Komponente (die durch die Verknüpfung aktiviert ist) nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="47da4-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="47da4-108">Daher ist die Verknüpfung beschädigt und führt keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="47da4-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="47da4-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="47da4-109">Result</span></span>

<span data-ttu-id="47da4-110">ICE59 gibt einen Fehler aus, wenn eine angekündigte Verknüpfung nicht zu den Komponenten gehört, die von der Zielfunktion der Verknüpfung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="47da4-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="47da4-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="47da4-111">Example</span></span>

<span data-ttu-id="47da4-112">ICE59 meldet den folgenden Fehler für das gezeigte Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47da4-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="47da4-113">In diesem Fall gibt shortcutb "FeatureA" an und startet bei Aktivierung die Schlüsseldatei von "componentb".</span><span class="sxs-lookup"><span data-stu-id="47da4-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="47da4-114">Obwohl componentb noch nie von FeatureA installiert wird, ist das Ziel der Verknüpfung nicht vorhanden, auch wenn die Installations-on-Demand-Phase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="47da4-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="47da4-115">Um diesen Fehler zu beheben, fügen Sie der [FeatureComponents-Tabelle](featurecomponents-table.md) eine Zeile hinzu, in der Featurekomponenten und componentb verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="47da4-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="47da4-116">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="47da4-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="47da4-117">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="47da4-117">Shortcut</span></span>  | <span data-ttu-id="47da4-118">Ziel</span><span class="sxs-lookup"><span data-stu-id="47da4-118">Target</span></span>   | <span data-ttu-id="47da4-119">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="47da4-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="47da4-120">Shortcutb</span><span class="sxs-lookup"><span data-stu-id="47da4-120">ShortcutB</span></span> | <span data-ttu-id="47da4-121">FeatureA</span><span class="sxs-lookup"><span data-stu-id="47da4-121">FeatureA</span></span> | <span data-ttu-id="47da4-122">Componentb</span><span class="sxs-lookup"><span data-stu-id="47da4-122">ComponentB</span></span>  |



 

[<span data-ttu-id="47da4-123">FeatureComponents-Tabelle</span><span class="sxs-lookup"><span data-stu-id="47da4-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="47da4-124">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="47da4-124">Feature\_</span></span> | <span data-ttu-id="47da4-125">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="47da4-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="47da4-126">FeatureA</span><span class="sxs-lookup"><span data-stu-id="47da4-126">FeatureA</span></span>  | <span data-ttu-id="47da4-127">Componenta</span><span class="sxs-lookup"><span data-stu-id="47da4-127">ComponentA</span></span>  |



 

<span data-ttu-id="47da4-128">[Funktions Tabelle](feature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="47da4-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="47da4-129">Funktion</span><span class="sxs-lookup"><span data-stu-id="47da4-129">Feature</span></span>  | <span data-ttu-id="47da4-130">Ebene</span><span class="sxs-lookup"><span data-stu-id="47da4-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="47da4-131">FeatureA</span><span class="sxs-lookup"><span data-stu-id="47da4-131">FeatureA</span></span> | <span data-ttu-id="47da4-132">10</span><span class="sxs-lookup"><span data-stu-id="47da4-132">10</span></span>    |



 

<span data-ttu-id="47da4-133">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="47da4-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="47da4-134">Komponente</span><span class="sxs-lookup"><span data-stu-id="47da4-134">Component</span></span>  | <span data-ttu-id="47da4-135">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="47da4-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="47da4-136">Componenta</span><span class="sxs-lookup"><span data-stu-id="47da4-136">ComponentA</span></span> | <span data-ttu-id="47da4-137">Mit der</span><span class="sxs-lookup"><span data-stu-id="47da4-137">FileA</span></span>   |
| <span data-ttu-id="47da4-138">Componentb</span><span class="sxs-lookup"><span data-stu-id="47da4-138">ComponentB</span></span> | <span data-ttu-id="47da4-139">FileB</span><span class="sxs-lookup"><span data-stu-id="47da4-139">FileB</span></span>   |



 

<span data-ttu-id="47da4-140">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="47da4-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="47da4-141">File</span><span class="sxs-lookup"><span data-stu-id="47da4-141">File</span></span>  | <span data-ttu-id="47da4-142">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="47da4-142">Component\_</span></span> | <span data-ttu-id="47da4-143">Sequenz</span><span class="sxs-lookup"><span data-stu-id="47da4-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="47da4-144">Mit der</span><span class="sxs-lookup"><span data-stu-id="47da4-144">FileA</span></span> | <span data-ttu-id="47da4-145">Componenta</span><span class="sxs-lookup"><span data-stu-id="47da4-145">ComponentA</span></span>  | <span data-ttu-id="47da4-146">1</span><span class="sxs-lookup"><span data-stu-id="47da4-146">1</span></span>        |
| <span data-ttu-id="47da4-147">FileB</span><span class="sxs-lookup"><span data-stu-id="47da4-147">FileB</span></span> | <span data-ttu-id="47da4-148">Componentb</span><span class="sxs-lookup"><span data-stu-id="47da4-148">ComponentB</span></span>  | <span data-ttu-id="47da4-149">2</span><span class="sxs-lookup"><span data-stu-id="47da4-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47da4-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47da4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47da4-151">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="47da4-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



