---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131513"
---
# <a name="a-windows-installer"></a><span data-ttu-id="4411a-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="4411a-103">A (Windows Installer)</span></span>

<span data-ttu-id="4411a-104">a [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="4411a-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4411a-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**Barrierefreiheit**</span><span class="sxs-lookup"><span data-stu-id="4411a-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-106">Entwurfs Implementierung, damit alle Benutzer auf die Benutzeroberfläche des Installers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="4411a-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="4411a-107">Weitere Informationen zur Barrierefreiheit finden Sie im Übersichts Thema: [Barrierefreiheit](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="4411a-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="4411a-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**Erwerbsphase**</span><span class="sxs-lookup"><span data-stu-id="4411a-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-109">Phase der Installation, in der das Installationsprogramm die Prozedur bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4411a-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="4411a-110">Die Erwerbsphase beginnt, wenn eine Anwendung oder ein Benutzer [*Windows Installer*](m-gly.md) anweist, eine Anwendung oder ein Feature zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4411a-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="4411a-111">Der Installer fragt dann die [*Datenbank*](i-gly.md) nach Informationen ab, wenn das [*Ausführungs Skript*](e-gly.md) für die Installation generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4411a-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="4411a-112">Weitere Informationen zu den Phasen einer-Installation finden Sie unter [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="4411a-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="4411a-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**Hinspiel**</span><span class="sxs-lookup"><span data-stu-id="4411a-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-114">Viele der Funktionen, die von Windows Installer ausgeführt werden, werden in Aktionen gekapselt.</span><span class="sxs-lookup"><span data-stu-id="4411a-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="4411a-115">Jede Aktion gibt die Ausführung einer bestimmten Funktion an, und der gesamte prozedurale Ablauf der Installation wird durch die Abfolge der Aktionen in den [*Sequenz Tabellen*](s-gly.md)vorgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="4411a-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="4411a-116">[*Standard Aktionen*](s-gly.md) werden in Windows Installer integriert.</span><span class="sxs-lookup"><span data-stu-id="4411a-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="4411a-117">[*Benutzerdefinierte Aktionen*](c-gly.md) werden vom Autor des Installations [*Pakets*](p-gly.md)geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4411a-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="4411a-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Administrator Genehmigungs Modus**</span><span class="sxs-lookup"><span data-stu-id="4411a-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-119">Der durch den Benutzerkonten Schutz (User Account Protection, UAC) aktivierte Genehmigungs Zustand, der alle Benutzer mit geringsten Rechten (einschließlich Administratoren) ausführt.</span><span class="sxs-lookup"><span data-stu-id="4411a-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="4411a-120">Benutzer müssen Ihre Zustimmung erteilen, um Installationen zu erhöhen, für die Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4411a-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="4411a-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**Lip**</span><span class="sxs-lookup"><span data-stu-id="4411a-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-122">Die Möglichkeit, die zum Laden von erforderlichen Schnittstellen zu erstellen und eine Anwendung verfügbar zu machen, ohne die Anwendung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4411a-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="4411a-123">Wenn ein Benutzer oder eine Anwendung eine angekündigte Oberfläche aktiviert, fährt der Installer mit der Installation der erforderlichen Komponenten fort.</span><span class="sxs-lookup"><span data-stu-id="4411a-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="4411a-124">Die beiden Arten der Werbung sind das [*zuweisen*](/windows) und [*veröffentlichen*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4411a-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="4411a-125">Weitere Informationen finden Sie unter auch [*bei Bedarf installieren*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4411a-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="4411a-126">Weitere Informationen darüber, wie das Installationsprogramm Anwendungen angekündigt [, finden Sie](advertisement.md)unter Ankündigung.</span><span class="sxs-lookup"><span data-stu-id="4411a-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4411a-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Anwendungs Informationsdienst (AIS)**</span><span class="sxs-lookup"><span data-stu-id="4411a-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-128">Ein Systemdienst von Windows Vista, der das Starten von Installationen ermöglicht, für die erhöhte Rechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4411a-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="4411a-129">Stellt die Zustimmungs Benutzeroberfläche bereit, die von der Benutzerkontensteuerung verwendet wird, um einen Benutzer zur Administrator Autorisierung aufzufordern</span><span class="sxs-lookup"><span data-stu-id="4411a-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="4411a-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**Musters**</span><span class="sxs-lookup"><span data-stu-id="4411a-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-131">Stellt eine Anwendung zur Verfügung und macht Sie so angezeigt, als wäre sie für einen Benutzer installiert, ohne Sie tatsächlich zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4411a-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="4411a-132">Beim zuweisen werden dem **Startmenü** Verknüpfungen und Symbole hinzugefügt, die entsprechenden Dateien zugeordnet und Registrierungseinträge für die Anwendung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4411a-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="4411a-133">Wenn ein Benutzer versucht, eine zugewiesene Anwendung zu öffnen, installiert das Installationsprogramm die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4411a-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="4411a-134">Das zuweisen und [*veröffentlichen*](p-gly.md) sind zwei Methoden zur [*Werbung*](/windows).</span><span class="sxs-lookup"><span data-stu-id="4411a-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="4411a-135">Weitere Informationen finden Sie unter [Ankündigung.](advertisement.md)</span><span class="sxs-lookup"><span data-stu-id="4411a-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4411a-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchrone Ausführung**</span><span class="sxs-lookup"><span data-stu-id="4411a-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="4411a-137">[*Benutzerdefinierte Aktion*](c-gly.md) , bei der das Installationsprogramm separate Threads der benutzerdefinierten Aktion und der aktuellen Installation gleichzeitig ausführt.</span><span class="sxs-lookup"><span data-stu-id="4411a-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="4411a-138">Weitere Informationen finden Sie unter [synchrone und asynchrone benutzerdefinierte Aktionen](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4411a-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
