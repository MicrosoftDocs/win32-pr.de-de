---
description: Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der Patch-Eigenschaft installiert wird.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Patchen von erst Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960829"
---
# <a name="patching-initial-installations"></a><span data-ttu-id="87894-103">Patchen von erst Installationen</span><span class="sxs-lookup"><span data-stu-id="87894-103">Patching Initial Installations</span></span>

<span data-ttu-id="87894-104">Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der [**Patch**](patch.md) -Eigenschaft installiert wird.</span><span class="sxs-lookup"><span data-stu-id="87894-104">A Windows Installer Patch (MSP) can be applied when installing an application for the first time by using the [**PATCH**](patch.md) property.</span></span>

<span data-ttu-id="87894-105">Zum Anwenden eines Patches bei der erstmaligen Installation der Anwendung muss die [**Patch**](patch.md) -Eigenschaft in der Befehlszeile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87894-105">To apply a patch the first time the application is installed, the [**PATCH**](patch.md) property must be set on the command line.</span></span> <span data-ttu-id="87894-106">Geben Sie den vollständigen Pfad zum Patch in der Befehlszeile als "Patch = {*path to Patch*}"-Eigenschaft/Wert-Paar an.</span><span class="sxs-lookup"><span data-stu-id="87894-106">Specify the full path to the patch on the command line as the "PATCH={*path to patch*}" property-value pair.</span></span>

<span data-ttu-id="87894-107">Beachten Sie, dass das Angeben der [**Patch**](patch.md) -Eigenschaft in der Befehlszeile die bei der Verwendung von [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder der/p- [Befehlszeilen Option](command-line-options.md)ausgeführten Patch-anwendbarkeits Prüfungen überschreibt.</span><span class="sxs-lookup"><span data-stu-id="87894-107">Note that specifying the [**PATCH**](patch.md) property on the command line overrides the patch applicability checks performed when using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md).</span></span>

<span data-ttu-id="87894-108">Wenn ein Patch mithilfe von " [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) " oder der [Befehlszeilen Option](command-line-options.md)"/p" angewendet wird, vergleicht das Installationsprogramm die aktuell auf dem Computer installierten Anwendungen mit der Liste der Produktcodes, die für den Empfang des Patches in der [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="87894-108">If a patch is applied using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the /p [Command Line Option](command-line-options.md), the installer compares the applications currently installed on the computer to the list of product codes eligible to receive the patch in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="87894-109">Wenn Sie die Eigenschaft [**Patch**](patch.md) in der Befehlszeile für die Installation bei der ersten Installation festlegen, werden die Anwendungen, die zum Empfangen des Patches berechtigt sind, durch Überprüfungs Bedingungen für die in das Patchpaket eingebetteten Transformationen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="87894-109">When you set the [**PATCH**](patch.md) property on the command line to install on first installation, the applications eligible to receive the patch is determined by validation conditions on the transforms embedded in the patch package.</span></span> <span data-ttu-id="87894-110">Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung eines patcherstellungs Tools wie [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="87894-110">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and [PATCHWIZ.DLL](patchwiz-dll.md).</span></span> <span data-ttu-id="87894-111">Die Überprüfungs Bedingungen für Transformationen im Patch stammen aus der Spalte "productvalidateflags" in der Tabelle " [TargetImages](targetimages-table-patchwiz-dll-.md) " der patcherstellungs-Eigenschaften Datei (. PCP).</span><span class="sxs-lookup"><span data-stu-id="87894-111">The validation conditions on transforms in the patch originate from the ProductValidateFlags column in the [TargetImages](targetimages-table-patchwiz-dll-.md) table of the Patch Creation Properties (.pcp) file.</span></span>

<span data-ttu-id="87894-112">Der Patch kann angewendet werden, wenn die Anwendung zum ersten Mal von einer Befehlszeile, einer anderen Anwendung oder einem Skript installiert wird.</span><span class="sxs-lookup"><span data-stu-id="87894-112">The patch can be applied the first time the application is installed by a command line, another application, or script.</span></span>

<span data-ttu-id="87894-113">Im folgenden wird das erste Patchen von der Befehlszeile gezeigt.</span><span class="sxs-lookup"><span data-stu-id="87894-113">The following shows first-time patching from the command line.</span></span>

<span data-ttu-id="87894-114">**msiexec/I** *package.msi* **Patch =**_"c: \\ Directory \\ Patch. msp"_</span><span class="sxs-lookup"><span data-stu-id="87894-114">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp"_</span></span>

<span data-ttu-id="87894-115">Das folgende Beispiel zeigt das erste Patchen aus einer anderen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="87894-115">The following shows first-time patching from another application.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

<span data-ttu-id="87894-116">Das folgende Beispiel zeigt das erste Patchen aus dem Skript.</span><span class="sxs-lookup"><span data-stu-id="87894-116">The following shows first-time patching from script.</span></span>


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



<span data-ttu-id="87894-117">\* \* Windows Installer 3,0 und höher: \* \*</span><span class="sxs-lookup"><span data-stu-id="87894-117">\*\*Windows Installer 3.0 and later:  \*\*</span></span>

<span data-ttu-id="87894-118">Ab Windows Installer Version 3,0 können bei der erstmaligen Installation einer Anwendung mehrere Patches angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="87894-118">Beginning with Windows Installer version 3.0, multiple patches can be applied when installing an application for the first time.</span></span> <span data-ttu-id="87894-119">Legen Sie die Eigenschaft [**Patch**](patch.md) auf eine durch Semikolons getrennte Liste der vollständigen Pfade der Patches fest.</span><span class="sxs-lookup"><span data-stu-id="87894-119">Set the [**PATCH**](patch.md) property to a semicolon delimited list of the patches' full paths.</span></span> <span data-ttu-id="87894-120">Das folgende Beispiel zeigt das erste Patchen mehrerer Patches von der Befehlszeile aus.</span><span class="sxs-lookup"><span data-stu-id="87894-120">The following shows first-time patching of multiple patches from the command line.</span></span>

<span data-ttu-id="87894-121">**msiexec/I** *package.msi* **Patch =**_"c: \\ Directory \\ Patch. msp; c: \\ Directory \\ Patch2. msp; c: \\ Directory \\ Patch3. msp"_</span><span class="sxs-lookup"><span data-stu-id="87894-121">**msiexec /I** *package.msi* **PATCH=**_"c:\\directory\\patch.msp;c:\\directory\\patch2.msp;c:\\directory\\patch3.msp"_</span></span>

 

 



