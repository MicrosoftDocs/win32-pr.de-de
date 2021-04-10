---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131476"
---
# <a name="p-windows-installer"></a><span data-ttu-id="4941c-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="4941c-103">P (Windows Installer)</span></span>

<span data-ttu-id="4941c-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="4941c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4941c-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Paketen**</span><span class="sxs-lookup"><span data-stu-id="4941c-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-106">[*MSI-Datei*](m-gly.md) und alle [*externen Quelldateien*](e-gly.md) , auf die von dieser Datei verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4941c-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="4941c-107">Ein Paket enthält daher alle Informationen, die die Windows Installer benötigt, um die Benutzeroberfläche auszuführen und die Anwendung zu installieren oder zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="4941c-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="4941c-108">Weitere Informationen finden Sie auch unter [*Installer Database*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**Paketcode**</span><span class="sxs-lookup"><span data-stu-id="4941c-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-110">GUID, die ein bestimmtes Paket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4941c-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="4941c-111">Ein eindeutiger Paketcode ist erforderlich, da einige Transformationen oder Patchpakete auf mehr als eine Anwendung angewendet werden können oder eine Anwendung auf eine andere Anwendung oder Version aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="4941c-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="4941c-112">Weitere Informationen finden Sie unter [Paket Codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Patchen**</span><span class="sxs-lookup"><span data-stu-id="4941c-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-114">Methode zum Aktualisieren einer Datei, die nur die geänderten Bits ersetzt, nicht die gesamte Datei.</span><span class="sxs-lookup"><span data-stu-id="4941c-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="4941c-115">Dies bedeutet, dass Benutzer einen Upgradepatch für ein Produkt herunterladen können, das wesentlich kleiner als das gesamte Produkt ist.</span><span class="sxs-lookup"><span data-stu-id="4941c-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="4941c-116">Weitere Informationen finden Sie unter [Patch-Pakete](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**Patchdatei**</span><span class="sxs-lookup"><span data-stu-id="4941c-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-118">Zum Patchen verwendetes [Patch-Paket](patch-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="4941c-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="4941c-119">Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**Vorschaumodus**</span><span class="sxs-lookup"><span data-stu-id="4941c-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-121">Der Modus zum Anzeigen des Entwurfs der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="4941c-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="4941c-122">Weitere Informationen finden Sie unter [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**Statusanzeige**</span><span class="sxs-lookup"><span data-stu-id="4941c-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-124">Steuerung: das Installationsprogramm kann während der Skript Ausführungszeit angezeigt werden, die den Fortschritt der Installation darstellt.</span><span class="sxs-lookup"><span data-stu-id="4941c-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="4941c-125">Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="4941c-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="4941c-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Property**</span><span class="sxs-lookup"><span data-stu-id="4941c-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-127">Globale Variablen, die während einer-Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4941c-127">Global variables used during an installation.</span></span> <span data-ttu-id="4941c-128">(Siehe [Informationen zu Eigenschaften](about-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="4941c-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="4941c-129">Der Begriff "Property" bezieht sich auch auf ein Attribut eines Automatisierungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="4941c-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="4941c-130">(Siehe [Automation Interface](automation-interface.md).)</span><span class="sxs-lookup"><span data-stu-id="4941c-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="4941c-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**liche**</span><span class="sxs-lookup"><span data-stu-id="4941c-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="4941c-132">Methode zum [*ankündigen eines Features oder einer Anwendung*](a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4941c-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="4941c-133">Bei der Veröffentlichung wird die Benutzeroberfläche nicht aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="4941c-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="4941c-134">Wenn jedoch eine andere Anwendung versucht, eine veröffentlichte Anwendung zu öffnen, sind genügend Informationen vorhanden, damit das Installationsprogramm die veröffentlichte Anwendung zuweisen kann.</span><span class="sxs-lookup"><span data-stu-id="4941c-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="4941c-135">Weitere Informationen finden Sie unter [*zuweisen*](a-gly.md) von-und- [Komponenten und-Funktionen](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="4941c-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



