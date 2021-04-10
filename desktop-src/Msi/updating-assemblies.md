---
description: Die Informationen in diesem Thema enthalten die empfohlenen Richtlinien zum Aktualisieren von Assemblys mithilfe von Windows Installer Patches.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Aktualisieren von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b185a9943ba20c81a1fa3431dd590eb05648c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050601"
---
# <a name="updating-assemblies"></a>Aktualisieren von Assemblys

Die Informationen in diesem Thema enthalten die empfohlenen Richtlinien zum Aktualisieren von Assemblys mithilfe von Windows Installer Patches.

Autoren von Assemblyaktualisierungen können die folgenden Richtlinien verwenden, die für alle Typen von Assemblys gelten:

-   Die empfohlene Methode zum Aktualisieren einer Assembly besteht darin, den starken Namen der Assembly in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)zu ändern. Die neue Assemblyversion kann durch eine neue Komponente oder durch dieselbe Komponente bereitgestellt werden, die die alte Version bereitstellt.
-   Wenn die neue Assemblyversion von der gleichen Komponente bereitgestellt wird, ändern Sie den Assemblytyp nicht von einer .NET Framework-Assembly in eine Win32-Assembly oder umgekehrt.
-   Wenn alle Anwendungen auf dem System die aktualisierte Assembly verwenden müssen, sollten Sie eine Richtlinienassembly bereitstellen. Eine Richtlinienassembly kann Anwendungen auf dem System umleiten, um die neue Assemblyversion zu verwenden. Richtlinienassemblys sollten durch Erstellen einer neuen Komponente bereitgestellt werden.
-   Zum Deinstallieren von Assemblyaktualisierungen ist Windows Installer 3,0 oder höher erforderlich. Weitere Informationen finden Sie unter [Entfernen von Patches](removing-patches.md).
-   Die neuere Version der Assembly sollte dieselbe oder eine höhere Version der Dateien aus zuvor veröffentlichten Assemblys enthalten.
-   Windows Installer 3,0 kann .NET Framework und Win32-Assemblys durch eine komplette Datei Ersetzung oder durch ein kleineres Delta Update bedienen. Weitere Informationen finden Sie unter [verringern der Patchgröße](reducing-patch-size.md).
-   Wenn das Update den starken Namen der Assembly ändert, sind die [msipatcholdassemblyfile](msipatcholdassemblyfile-table.md) -Tabelle und die [msipatcholdassemblyname](msipatcholdassemblyname-table.md) -Tabelle erforderlich, wenn das Patchpaket nicht über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle verfügt. Die msipatcholdassemblyfile-Tabelle und die msipatcholdassemblyname-Tabelle sind nicht erforderlich, wenn das Patchpaket Informationen zur Patchsequenzierung in einer msipatchsequence-Tabelle aufweist.
-   Vor dem Freigeben eines neuen Patches testen Sie den Patch, indem Sie ihn mit allen zuvor veröffentlichten Patches anwenden.

## <a name="updating-win32-assemblies"></a>Aktualisieren von Win32

Beachten Sie beim Aktualisieren von Win32-Assemblys die folgenden Richtlinien:

