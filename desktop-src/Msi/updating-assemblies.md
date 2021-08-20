---
description: In den Informationen in diesem Thema werden die empfohlenen Richtlinien zum Aktualisieren von Assemblys mithilfe Windows Installer-Patches beschrieben.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Aktualisieren von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65467613206f3736f35852a919432b11a6761860bd0db22c6da2600c159ef0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141623"
---
# <a name="updating-assemblies"></a>Aktualisieren von Assemblys

In den Informationen in diesem Thema werden die empfohlenen Richtlinien zum Aktualisieren von Assemblys mithilfe Windows Installer-Patches beschrieben.

Autoren von Assemblyupdates können die folgenden Richtlinien verwenden, die für alle Typen von Assemblys gelten:

-   Die empfohlene Methode zum Aktualisieren einer Assembly ist das Ändern des starken Namens der Assembly in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md). Die neue Assemblyversion kann von einer neuen Komponente oder von derselben Komponente bereitgestellt werden, die die alte Version zur Verfügung stellt.
-   Wenn die neue Assemblyversion von derselben Komponente bereitgestellt wird, ändern Sie den Assemblytyp nicht von einer .NET Framework-Assembly in eine Win32-Assembly oder umgekehrt.
-   Wenn alle Anwendungen im System die aktualisierte Assembly verwenden müssen, sollten Sie eine Richtlinien-Assembly bereitstellen. Eine Richtlinien-Assembly kann Anwendungen auf dem System umleiten, um die neue Assemblyversion zu verwenden. Richtlinienassemblys sollten durch Erstellen einer neuen Komponente bereitgestellt werden.
-   Windows Installationsprogramm 3.0 oder höher ist erforderlich, um Assemblyupdates zu deinstallieren. Weitere Informationen finden Sie unter [Entfernen von Patches.](removing-patches.md)
-   Die neuere Version der Assembly sollte die gleichen oder höhere Versionen von Dateien aus zuvor freigegebenen Assemblys enthalten.
-   Windows Installer 3.0 kann .NET Framework und Win32-Assemblys durch einen vollständigen Dateiersetzungs- oder durch ein kleineres Deltaupdate serviceen. Weitere Informationen finden Sie unter [Reduzieren der Patchgröße.](reducing-patch-size.md)
-   Wenn ihr Update den starken Namen der Assembly ändert, sind die [Tabelle MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) und [die Tabelle MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) erforderlich, wenn das Patchpaket keine [MsiPatchSequence-Tabelle](msipatchsequence-table.md) enthält. Die Tabelle MsiPatchOldAssemblyFile und msiPatchOldAssemblyName sind nicht erforderlich, wenn das Patchpaket Informationen zur Patchsequenzierung in einer MsiPatchSequence-Tabelle enthält.
-   Bevor Sie einen neuen Patch veröffentlichen, testen Sie den Patch, indem Sie ihn mit allen zuvor veröffentlichten Patches anwenden.

## <a name="updating-win32-assemblies"></a>Aktualisieren von Win32-Assemblys

Befolgen Sie beim Aktualisieren von Win32-Assemblys die folgenden Richtlinien:

-   Ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle angegeben ist.](msiassemblyname-table.md)
-   Wenn Ihre Anwendung immer die neue Version der Assembly verwenden soll, ohne die Assemblyversion zu beeinträchtigen, die von anderen Anwendungen im System verwendet wird, verwenden Sie dieselbe Komponente, um die neue Assemblyversion zu enthalten, die Sie für die alte Assemblyversion verwendet haben. Behalten Sie die gleiche ComponentId in der [Tabelle Component](component-table.md) bei. Nachdem ihre Anwendung gepatcht wurde, enthält sie nur einen Verweis auf die neue Version der Assembly. Die alte Version der Assembly kann mit der neuen Version im globalen Assemblycache verbleiben. Dies wirkt sich nicht auf andere Anwendungen auf dem System aus, die die alte Version der Assembly verwenden. Wenn dieselbe Komponente sowohl für die neue als auch für die alte Version der Assembly verwendet wird, kann das Update ein kleinerer Deltapatch sein.
-   Wenn die neue Version der Assembly nicht mit allen Systemen kompatibel ist, auf denen Sie die Anwendung installieren möchten, können Sie die neue und die alte Version der Assembly als nebenseitige Assemblys installieren. Um beide Assemblyversionen nebeneinander zu installieren, erstellen Sie eine neue Komponente, die die neue Assemblyversion enthält. Die ComponentId in der [Component-Tabelle](component-table.md) für die neue Komponente sollte sich von der ComponentId der Komponente mit der alten Version unterscheiden. Nachdem Ihre Anwendung gepatcht wurde, enthält sie Verweise auf beide Assemblyversionen. Anschließend kann die Anwendung über ein Manifest zur kompatiblen Version der Assembly geleitet werden. Wenn für die neue und die alte Version der Assembly unterschiedliche Komponenten verwendet werden, verwendet Ihr Update den vollständigen Dateiersetzungs-.

