---
description: Ein großes Upgrade kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung über die Befehlszeile oder eine ausführbare Datei Patchen.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864483"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="b2cf9-103">Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts</span><span class="sxs-lookup"><span data-stu-id="b2cf9-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="b2cf9-104">Ein großes Upgrade kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung über die Befehlszeile oder eine ausführbare Datei Patchen.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="b2cf9-105">Das Bereitstellen eines größeren Upgrades als Patch-Paket wird nicht empfohlen, da ein wichtiges Upgradepatch-Paket nicht mit anderen Updates sequenziert werden kann und da es sich bei dem Patch nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="b2cf9-106">Das [Msimsp.exe](msimsp-exe.md) -Hilfsprogramm kann nicht zum Generieren eines Patchpakets verwendet werden, das ein großes Upgrade anwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="b2cf9-107">Wenden Sie stattdessen größere Upgrades an, wie unter [Anwenden von größeren Upgrades durch die Installation des Produkts](applying-major-upgrades-by-installing-the-product.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="b2cf9-108">**So wenden Sie einen wichtigen Upgradepatch auf eine lokale Installation des Produkts an**</span><span class="sxs-lookup"><span data-stu-id="b2cf9-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="b2cf9-109">Starten Sie die Installation des Patches von der Befehlszeile aus, oder verwenden Sie eine ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="b2cf9-110">Um von der Befehlszeile aus zu starten, verwenden Sie msiexec/p Patch. msp.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="b2cf9-111">Um von einer ausführbaren Datei zu starten, rufen Sie [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder die [**Applypatch-Methode**](installer-applypatch.md) auf, und geben Sie dieselben Befehlszeilenargumente an.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="b2cf9-112">Beim Patchen einer Client Installation wird die Installationsquelle vom Installationsprogramm ignoriert, und die Dateien, die bereits auf dem Computer des Benutzers installiert sind, werden gepatcht.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="b2cf9-113">Das Installationsprogramm ändert alle gepatchten Komponenten, die als "Run-From-Source" gekennzeichnet sind, in "lokal</span><span class="sxs-lookup"><span data-stu-id="b2cf9-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="b2cf9-114">Benutzer können diese Komponenten nicht aus der Quelle ausführen, solange der Patch auf dem Computer verbleibt.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="b2cf9-115">Das Installationsprogramm fügt alle Transformationen hinzu, die zum Aktualisieren der MSI-Datei verwendet werden, oder fügt dem Benutzerprofil patchspezifische Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="b2cf9-116">Das Installationsprogramm speichert die MSI-Datei auf dem Computer des Benutzers zwischen, sodass die Anwendung bei Bedarf installiert, neu installiert und repariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="b2cf9-117">Nachdem ein Patch auf eine eigenständige Installation angewendet wurde, verweist das Installationsprogramm auf zwei oder mehr Quell Listen auf externe Dateien: eine für die ursprüngliche Quelle und eine für jeden angewendeten Patch.</span><span class="sxs-lookup"><span data-stu-id="b2cf9-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



