---
description: Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie Sie einfach mithilfe von msiinstallproduct oder msikonfigurireproduct. Sie können eine angekündigte Anwendung auch über die Befehlszeile entfernen. Siehe Befehlszeilenoptionen.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Entfernen einer angekündigten Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866076"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="db200-105">Entfernen einer angekündigten Anwendung</span><span class="sxs-lookup"><span data-stu-id="db200-105">Removing an Advertised Application</span></span>

<span data-ttu-id="db200-106">Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie Sie einfach mithilfe von [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) oder [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="db200-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="db200-107">Sie können eine angekündigte Anwendung auch über die Befehlszeile entfernen.</span><span class="sxs-lookup"><span data-stu-id="db200-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="db200-108">Siehe [Befehlszeilenoptionen](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="db200-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="db200-109">Beachten Sie, dass es möglicherweise nicht möglich ist, eine angekündigte Anwendung zu entfernen, wenn Sie das Paket so verfasst haben, dass die Ausführung einer Installation von der Anweisung abhängt, die **nicht installiert** ist.</span><span class="sxs-lookup"><span data-stu-id="db200-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="db200-110">Eine angekündigte Anwendung ist nicht auf dem Computer des Benutzers installiert, und die [**installierte**](installed.md) Eigenschaft wird vom Installationsprogramm nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db200-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="db200-111">Das Paket muss erstellt werden, damit angekündigte Anwendungen deinstalliert werden können.</span><span class="sxs-lookup"><span data-stu-id="db200-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



