---
description: Erfahren Sie mehr über Windows Installer Konzepte, die mit dem Buchstaben C beginnen, z. B. Schränkdatei und Prüfsumme.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010923"
---
# <a name="c-windows-installer"></a><span data-ttu-id="95535-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="95535-103">C (Windows Installer)</span></span>

<span data-ttu-id="95535-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="95535-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="95535-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**Cab-Datei**</span><span class="sxs-lookup"><span data-stu-id="95535-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="95535-106">Eine einzelne Datei, in der Regel mit einer .cab Erweiterung, die komprimierte Dateien in einer Dateibibliothek speichert.</span><span class="sxs-lookup"><span data-stu-id="95535-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="95535-107">Das Cab-Format ist eine effiziente Möglichkeit zum Packen mehrerer Dateien, da die Komprimierung über Dateigrenzen hinweg durchgeführt wird, was das Komprimierungsverhältnis erheblich verbessert.</span><span class="sxs-lookup"><span data-stu-id="95535-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="95535-108">Informationen zum Erstellen von Schränken finden Sie unter [Cabinet Files](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="95535-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Prüfsumme**</span><span class="sxs-lookup"><span data-stu-id="95535-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="95535-110">Berechneter Wert, der vom Inhalt einer Datei abhängt.</span><span class="sxs-lookup"><span data-stu-id="95535-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="95535-111">Sie wird mit Daten gespeichert, um Dateibeschädigungen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="95535-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="95535-112">Das System überprüft diesen Wert, um sicherzustellen, dass die Daten nicht korruptiert sind.</span><span class="sxs-lookup"><span data-stu-id="95535-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="95535-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Komponente**</span><span class="sxs-lookup"><span data-stu-id="95535-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="95535-114">Der kleinste Teil einer Installation, die vom Installationsprogramm verarbeitet wird, auch ein Baustein einer Anwendung oder eines Features aus der Perspektive des Programmierers.</span><span class="sxs-lookup"><span data-stu-id="95535-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="95535-115">Beispiele für Komponenten sind eine Gruppe verwandter Dateien, ein COM-Objekt oder eine Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="95535-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="95535-116">Weitere Informationen finden Sie unter [Komponenten und Features.](components-and-features.md)</span><span class="sxs-lookup"><span data-stu-id="95535-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**Committen von Datenbanken**</span><span class="sxs-lookup"><span data-stu-id="95535-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="95535-118">Kumulierte Änderungen, die in einer Datenbank vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="95535-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="95535-119">Die Änderungen werden erst in der tatsächlichen Datenbank widergespiegelt, wenn ein Commit für die Datenbank ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="95535-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="95535-120">Weitere Informationen finden Sie unter [Committen von Datenbanken.](committing-databases.md)</span><span class="sxs-lookup"><span data-stu-id="95535-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span><span class="sxs-lookup"><span data-stu-id="95535-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="95535-122">Aspekt der Funktionalität der Benutzeroberfläche des Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="95535-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="95535-123">Ein typisches ControlEvent löst beim Aktivieren eines Dialogfeldsteuerelements oder eines anderen Ereignisses eine Aktion durch das Installationsprogramm aus.</span><span class="sxs-lookup"><span data-stu-id="95535-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="95535-124">Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95535-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Kostet**</span><span class="sxs-lookup"><span data-stu-id="95535-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="95535-126">Methode, die vom Installationsprogramm verwendet wird, um die Speicherplatzanforderungen für die Installation zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="95535-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="95535-127">Bei der Kostenkalkulation werden Faktoren berücksichtigt, z. B. ob vorhandene Dateien überschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="95535-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="95535-128">Weitere Informationen finden Sie unter [Dateikosten.](file-costing.md)</span><span class="sxs-lookup"><span data-stu-id="95535-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**CUB-Datei**</span><span class="sxs-lookup"><span data-stu-id="95535-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="95535-130">Validierungsmodul, das benutzerdefinierte ICE-Aktionen speichert und Zugriff darauf bietet.</span><span class="sxs-lookup"><span data-stu-id="95535-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="95535-131">Weitere Informationen finden Sie unter [CUB-Beispieldatei.](sample--cub-file.md)</span><span class="sxs-lookup"><span data-stu-id="95535-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="95535-132">Weitere Informationen finden Sie auch [unter Windows Installer Dateierweiterungen](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="95535-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="95535-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**Benutzerdefinierte Aktion**</span><span class="sxs-lookup"><span data-stu-id="95535-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="95535-134">Wird vom Autor des [*Pakets*](p-gly.md) geschrieben, aber nicht als Standardaktion in das Installationsprogramm integriert.</span><span class="sxs-lookup"><span data-stu-id="95535-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="95535-135">Weitere Informationen finden Sie unter [Benutzerdefinierte Aktionen.](custom-actions.md)</span><span class="sxs-lookup"><span data-stu-id="95535-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



