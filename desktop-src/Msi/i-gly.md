---
description: Erfahren Sie Windows Installer Konzepte, die mit dem Buchstaben I beginnen, z. B. Die Tabelle "Adresse importieren" und die Installationsebene.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010653"
---
# <a name="i-windows-installer"></a><span data-ttu-id="c9a70-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="c9a70-103">I (Windows Installer)</span></span>

<span data-ttu-id="c9a70-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](f-gly.md) [](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="c9a70-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c9a70-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**IDT-Datei**</span><span class="sxs-lookup"><span data-stu-id="c9a70-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-106">Exportierte Installer-Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="c9a70-106">Exported installer database table.</span></span> <span data-ttu-id="c9a70-107">Weitere Informationen finden Sie unter [Importieren und Exportieren Windows Installer](importing-and-exporting.md) [Dateierweiterungen](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importieren der Adresstabelle (IAT)**</span><span class="sxs-lookup"><span data-stu-id="c9a70-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-109">Hier wird die berechnete virtuelle Adresse aus jeder Funktion gespeichert, die aus allen DLLs importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9a70-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**Interne Benutzeroberfläche**</span><span class="sxs-lookup"><span data-stu-id="c9a70-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-111">Integrierte Funktionen des Installationsprogramms, die zum Erstellen einer grafischen Benutzeroberfläche für die Installation verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c9a70-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="c9a70-112">Ein Autor kann eine externe [*Benutzeroberfläche auswählen.*](e-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c9a70-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="c9a70-113">Weitere Informationen finden Sie unter [Informationen zum Benutzeroberfläche](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**Installationsebene**</span><span class="sxs-lookup"><span data-stu-id="c9a70-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-115">Angegebener Installationswert.</span><span class="sxs-lookup"><span data-stu-id="c9a70-115">Specified installation value.</span></span> <span data-ttu-id="c9a70-116">Eine Anwendung wird nur installiert, wenn ihre eigene Ebene kleiner oder gleich der Installationsebene ist.</span><span class="sxs-lookup"><span data-stu-id="c9a70-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="c9a70-117">Der für die Installation ausgewählte Satz von Anwendungen kann daher durch Ändern der Installationsebene geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c9a70-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="c9a70-118">Weitere Informationen finden Sie unter [FeatureTabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**Installation bei Bedarf**</span><span class="sxs-lookup"><span data-stu-id="c9a70-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-120">Dienst, der Anwendungen oder Features wie vom Benutzer oder einer anderen Anwendung angefordert installiert.</span><span class="sxs-lookup"><span data-stu-id="c9a70-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="c9a70-121">[*Die*](a-gly.md) Werbung macht ein Feature oder eine Anwendung für die Installation bei Bedarf verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9a70-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="c9a70-122">Weitere Informationen finden Sie unter Installation [on Demand](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**Installationskontext**</span><span class="sxs-lookup"><span data-stu-id="c9a70-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-124">Die Kombination aus Installationsrechten und Installationstypen erzeugt drei verschiedene Installationskontexte: nicht verwaltet pro Benutzer, benutzer- und computerver verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c9a70-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="c9a70-125">Es gibt keine Computer, die nicht verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c9a70-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Installer**</span><span class="sxs-lookup"><span data-stu-id="c9a70-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-127">Der [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**Installer-Datenbank**</span><span class="sxs-lookup"><span data-stu-id="c9a70-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-129">Relationale Datenbank mit Setupanweisungen für eine Installation.</span><span class="sxs-lookup"><span data-stu-id="c9a70-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="c9a70-130">Die Installer-Datenbank wird in der.msi [*gespeichert.*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c9a70-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="c9a70-131">Weitere Informationen finden Sie unter [Installer Database](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="c9a70-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**Installer-Funktion**</span><span class="sxs-lookup"><span data-stu-id="c9a70-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-133">Wird von einem Benutzer oder einer Anwendung aufgerufen, um Installationsdienste und -funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9a70-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="c9a70-134">Dies ist die Anwendungsprogrammierschnittstelle des Installationsprogramms.</span><span class="sxs-lookup"><span data-stu-id="c9a70-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="c9a70-135">Weitere Informationen finden Sie unter [Installer Function Reference (Referenz zur Installerfunktion).](installer-function-reference.md)</span><span class="sxs-lookup"><span data-stu-id="c9a70-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**Installer-Paketerstellungstool**</span><span class="sxs-lookup"><span data-stu-id="c9a70-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-137">Software, die einem Entwickler das Erstellen und Bearbeiten einer.msi [*ermöglicht.*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c9a70-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="c9a70-138">Dies umfasst zusammen [*mit allen externen Quelldateien*](e-gly.md) ein [*Paket,*](p-gly.md) das alle informationen enthält, die für eine Installation erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c9a70-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="c9a70-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**Interne Quelldateien**</span><span class="sxs-lookup"><span data-stu-id="c9a70-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="c9a70-140">Wird in der.msi [*gespeichert.*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c9a70-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="c9a70-141">Mehrere interne Quelldateien können komprimiert und zusammen in einer [*Schränkdatei*](c-gly.md) gespeichert werden, die in einer .msi ist.</span><span class="sxs-lookup"><span data-stu-id="c9a70-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