-   Ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)angegeben ist.
-   Wenn Sie möchten, dass die Anwendung immer die neue Version der Assembly verwendet, ohne dass sich dies auf die von anderen Anwendungen auf dem System verwendete Assemblyversion auswirkt, verwenden Sie die gleiche Komponente, um die neue Assemblyversion zu verwenden, die Sie für die alte Assemblyversion Behalten Sie die gleiche ComponentID in der [Component](component-table.md) -Tabelle bei. Nachdem die Anwendung gepatcht wurde, enthält Sie nur einen Verweis auf die neue Version der Assembly. Die alte Version der Assembly kann mit der neuen Version im globalen Assemblycache verbleiben. Dies wirkt sich nicht auf andere Anwendungen auf dem System aus, die die alte Version der Assembly verwenden. Wenn dieselbe Komponente sowohl für die neue als auch für die alte Version der Assembly verwendet wird, kann es sich bei dem Update um einen kleineren Delta Patch handeln.
-   Wenn die neue Version der Assembly nicht mit allen Systemen kompatibel ist, auf denen Sie Ihre Anwendung installieren möchten, können Sie die neue und alte Version der Assembly als parallele Assemblys installieren. Um beide Assemblyversionen nebeneinander zu installieren, erstellen Sie eine neue-Komponente, die die neue Assemblyversion enthält. Die ComponentID in der [Komponenten](component-table.md) Tabelle für die neue Komponente sollte sich von der Komponenten-ID der Komponente mit der alten Version unterscheiden. Nachdem die Anwendung gepatcht wurde, enthält Sie Verweise auf beide Assemblyversionen. Anschließend kann die Anwendung durch ein Manifest an die kompatible Version der Assembly weitergeleitet werden. Wenn verschiedene Komponenten für die neue und alte Version der Assembly verwendet werden, wird für das Update der vollständige Dateiaustausch verwendet.

## <a name="updating-net-framework-assemblies"></a>Aktualisieren .NET Framework Assemblys

Verwenden Sie die folgenden Richtlinien, wenn Sie .NET Framework Assemblys Aktualisieren.

-   Ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)angegeben ist.
-   Wenn Sie möchten, dass die Anwendung immer die neue Version der Assembly verwendet, ohne die von anderen Anwendungen auf dem System verwendete Assemblyversion zu beeinträchtigen, ändern Sie den starken Namen der neuen Assembly, die in der [Tabelle MsiAssemblyName](msiassemblyname-table.md)angegeben ist, und verwenden Sie dieselbe Komponente, um die neue Assemblyversion aufzunehmen, die Sie für die alte Assemblyversion verwendet haben Behalten Sie die gleiche ComponentID in der [Component](component-table.md) -Tabelle bei. Nachdem die Anwendung gepatcht wurde, enthält Sie nur einen Verweis auf die neue Version der Assembly. Die alte Version der Assembly kann mit der neuen Version im globalen Cache verbleiben. Dies wirkt sich nicht auf andere Anwendungen auf dem System aus, die die alte Version der Assembly verwenden. Wenn dieselbe Komponente sowohl für die neue als auch für die alte Version der Assembly verwendet wird, kann es sich bei dem Update um einen kleineren Delta Patch handeln.
-   Wenn die neue Version der Assembly nicht mit allen Systemen kompatibel ist, auf denen Sie Ihre Anwendung installieren möchten, können Sie die neue und alte Version der Assembly als parallele Assemblys installieren. Um beide Assemblyversionen nebeneinander zu installieren, ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)angegeben ist, und erstellen Sie eine neue-Komponente, die die neue Assemblyversion enthält. Die ComponentID in der [Komponenten](component-table.md) Tabelle für die neue Komponente sollte sich von der Komponenten-ID der Komponente mit der alten Version unterscheiden. Nachdem die Anwendung gepatcht wurde, enthält Sie Verweise auf beide Assemblyversionen. Die Anwendung kann dann durch ein Manifest an die kompatible Version der Assembly weitergeleitet werden. Wenn verschiedene Komponenten für die neue und alte Version der Assembly verwendet werden, wird für das Update der vollständige Dateiaustausch verwendet.
-   Ein direktes Update überschreibt die Kopie einer .NET Framework-Assembly im globalen Assemblycache. Bei dieser Art von Assemblyaktualisierung wird der starke Name der Assembly nicht geändert. Nur der Wert im Feld "File Version" der [Tabelle "MsiAssemblyName](msiassemblyname-table.md) " wird geändert. Für das direkte Update einer .NET Framework Assembly ist .NET Framework 1,1 SP1 oder höher erforderlich.
    > [!Note]  
    > Der direkte Updatetyp überschreibt die Kopie der Assembly im globalen Cache und kann andere Anwendungen unterbrechen, wenn die neue Version der Assembly nicht vollständig abwärts kompatibel ist. Die empfohlene Methode zum Aktualisieren einer Assembly besteht darin, den starken Namen der Assembly in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)zu ändern.

     

 

 



