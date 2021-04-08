---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866307"
---
# <a name="i-windows-installer"></a><span data-ttu-id="09557-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="09557-103">I (Windows Installer)</span></span>

<span data-ttu-id="09557-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="09557-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="09557-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**IDT-Datei**</span><span class="sxs-lookup"><span data-stu-id="09557-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="09557-106">Datenbanktabelle des exportierten Installers.</span><span class="sxs-lookup"><span data-stu-id="09557-106">Exported installer database table.</span></span> <span data-ttu-id="09557-107">Weitere Informationen finden Sie unter [importieren und exportieren](importing-and-exporting.md) und [Windows Installer Dateierweiterungen](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="09557-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importieren der Adress Tabelle (IAT)**</span><span class="sxs-lookup"><span data-stu-id="09557-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="09557-109">Dabei wird die berechnete virtuelle Adresse aus jeder aus allen DLLs importierten Funktion gespeichert.</span><span class="sxs-lookup"><span data-stu-id="09557-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="09557-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interne Benutzeroberfläche**</span><span class="sxs-lookup"><span data-stu-id="09557-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="09557-111">Integrierte Funktionen des Installers, mit denen eine grafische Benutzeroberfläche für die Installation erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="09557-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="09557-112">Ein Autor kann eine [*externe Benutzeroberfläche*](e-gly.md)auswählen.</span><span class="sxs-lookup"><span data-stu-id="09557-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="09557-113">Weitere Informationen finden Sie unter Informationen zur [Benutzeroberfläche](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="09557-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**Installationsstufe**</span><span class="sxs-lookup"><span data-stu-id="09557-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="09557-115">Der angegebene Installations Wert.</span><span class="sxs-lookup"><span data-stu-id="09557-115">Specified installation value.</span></span> <span data-ttu-id="09557-116">Eine Anwendung wird nur installiert, wenn die eigene Ebene kleiner oder gleich der Installations Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="09557-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="09557-117">Der Satz von Anwendungen, der für die Installation ausgewählt wurde, kann daher durch Ändern der Installations Ebene geändert werden.</span><span class="sxs-lookup"><span data-stu-id="09557-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="09557-118">Weitere Informationen finden Sie unter [Funktions Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="09557-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**Installation bei Bedarf**</span><span class="sxs-lookup"><span data-stu-id="09557-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="09557-120">Dienst, mit dem Anwendungen oder Features installiert werden, die vom Benutzer oder von einer anderen Anwendung angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="09557-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="09557-121">Durch die [*Werbung*](a-gly.md) wird ein Feature oder eine Anwendung für die Installation bei Bedarf bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="09557-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="09557-122">Weitere Informationen finden Sie unter: [Installation nach Bedarf](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="09557-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**Installations Kontext**</span><span class="sxs-lookup"><span data-stu-id="09557-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="09557-124">Die Kombination von Installations rechten und Installationstypen erzeugt drei verschiedene Installations Kontexte: Benutzer, die nicht verwaltet werden, pro Benutzer verwaltet und pro Computer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="09557-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="09557-125">Es gibt keinen Computer, der nicht verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="09557-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="09557-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**ations**</span><span class="sxs-lookup"><span data-stu-id="09557-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="09557-127">Der [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="09557-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**Installer-Datenbank**</span><span class="sxs-lookup"><span data-stu-id="09557-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="09557-129">Eine relationale Datenbank, die Setup Anweisungen für eine-Installation enthält.</span><span class="sxs-lookup"><span data-stu-id="09557-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="09557-130">Die Installer-Datenbank wird in der [*MSI-Datei*](m-gly.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="09557-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="09557-131">Weitere Informationen finden Sie unter [Installer Database](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="09557-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**Installer-Funktion**</span><span class="sxs-lookup"><span data-stu-id="09557-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="09557-133">Wird von einem Benutzer oder einer Anwendung aufgerufen, um Installer-Dienste und-Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="09557-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="09557-134">Dies ist die Anwendungsprogrammierschnittstelle des Installers.</span><span class="sxs-lookup"><span data-stu-id="09557-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="09557-135">Weitere Informationen finden Sie unter [installationsfunktionsreferenz](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="09557-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="09557-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**Installer-Paket Erstellungs Tool**</span><span class="sxs-lookup"><span data-stu-id="09557-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="09557-137">Software, die es Entwicklern ermöglicht, eine MSI- [*Datei*](m-gly.md)zu erstellen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="09557-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="09557-138">Dies umfasst zusammen mit [*externen Quelldateien*](e-gly.md) ein [*Paket*](p-gly.md) , das alle für eine Installation erforderlichen Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="09557-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="09557-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**interne Quelldateien**</span><span class="sxs-lookup"><span data-stu-id="09557-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="09557-140">In der [*MSI-Datei*](m-gly.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="09557-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="09557-141">Mehrere interne Quelldateien können komprimiert und zusammen in einer CAB- [*Datei*](c-gly.md) gespeichert werden, die in einer MSI-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="09557-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



