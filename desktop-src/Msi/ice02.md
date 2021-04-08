---
description: ICE02 überprüft, ob bestimmte Verweise zwischen der Komponente, der Datei und den Registrierungs Tabellen einander unterliegen. Diese Verweise müssen einander gegenseitig sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen konnte.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750136"
---
# <a name="ice02"></a><span data-ttu-id="1bd81-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="1bd81-104">ICE02</span></span>

<span data-ttu-id="1bd81-105">ICE02 überprüft, ob bestimmte Verweise zwischen der [Komponente](component-table.md), der [Datei](file-table.md)und den [Registrierungs](registry-table.md) Tabellen einander unterliegen.</span><span class="sxs-lookup"><span data-stu-id="1bd81-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="1bd81-106">Diese Verweise müssen einander gegenseitig sein, damit das Installationsprogramm den Installationsstatus von Komponenten ordnungsgemäß bestimmen konnte.</span><span class="sxs-lookup"><span data-stu-id="1bd81-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="1bd81-107">Das Installationsprogramm verwendet die KEYPATH-Spalte der Component-Tabelle, um zu erkennen, ob die in der Component-Spalte aufgeführte Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1bd81-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="1bd81-108">Die KEYPATH-Spalte enthält einen Schlüssel in die Registrierungs-oder Datei Tabellen.</span><span class="sxs-lookup"><span data-stu-id="1bd81-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="1bd81-109">Beide Tabellen haben eine Komponenten \_ Spalte, die einen Schlüssel zurück in die Komponenten Tabelle enthält, der auf die Komponente verweist, die den Registrierungs Eintrag bzw. die Registrierungsdatei steuert.</span><span class="sxs-lookup"><span data-stu-id="1bd81-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="1bd81-110">Diese Verweise müssen einander gegenseitig sein.</span><span class="sxs-lookup"><span data-stu-id="1bd81-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="1bd81-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="1bd81-111">Result</span></span>

<span data-ttu-id="1bd81-112">ICE02 gibt eine Fehlermeldung aus, wenn ein Verweis gefunden wird, der gegenseitig sein soll und nicht ist.</span><span class="sxs-lookup"><span data-stu-id="1bd81-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="1bd81-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1bd81-113">Example</span></span>

<span data-ttu-id="1bd81-114">ICE02 würde die folgende Fehlermeldung für eine MSI-Datei mit den angezeigten Datenbankeinträgen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="1bd81-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="1bd81-115">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1bd81-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="1bd81-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="1bd81-116">Component</span></span> | <span data-ttu-id="1bd81-117">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="1bd81-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="1bd81-118">Red</span><span class="sxs-lookup"><span data-stu-id="1bd81-118">Red</span></span>       | <span data-ttu-id="1bd81-119">Rote \_ Datei</span><span class="sxs-lookup"><span data-stu-id="1bd81-119">Red\_File</span></span> |
| <span data-ttu-id="1bd81-120">Blau</span><span class="sxs-lookup"><span data-stu-id="1bd81-120">Blue</span></span>      | <span data-ttu-id="1bd81-121">Rote \_ Datei</span><span class="sxs-lookup"><span data-stu-id="1bd81-121">Red\_File</span></span> |



 

<span data-ttu-id="1bd81-122">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="1bd81-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="1bd81-123">Datei Spalte</span><span class="sxs-lookup"><span data-stu-id="1bd81-123">File Column</span></span> | <span data-ttu-id="1bd81-124">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="1bd81-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="1bd81-125">Rote \_ Datei</span><span class="sxs-lookup"><span data-stu-id="1bd81-125">Red\_File</span></span>   | <span data-ttu-id="1bd81-126">Red</span><span class="sxs-lookup"><span data-stu-id="1bd81-126">Red</span></span>         |
| <span data-ttu-id="1bd81-127">Blaue \_ Datei</span><span class="sxs-lookup"><span data-stu-id="1bd81-127">Blue\_File</span></span>  | <span data-ttu-id="1bd81-128">Blau</span><span class="sxs-lookup"><span data-stu-id="1bd81-128">Blue</span></span>        |



 

<span data-ttu-id="1bd81-129">Die Komponente blau verweist \_ auf die rote Datei, aber \_ die rote Datei wird nicht von der Komponente blau gesteuert und kann daher nicht die KEYPATH-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="1bd81-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="1bd81-130">Wenn das Installationsprogramm aufgerufen wurde, um den Installationsstatus blau zu erhalten, würde fälschlicherweise überprüft, ob die rote \_ Datei installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1bd81-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="1bd81-131">Wenn Sie das Feld "KEYPATH" für Blau in der Komponenten Tabelle in die blaue Datei ändern, wird \_ der Fehler behoben.</span><span class="sxs-lookup"><span data-stu-id="1bd81-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd81-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bd81-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd81-133">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="1bd81-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



