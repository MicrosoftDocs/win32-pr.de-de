---
description: ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüssel Pfad für eine Komponente verwendet werden, in der Tabelle "| atefolder" aufgeführt sind.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350488"
---
# <a name="ice18"></a><span data-ttu-id="92649-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="92649-103">ICE18</span></span>

<span data-ttu-id="92649-104">ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüssel Pfad für eine Komponente verwendet werden, in der Tabelle "| [atefolder](createfolder-table.md)" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="92649-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="92649-105">Wenn die KEYPATH-Spalte der [Komponenten Tabelle](component-table.md) NULL ist, bedeutet dies, dass das in der Spalte Verzeichnis aufgeführte Verzeichnis \_ der Schlüssel Pfad für diese Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="92649-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="92649-106">Da Ordner, die vom Installationsprogramm erstellt werden, gelöscht werden, wenn Sie leer sind, muss dieser Ordner in der [Tabelle](createfolder-table.md) "" erstellt werden, um zu verhindern, dass das Installationsprogramm jedes Mal versucht, eine Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="92649-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="92649-107">Machen Sie das Verzeichnis System Folder nicht zum Schlüssel Pfad einer Komponente.</span><span class="sxs-lookup"><span data-stu-id="92649-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="92649-108">Da dieser Ordner auf jedem Betriebssystem vorhanden ist, erkennt das Installationsprogramm immer den Schlüssel Pfad, unabhängig davon, ob die Komponente vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="92649-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="92649-109">In diesem Fall sollte der Schlüssel Pfad eine Datei, ein Registrierungs Eintrag oder eine ODBC-Datenquelle sein.</span><span class="sxs-lookup"><span data-stu-id="92649-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="92649-110">Beim Durchführen einer Validierung wird zuerst überprüft, ob Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="92649-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="92649-111">Die KEYPATH-Spalte der [Component-Tabelle](component-table.md) enthält einen NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="92649-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="92649-112">Es sind keine Dateien für die Komponente in der [Dateitabelle](file-table.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="92649-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="92649-113">Es sind keine Dateien für die in der [Tabelle "RemoveFile](removefile-table.md) " aufgeführte Komponente vorhanden, und der Wert in "dirproperty" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.</span><span class="sxs-lookup"><span data-stu-id="92649-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="92649-114">Es sind keine Dateien für die in der [duplicatefile-Tabelle](duplicatefile-table.md) aufgeführte Komponente vorhanden, und der Wert im Ordner "destfolder" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.</span><span class="sxs-lookup"><span data-stu-id="92649-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="92649-115">Es sind keine Dateien für die in der [Tabelle "muvefile](movefile-table.md) " aufgeführten Komponenten vorhanden, und der Wert im Ordner "destfolder" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.</span><span class="sxs-lookup"><span data-stu-id="92649-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="92649-116">Wenn diese alle zutreffen, überprüft ICE18 Folgendes:</span><span class="sxs-lookup"><span data-stu-id="92649-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="92649-117">Die Komponenten \_ Spalte der Tabelle "| [atefolder](createfolder-table.md) " weist den gleichen Wert auf wie die Komponenten Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="92649-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="92649-118">Die Verzeichnis \_ Spalte der Tabelle "| atefolder" hat denselben Wert wie die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="92649-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="92649-119">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="92649-119">Result</span></span>

<span data-ttu-id="92649-120">ICE18 gibt eine Fehlermeldung aus, wenn das Installationspaket ein Verzeichnis als Schlüssel Pfad für die Komponente angibt, die nicht in der Tabelle "| [atefolder](createfolder-table.md)" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="92649-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92649-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92649-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92649-122">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="92649-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



