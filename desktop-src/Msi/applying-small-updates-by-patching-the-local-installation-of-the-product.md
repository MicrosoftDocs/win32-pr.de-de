---
description: Ein kleines Update kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung Patchen.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959533"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="6379b-103">Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts</span><span class="sxs-lookup"><span data-stu-id="6379b-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="6379b-104">Ein kleines Update kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung Patchen.</span><span class="sxs-lookup"><span data-stu-id="6379b-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="6379b-105">**So wenden Sie einen kleinen Update Patch auf eine lokale Installation des Produkts an**</span><span class="sxs-lookup"><span data-stu-id="6379b-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="6379b-106">Starten Sie die Installation des Patches von der Befehlszeile aus, oder verwenden Sie eine ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="6379b-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="6379b-107">Um von der Befehlszeile aus zu starten, verwenden Sie **msiexec/p Patch. msp \[ REINSTALL =**_Feature List_ *_\] REINSTALLMODE = omus_*.</span><span class="sxs-lookup"><span data-stu-id="6379b-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="6379b-108">Um von einer ausführbaren Datei zu starten, rufen Sie [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder die [**Applypatch-Methode**](installer-applypatch.md) auf, und geben Sie dieselben Befehlszeilenargumente an.</span><span class="sxs-lookup"><span data-stu-id="6379b-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="6379b-109">Beim Patchen einer Client Installation wird die Installationsquelle vom Installationsprogramm ignoriert, und die Dateien, die bereits auf dem Computer des Benutzers installiert sind, werden gepatcht.</span><span class="sxs-lookup"><span data-stu-id="6379b-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="6379b-110">Das Installationsprogramm ändert alle gepatchten Komponenten, die als "Run-From-Source" gekennzeichnet sind, in "lokal</span><span class="sxs-lookup"><span data-stu-id="6379b-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="6379b-111">Benutzer können diese Komponenten nicht aus der Quelle ausführen, solange der Patch auf dem Computer verbleibt.</span><span class="sxs-lookup"><span data-stu-id="6379b-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="6379b-112">Das Installationsprogramm fügt alle Transformationen hinzu, die zum Aktualisieren der MSI-Datei verwendet werden, oder fügt dem Benutzerprofil patchspezifische Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6379b-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="6379b-113">Das Installationsprogramm speichert die MSI-Datei auf dem Computer des Benutzers zwischen, sodass die Anwendung bei Bedarf installiert, neu installiert und repariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6379b-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="6379b-114">Nach dem Anwenden eines Patches auf eine eigenständige Installation verweist das Installationsprogramm auf zwei oder mehr Quell Listen auf externe Dateien: eine für die ursprüngliche Quelle und eine für jeden angewendeten Patch.</span><span class="sxs-lookup"><span data-stu-id="6379b-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



