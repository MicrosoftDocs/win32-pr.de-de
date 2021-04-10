---
description: ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zur gleichen Komponente wie die Verknüpfung selbst gehört, oder ob die Attribute der Zielkomponente sicherstellen, dass die Installations Speicherorte nicht geändert werden.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960484"
---
# <a name="ice67"></a><span data-ttu-id="5120d-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="5120d-103">ICE67</span></span>

<span data-ttu-id="5120d-104">ICE67 überprüft, ob das Ziel einer nicht angekündigten Verknüpfung zur gleichen Komponente wie die Verknüpfung selbst gehört, oder ob die Attribute der Zielkomponente sicherstellen, dass die Installations Speicherorte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5120d-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="5120d-105">Wenn eine Warnung oder ein Fehler, der von ICE67 gemeldet wird, nicht behoben werden kann, kann die Verknüpfung ungültig werden, wenn die Zielkomponente den Zustand ändert und die Quell Komponente dies nicht bewirkt.</span><span class="sxs-lookup"><span data-stu-id="5120d-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="5120d-106">Wenn z. b. die Komponente der Zieldatei auf "aus Quelle ausführen" festgelegt ist, führt eine Neuinstallation, bei der die Komponente in "lokal" geändert wird, dazu, dass die Komponente mit der Verknüpfung nicht neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="5120d-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="5120d-107">Daher verweist die Verknüpfung auf einen ungültigen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="5120d-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="5120d-108">Beachten Sie, dass die Verwendung einer anderen Komponente für die Verknüpfung in einigen Fällen unvermeidlich ist.</span><span class="sxs-lookup"><span data-stu-id="5120d-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="5120d-109">Wenn die Verknüpfung z. b. im Benutzerprofil erstellt wird und die Datei in einem Verzeichnis ohne Profil installiert wird, können Sie möglicherweise nicht die gleiche Komponente für beide Datenelemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="5120d-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="5120d-110">(Dies führt zu Fehlern in Szenarios mit mehreren Benutzern – z. b. in [ICE57](ice57.md)).</span><span class="sxs-lookup"><span data-stu-id="5120d-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="5120d-111">In diesem Fall können Sie möglicherweise angekündigte Verknüpfungen verwenden, um das gewünschte Verhalten zu erreichen, oder Sie können einfach sicherstellen, dass die Zielkomponente nicht von der Quelle in den lokalen Typ geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5120d-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="5120d-112">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="5120d-112">Result</span></span>

<span data-ttu-id="5120d-113">ICE67 gibt einen Fehler oder eine Warnung aus, wenn das Ziel einer nicht angekündigten Verknüpfung nicht zur gleichen Komponente wie die Verknüpfung selbst gehört, oder wenn die Attribute der Zielkomponente nicht sicherstellen, dass die Installations Speicherorte nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5120d-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="5120d-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5120d-114">Example</span></span>

<span data-ttu-id="5120d-115">ICE67 meldet die folgenden Warnungen und Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5120d-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="5120d-116">Shortcut1 wird von Component2 installiert, aber die Zieldatei file1 wird von Component1 installiert.</span><span class="sxs-lookup"><span data-stu-id="5120d-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="5120d-117">Die Zielkomponente ist als optional gekennzeichnet (was bedeutet, dass Sie lokal oder von der Quelle aus ausgeführt werden kann).</span><span class="sxs-lookup"><span data-stu-id="5120d-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="5120d-118">Eine mögliche Situation, die zu einem Problem führt, besteht darin, dass Component1 von der Quelle in den lokalen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="5120d-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="5120d-119">Dies würde dazu führen, dass Shortcut1 auf einen ungültigen Speicherort verweist.</span><span class="sxs-lookup"><span data-stu-id="5120d-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="5120d-120">Um diese Warnung zu beheben, installieren Sie die Verknüpfung als Teil von Component1, oder markieren Sie Component1 als LocalOnly oder sourceOnly.</span><span class="sxs-lookup"><span data-stu-id="5120d-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="5120d-121">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5120d-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5120d-122">File</span><span class="sxs-lookup"><span data-stu-id="5120d-122">File</span></span>  | <span data-ttu-id="5120d-123">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="5120d-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="5120d-124">Datei1</span><span class="sxs-lookup"><span data-stu-id="5120d-124">File1</span></span> | <span data-ttu-id="5120d-125">Component1</span><span class="sxs-lookup"><span data-stu-id="5120d-125">Component1</span></span>  |



 

<span data-ttu-id="5120d-126">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5120d-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="5120d-127">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="5120d-127">Shortcut</span></span>  | <span data-ttu-id="5120d-128">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="5120d-128">Component\_</span></span> | <span data-ttu-id="5120d-129">Ziel</span><span class="sxs-lookup"><span data-stu-id="5120d-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="5120d-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="5120d-130">Shortcut1</span></span> | <span data-ttu-id="5120d-131">Component2</span><span class="sxs-lookup"><span data-stu-id="5120d-131">Component2</span></span>  | <span data-ttu-id="5120d-132">\[\#File1\]</span><span class="sxs-lookup"><span data-stu-id="5120d-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="5120d-133">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="5120d-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5120d-134">Komponente</span><span class="sxs-lookup"><span data-stu-id="5120d-134">Component</span></span>  | <span data-ttu-id="5120d-135">Attribute</span><span class="sxs-lookup"><span data-stu-id="5120d-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="5120d-136">Component1</span><span class="sxs-lookup"><span data-stu-id="5120d-136">Component1</span></span> | <span data-ttu-id="5120d-137">2</span><span class="sxs-lookup"><span data-stu-id="5120d-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="5120d-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5120d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5120d-139">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="5120d-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



