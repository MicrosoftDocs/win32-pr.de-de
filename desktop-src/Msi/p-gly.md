---
description: Erfahren Sie mehr über Windows Installer Konzepte, die mit dem Buchstaben P beginnen, z. B. Paketcode und Patchen.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011102"
---
# <a name="p-windows-installer"></a><span data-ttu-id="80778-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="80778-103">P (Windows Installer)</span></span>

<span data-ttu-id="80778-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="80778-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="80778-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Paket**</span><span class="sxs-lookup"><span data-stu-id="80778-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="80778-106">[*.msi Datei*](m-gly.md) und alle [*externen Quelldateien,*](e-gly.md) auf die von dieser Datei verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="80778-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="80778-107">Ein Paket enthält daher alle Informationen, die der Windows Installer benötigt, um die Benutzeroberfläche auszuführen und die Anwendung zu installieren oder zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="80778-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="80778-108">Weitere Informationen finden Sie auch unter [*Installationsprogrammdatenbank*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="80778-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**Paketcode**</span><span class="sxs-lookup"><span data-stu-id="80778-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="80778-110">GUID, die ein bestimmtes Paket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="80778-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="80778-111">Ein eindeutiger Paketcode ist erforderlich, da einige Transformationen oder Patchpakete auf mehrere Anwendungen angewendet werden können oder eine Anwendung auf eine andere Anwendung oder Version aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="80778-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="80778-112">Weitere Informationen finden Sie unter [Paketcodes.](package-codes.md)</span><span class="sxs-lookup"><span data-stu-id="80778-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Patchen**</span><span class="sxs-lookup"><span data-stu-id="80778-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="80778-114">Methode zum Aktualisieren einer Datei, die nur die geänderten Bits anstelle der gesamten Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="80778-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="80778-115">Dies bedeutet, dass Benutzer einen Upgradepatch für ein Produkt herunterladen können, das viel kleiner als das gesamte Produkt ist.</span><span class="sxs-lookup"><span data-stu-id="80778-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="80778-116">Weitere Informationen finden Sie unter [Patchpakete.](patch-packages.md)</span><span class="sxs-lookup"><span data-stu-id="80778-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**Patchdatei**</span><span class="sxs-lookup"><span data-stu-id="80778-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="80778-118">P [atch-Paket, das](patch-packages.md) zum Patchen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="80778-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="80778-119">Weitere Informationen finden Sie unter [Patchen und Upgrades.](patching-and-upgrades.md)</span><span class="sxs-lookup"><span data-stu-id="80778-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**Vorschaumodus**</span><span class="sxs-lookup"><span data-stu-id="80778-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="80778-121">Modus zum Anzeigen des Entwurfs der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="80778-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="80778-122">Weitere Informationen finden Sie unter [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="80778-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**Statusanzeige**</span><span class="sxs-lookup"><span data-stu-id="80778-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="80778-124">Steuern Sie, ob das Installationsprogramm während der Skriptausführungszeit angezeigt werden kann, die den Fortschritt der Installation darstellt.</span><span class="sxs-lookup"><span data-stu-id="80778-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="80778-125">Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuerelements.](authoring-a-progressbar-control.md)</span><span class="sxs-lookup"><span data-stu-id="80778-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="80778-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="80778-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="80778-127">Globale Variablen, die während einer Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80778-127">Global variables used during an installation.</span></span> <span data-ttu-id="80778-128">(Siehe [Informationen zu Eigenschaften](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="80778-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="80778-129">Der Begriff "Eigenschaft" bezieht sich auch auf ein Attribut eines Automatisierungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="80778-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="80778-130">(Weitere Informationen finden Sie unter [Automation Interface](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="80778-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="80778-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Publishing**</span><span class="sxs-lookup"><span data-stu-id="80778-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="80778-132">Methode zum [*Anwerben*](a-gly.md) eines Features oder einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="80778-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="80778-133">Bei der Veröffentlichung wird die Benutzeroberfläche nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="80778-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="80778-134">Wenn jedoch eine andere Anwendung versucht, eine veröffentlichte Anwendung zu öffnen, sind genügend Informationen vorhanden, damit das Installationsprogramm die veröffentlichte Anwendung zuweisen kann.</span><span class="sxs-lookup"><span data-stu-id="80778-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="80778-135">Weitere Informationen finden Sie unter [*Assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="80778-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



