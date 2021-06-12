---
description: Erfahren Sie Windows Installer Konzepte, die mit dem Buchstaben A beginnen, z. B. Barrierefreiheit und Erwerbsphase.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011123"
---
# <a name="a-windows-installer"></a><span data-ttu-id="c75ab-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="c75ab-103">A (Windows Installer)</span></span>

<span data-ttu-id="c75ab-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="c75ab-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c75ab-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Zugänglichkeit**</span><span class="sxs-lookup"><span data-stu-id="c75ab-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-106">Entwurfsimplementierung, um die Benutzeroberfläche des Installationsprogramms für alle Benutzer zugänglich zu machen.</span><span class="sxs-lookup"><span data-stu-id="c75ab-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="c75ab-107">Weitere Informationen zur Barrierefreiheit finden Sie im Übersichtsthema [Barrierefreiheit.](accessibility.md)</span><span class="sxs-lookup"><span data-stu-id="c75ab-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**Erwerbsphase**</span><span class="sxs-lookup"><span data-stu-id="c75ab-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-109">Installationsphase, in der das Installationsprogramm die Prozedur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="c75ab-110">Die Erwerbsphase beginnt, wenn eine [](m-gly.md) Anwendung oder ein Benutzer Windows Installer anweisen, eine Anwendung oder ein Feature zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c75ab-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="c75ab-111">Das Installationsprogramm fragt dann die Datenbank [*nach Informationen ab,*](i-gly.md) während das Ausführungsskript [*für*](e-gly.md) die Installation generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c75ab-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="c75ab-112">Weitere Informationen zu den Phasen einer Installation finden Sie unter [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="c75ab-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Aktion**</span><span class="sxs-lookup"><span data-stu-id="c75ab-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-114">Viele der funktionen, die von Windows Installer werden in Aktionen gekapselt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="c75ab-115">Jede Aktion gibt die Ausführung einer bestimmten Funktion an, und der gesamte prozedurale Ablauf der Installation wird durch die Abfolge von Aktionen in den [*Sequenztabellen vorgegeben.*](s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c75ab-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="c75ab-116">[*Standardaktionen*](s-gly.md) sind in Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c75ab-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="c75ab-117">[*Benutzerdefinierte Aktionen*](c-gly.md) werden vom Autor des Installationspakets [*geschrieben.*](p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c75ab-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Administratorgenehmigungsmodus**</span><span class="sxs-lookup"><span data-stu-id="c75ab-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-119">Der genehmigungsstatus, der durch den Benutzerkontenschutz (User Account Protection, UAC) aktiviert wird, der alle Benutzer mit den geringsten Berechtigungen einschließlich Administratoren ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c75ab-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="c75ab-120">Benutzer müssen ihre Zustimmung zum Erhöhen von Installationen erteilen, für die Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c75ab-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Werbung**</span><span class="sxs-lookup"><span data-stu-id="c75ab-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-122">Möglichkeit, die schnittstellen, die zum Laden erforderlich sind, und eine Anwendung verfügbar zu machen, ohne die Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c75ab-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="c75ab-123">Wenn ein Benutzer oder eine Anwendung eine angekündigte Schnittstelle aktiviert, wird das Installationsprogramm mit der Installation der erforderlichen Komponenten fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="c75ab-124">Die beiden Arten der Werbung sind das [*Zuweisen und*](/windows) [*Veröffentlichen von*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c75ab-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="c75ab-125">Weitere Informationen finden Sie unter [*install-on-demand*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c75ab-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="c75ab-126">Weitere Informationen zur Ankündigung von Anwendungen durch das Installationsprogramm finden Sie unter [Ankündigung](advertisement.md)von .</span><span class="sxs-lookup"><span data-stu-id="c75ab-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (III)**</span><span class="sxs-lookup"><span data-stu-id="c75ab-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-128">Ein Systemdienst von Windows Vista, der das Starten von Installationen erleichtert, für deren Ausführung erhöhte Rechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c75ab-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="c75ab-129">Stellt die Zustimmungsbenutzeroberfläche zur Verfügung, die von der Benutzerkontensteuerung verwendet wird, um einen Benutzer zur Administratorautorisierung aufforderungen.</span><span class="sxs-lookup"><span data-stu-id="c75ab-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Zuweisen**</span><span class="sxs-lookup"><span data-stu-id="c75ab-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-131">Macht eine Anwendung verfügbar und sieht so aus, als wäre sie für einen Benutzer installiert worden, ohne sie tatsächlich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c75ab-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="c75ab-132">Durch zuweisen werden dem Startmenü Verknüpfungen und Symbole hinzufügt, entsprechende Dateien zugeordnet und Registrierungseinträge für die Anwendung schreibt. </span><span class="sxs-lookup"><span data-stu-id="c75ab-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="c75ab-133">Wenn ein Benutzer versucht, eine zugewiesene Anwendung zu öffnen, installiert das Installationsprogramm die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c75ab-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="c75ab-134">Das Zuweisen und [*Veröffentlichen sind*](p-gly.md) zwei Methoden zur [*Werbung*](/windows)von .</span><span class="sxs-lookup"><span data-stu-id="c75ab-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="c75ab-135">Weitere Informationen finden Sie unter [Advertisement](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="c75ab-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c75ab-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchrone Ausführung**</span><span class="sxs-lookup"><span data-stu-id="c75ab-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="c75ab-137">[*Benutzerdefinierte Aktion,*](c-gly.md) bei der das Installationsprogramm separate Threads der benutzerdefinierten Aktion und der aktuellen Installation gleichzeitig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="c75ab-138">Weitere Informationen finden Sie unter [Synchrone und asynchrone benutzerdefinierte Aktionen.](synchronous-and-asynchronous-custom-actions.md)</span><span class="sxs-lookup"><span data-stu-id="c75ab-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
