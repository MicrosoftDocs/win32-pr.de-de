---
description: ICEM13 überprüft, ob das Mergemodul keine Herausgeber Richtlinie und keine konfigurationsassemblys enthält.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864404"
---
# <a name="icem13"></a><span data-ttu-id="dfc31-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="dfc31-103">ICEM13</span></span>

<span data-ttu-id="dfc31-104">ICEM13 überprüft, ob das Mergemodul keine Herausgeber Richtlinie und keine konfigurationsassemblys enthält.</span><span class="sxs-lookup"><span data-stu-id="dfc31-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="dfc31-105">Herausgeber Richtlinien und konfigurationsassemblys sollten nicht in Mergemodulen enthalten sein, die für die Weiterverteilung vorgesehen sind, da dies Auswirkungen auf andere Anwendungen auf dem Computer</span><span class="sxs-lookup"><span data-stu-id="dfc31-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="dfc31-106">Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc31-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="dfc31-107">Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="dfc31-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="dfc31-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="dfc31-108">Result</span></span>

<span data-ttu-id="dfc31-109">ICEM13 gibt eine Warnmeldung aus, wenn Sie eine im Komponenten Feld der [MsiAssembly-Tabelle](msiassembly-table.md) des Mergemoduls angegebene Komponente findet, bei der es sich um eine Herausgeber Richtlinie oder eine Konfigurationsassembly handelt.</span><span class="sxs-lookup"><span data-stu-id="dfc31-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="dfc31-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dfc31-110">Example</span></span>

<span data-ttu-id="dfc31-111">ICEM13 gibt die folgende Warnmeldung aus, wenn eine Zeile in der [MsiAssembly-Tabelle](msiassembly-table.md) gefunden wird, in der die Komponente " \[ 1 \] " im Komponenten Feld angegeben ist, bei der es sich um eine Herausgeber Richtlinie oder eine Konfigurationsassembly handelt, die im Mergemodul enthalten ist</span><span class="sxs-lookup"><span data-stu-id="dfc31-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="dfc31-112">Es ist möglich, Herausgeber Richtlinien und konfigurationsassemblys mithilfe der Windows Installer zu installieren. es wird jedoch nicht empfohlen, diese Assemblys in Mergemodulen neu zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="dfc31-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfc31-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfc31-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfc31-114">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="dfc31-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



