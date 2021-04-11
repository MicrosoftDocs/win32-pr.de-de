---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1970c8e9063657701183c91ff337d06d169914fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215707"
---
# <a name="c-windows-installer"></a><span data-ttu-id="fac3e-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="fac3e-103">C (Windows Installer)</span></span>

<span data-ttu-id="fac3e-104">[a](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="fac3e-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="fac3e-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**CAB-Datei**</span><span class="sxs-lookup"><span data-stu-id="fac3e-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-106">Eine einzelne Datei (in der Regel mit der Erweiterung ". cab"), die komprimierte Dateien in einer Datei Bibliothek speichert.</span><span class="sxs-lookup"><span data-stu-id="fac3e-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="fac3e-107">Das CAB-Format stellt eine effiziente Möglichkeit zum Packen mehrerer Dateien dar, da die Komprimierung über Dateigrenzen hinweg erfolgt und das Komprimierungs Verhältnis erheblich verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="fac3e-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="fac3e-108">Weitere Informationen zum Erstellen von Schränken finden Sie unter CAB- [Dateien](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Prüfsumme**</span><span class="sxs-lookup"><span data-stu-id="fac3e-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-110">Berechneter Wert, der vom Inhalt einer Datei abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="fac3e-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="fac3e-111">Sie wird mit Daten gespeichert, um Datei Beschädigungen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="fac3e-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="fac3e-112">Das System überprüft diesen Wert, um sicherzustellen, dass die Daten nicht beschädigt sind.</span><span class="sxs-lookup"><span data-stu-id="fac3e-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Zulieferern**</span><span class="sxs-lookup"><span data-stu-id="fac3e-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-114">Die kleinste Installation, die vom Installationsprogramm verarbeitet wird, auch ein Baustein einer Anwendung oder eines Features aus der Sicht des Programmierers.</span><span class="sxs-lookup"><span data-stu-id="fac3e-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="fac3e-115">Beispiele für Komponenten sind eine Gruppe verwandter Dateien, ein COM-Objekt oder eine Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="fac3e-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="fac3e-116">Weitere Informationen finden Sie unter [Komponenten und Features](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**Commit für Datenbanken**</span><span class="sxs-lookup"><span data-stu-id="fac3e-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-118">Akkumulierte Änderungen, die in einer Datenbank vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="fac3e-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="fac3e-119">Die Änderungen werden erst dann in der tatsächlichen Datenbank wiedergegeben, wenn für die Datenbank ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="fac3e-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="fac3e-120">Weitere Informationen finden Sie unter [Commit für Datenbanken](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**Tabelle ControlEvent besitzt**</span><span class="sxs-lookup"><span data-stu-id="fac3e-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-122">Aspekt der Funktionalität der Benutzeroberfläche des Installers.</span><span class="sxs-lookup"><span data-stu-id="fac3e-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="fac3e-123">Ein typisches ControlEvent löst beim Aktivieren eines Dialogfeld-Steuer Elements oder eines anderen Ereignisses eine Aktion durch das Installationsprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="fac3e-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="fac3e-124">Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Rechnung**</span><span class="sxs-lookup"><span data-stu-id="fac3e-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-126">Methode, die vom Installationsprogramm zum Ermitteln der Speicherplatzanforderungen für die Installation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fac3e-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="fac3e-127">Beim Kostenfaktor werden Faktoren berücksichtigt, z. b. ob vorhandene Dateien überschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fac3e-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="fac3e-128">Weitere Informationen finden Sie unter [Datei Kosten](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**CUB-Datei**</span><span class="sxs-lookup"><span data-stu-id="fac3e-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-130">Validierungs Modul, das den Zugriff auf benutzerdefinierte Ice-Aktionen speichert und ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="fac3e-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="fac3e-131">Weitere Informationen finden Sie unter [Sample. CUB-Datei](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="fac3e-132">Weitere Informationen finden Sie unter [Windows Installer Dateierweiterungen](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="fac3e-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**benutzerdefinierte Aktion**</span><span class="sxs-lookup"><span data-stu-id="fac3e-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="fac3e-134">Wird vom Autor des [*Pakets*](p-gly.md) geschrieben, aber nicht als Standardaktion in das Installationsprogramm integriert.</span><span class="sxs-lookup"><span data-stu-id="fac3e-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="fac3e-135">Weitere Informationen finden Sie unter [benutzerdefinierte Aktionen](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="fac3e-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



