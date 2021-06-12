---
description: Erfahren Sie Windows Installer Konzepte, die mit dem Buchstaben E beginnen, z. B. mit erhöhten Rechten und einer externen Quelldatei.
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: E (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011094"
---
# <a name="e-windows-installer"></a><span data-ttu-id="54106-103">E (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="54106-103">E (Windows Installer)</span></span>

<span data-ttu-id="54106-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="54106-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="54106-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**Erhöhten**</span><span class="sxs-lookup"><span data-stu-id="54106-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="54106-106">Aktionen, die mit Systemberechtigungen ausgeführt werden, werden als erhöhte Rechte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54106-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="54106-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**Ausführungsphase**</span><span class="sxs-lookup"><span data-stu-id="54106-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="54106-108">Wenn das Installationsprogramm ein Skript mit Installationsprogrammaktionen ausricht.</span><span class="sxs-lookup"><span data-stu-id="54106-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="54106-109">In Microsoft Windows 2000 wird dieser Vorgang vom Installationsprogrammdienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54106-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="54106-110">In einer verwalteten Anwendung wird das Skript mit Systemberechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54106-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="54106-111">Weitere Informationen finden Sie unter [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="54106-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="54106-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**Ausführungsskript**</span><span class="sxs-lookup"><span data-stu-id="54106-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="54106-113">Installationsprogrammaktionen für eine Installation.</span><span class="sxs-lookup"><span data-stu-id="54106-113">Installer actions for an installation.</span></span> <span data-ttu-id="54106-114">Das Ausführungsskript wird während der [*Erwerbsphase der*](a-gly.md) Installation generiert und während der [*Ausführungsphase ausgeführt.*](/windows)</span><span class="sxs-lookup"><span data-stu-id="54106-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="54106-115">Weitere Informationen finden Sie unter [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="54106-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="54106-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**Externe Quelldateien**</span><span class="sxs-lookup"><span data-stu-id="54106-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="54106-117">Quelldateien der zu installierenden Anwendung, die außerhalb der.msi [*gespeichert werden.*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="54106-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="54106-118">Mehrere externe Quelldateien können komprimiert und zusammen in einer im Paket enthaltenen [*Schränkdatei*](c-gly.md) gespeichert [*werden.*](p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="54106-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="54106-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**Externe Benutzeroberfläche**</span><span class="sxs-lookup"><span data-stu-id="54106-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="54106-120">Benutzeroberfläche, die vom Autor eines Installationspakets bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="54106-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="54106-121">Es werden nicht die internen Benutzeroberflächenfunktionen des Installationsprogramms verwendet.</span><span class="sxs-lookup"><span data-stu-id="54106-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="54106-122">Weitere Informationen finden Sie unter [Informationen zum Benutzeroberfläche](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="54106-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 