## <a name="updating-net-framework-assemblies"></a>Aktualisieren .NET Framework Assemblys

Befolgen Sie die folgenden Richtlinien, wenn Sie .NET Framework aktualisieren.

-   Ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle angegeben ist.](msiassemblyname-table.md)
-   Wenn Ihre Anwendung immer die neue Version der Assembly verwenden soll, ohne die Assemblyversion zu beeinträchtigen, die von anderen Anwendungen im System verwendet wird, ändern Sie den starken Namen der neuen Assembly, die in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md)angegeben ist, und verwenden Sie dieselbe Komponente, um die neue Assemblyversion zu enthalten, die Sie für die alte Assemblyversion verwendet haben. Behalten Sie die gleiche ComponentId in der [Tabelle Component](component-table.md) bei. Nachdem ihre Anwendung gepatcht wurde, enthält sie nur einen Verweis auf die neue Version der Assembly. Die alte Version der Assembly kann bei der neuen Version im globalen Cache verbleiben. Dies wirkt sich nicht auf andere Anwendungen auf dem System aus, die die alte Version der Assembly verwenden. Wenn dieselbe Komponente sowohl für die neue als auch für die alte Version der Assembly verwendet wird, kann das Update ein kleinerer Deltapatch sein.
-   Wenn die neue Version der Assembly nicht mit allen Systemen kompatibel ist, auf denen Sie die Anwendung installieren möchten, können Sie die neuen und alten Versionen der Assembly als nebenseitige Assemblys installieren. Um beide Assemblyversionen nebeneinander zu installieren, ändern Sie den starken Namen der neuen Assembly, die in der [Tabelle MsiAssemblyName](msiassemblyname-table.md)angegeben ist, und erstellen Sie eine neue Komponente, die die neue Assemblyversion enthält. Die ComponentId in der [Component-Tabelle](component-table.md) für die neue Komponente sollte sich von der ComponentId der Komponente mit der alten Version unterscheiden. Nachdem Ihre Anwendung gepatcht wurde, enthält sie Verweise auf beide Assemblyversionen. Die Anwendung kann dann von einem Manifest an die kompatible Version der Assembly geleitet werden. Wenn für die neue und die alte Version der Assembly unterschiedliche Komponenten verwendet werden, verwendet Ihr Update den vollständigen Dateiersetzungs-.
-   Ein vorhandenes Update überschreibt die Kopie einer .NET Framework Assembly im globalen Assemblycache. Dieser Typ der Assemblyaktualisierung ändert nicht den starken Namen der Assembly. Nur der Wert im FileVersion-Feld der [Tabelle MsiAssemblyName](msiassemblyname-table.md) wird geändert. Das place-Update einer .NET Framework Assembly erfordert .NET Framework 1.1 SP1 oder höher.
    > [!Note]  
    > Der typspezifische Update überschreibt die Kopie der Assembly im globalen Cache und kann andere Anwendungen unterbricht, wenn die neue Version der Assembly nicht vollständig abwärtskompatibel ist. Die empfohlene Methode zum Aktualisieren einer Assembly ist das Ändern des starken Namens der Assembly in der [MsiAssemblyName-Tabelle](msiassemblyname-table.md).

     

 

 



