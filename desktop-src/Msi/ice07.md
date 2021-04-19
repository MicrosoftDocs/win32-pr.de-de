---
description: ICE07 überprüft, ob das Installationspaket angibt, dass die Schriftarten in den Ordner "fonsor" installiert werden. Wenn eine Schriftart in einem anderen Ordner als dem Ordner "fonsorfolder" installiert wird, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362568"
---
# <a name="ice07"></a><span data-ttu-id="6fab1-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="6fab1-104">ICE07</span></span>

<span data-ttu-id="6fab1-105">ICE07 überprüft, ob das Installationspaket angibt, dass die Schriftarten in den Ordner "fonsor" installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6fab1-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="6fab1-106">Wenn eine Schriftart in einem anderen Ordner als dem Ordner "fonsorfolder" installiert wird, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6fab1-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="6fab1-107">Die benutzerdefinierte Aktion ICE07 führt die folgenden Aktionen für jede Schriftart in der [Schriftart Tabelle](font-table.md)aus.</span><span class="sxs-lookup"><span data-stu-id="6fab1-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="6fab1-108">Sucht die Schriftart Datei, zu der jeder Schriftart Titel gehört, mithilfe der [Schriftart Tabelle](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="6fab1-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="6fab1-109">Fragt die Komponenten \_ Spalte der [Dateitabelle](file-table.md) für die Komponente ab, die die einzelnen Dateien steuert.</span><span class="sxs-lookup"><span data-stu-id="6fab1-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="6fab1-110">Fragt die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md) ab, um einen Schlüssel in der Verzeichnis Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6fab1-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="6fab1-111">Löst die [Verzeichnis Tabelle](directory-table.md) auf, um den Namen des Ordners zu bestimmen, in dem das Installationsprogramm die Schriftart Datei installieren soll.</span><span class="sxs-lookup"><span data-stu-id="6fab1-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="6fab1-112">Gibt einen Fehler aus, wenn die Schriftart Datei in einem anderen Ordner als dem Ordner "Foner" installiert wird.</span><span class="sxs-lookup"><span data-stu-id="6fab1-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="6fab1-113">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="6fab1-113">Result</span></span>

<span data-ttu-id="6fab1-114">ICE07 gibt einen Fehler aus, wenn feststellt, dass die Datenbank angibt, dass eine Schriftart Datei in einem anderen Ordner als dem Ordner "Foner" installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fab1-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="6fab1-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6fab1-115">Example</span></span>

<span data-ttu-id="6fab1-116">IC07 würde die folgende Fehlermeldung für das gezeigte Beispiel veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6fab1-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="6fab1-117">Schriftart Tabelle</span><span class="sxs-lookup"><span data-stu-id="6fab1-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="6fab1-118">Datei\_</span><span class="sxs-lookup"><span data-stu-id="6fab1-118">File\_</span></span> | <span data-ttu-id="6fab1-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="6fab1-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="6fab1-120">Myrtle</span><span class="sxs-lookup"><span data-stu-id="6fab1-120">Myrtle</span></span> | <span data-ttu-id="6fab1-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="6fab1-121">Tahoma</span></span>    |



 

<span data-ttu-id="6fab1-122">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6fab1-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="6fab1-123">File</span><span class="sxs-lookup"><span data-stu-id="6fab1-123">File</span></span>   | <span data-ttu-id="6fab1-124">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="6fab1-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="6fab1-125">Myrtle</span><span class="sxs-lookup"><span data-stu-id="6fab1-125">Myrtle</span></span> | <span data-ttu-id="6fab1-126">Myrtle- \_ Strand</span><span class="sxs-lookup"><span data-stu-id="6fab1-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="6fab1-127">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="6fab1-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="6fab1-128">Komponente</span><span class="sxs-lookup"><span data-stu-id="6fab1-128">Component</span></span>     | <span data-ttu-id="6fab1-129">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="6fab1-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="6fab1-130">Myrtle- \_ Strand</span><span class="sxs-lookup"><span data-stu-id="6fab1-130">Myrtle\_Beach</span></span> | <span data-ttu-id="6fab1-131">Sand Leiste</span><span class="sxs-lookup"><span data-stu-id="6fab1-131">SandBar</span></span>     |



 

<span data-ttu-id="6fab1-132">In diesem Beispiel wird die Schriftart Tahoma der Schriftart Datei Myrtle zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6fab1-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="6fab1-133">Die Datei Myrtle gehört zum komponentenstrand der Komponente \_ .</span><span class="sxs-lookup"><span data-stu-id="6fab1-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="6fab1-134">Die Auflösung der Verzeichnis Tabelle zeigt, dass alle Dateien, die zu Myrtle Beach gehören, \_ im Ordner Sand Bar installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6fab1-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="6fab1-135">Da dies nicht der Ordner "Foner" ist, wird von ICE07 eine Fehlermeldung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fab1-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="6fab1-136">Beachten Sie, dass \_ die Schriftart Tahoma möglicherweise nicht zum Myrtle-Strand gehört, wenn der Myrtle-komponentenplatz tatsächlich im Sand leisten Ordner und nicht im Ordner "Foner" gehört \_ .</span><span class="sxs-lookup"><span data-stu-id="6fab1-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="6fab1-137">Eine mögliche Lösung für den Fehler wäre das Einschließen von Tahoma in eine andere Komponente, die im Verzeichnis "fonsorfolder" installiert wird.</span><span class="sxs-lookup"><span data-stu-id="6fab1-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fab1-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fab1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fab1-139">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="6fab1-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



