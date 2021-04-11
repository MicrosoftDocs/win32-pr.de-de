---
description: Wenn der Windows Installer das Installationsskript für die Installation eines Produkts oder einer Anwendung verarbeitet, generiert es gleichzeitig ein Rollback-Skript und speichert eine Kopie jeder Datei, die während der Installation gelöscht wurde.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Rollback-Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130665"
---
# <a name="rollback-installation"></a><span data-ttu-id="bf6a9-103">Rollback-Installation</span><span class="sxs-lookup"><span data-stu-id="bf6a9-103">Rollback Installation</span></span>

<span data-ttu-id="bf6a9-104">Wenn der Windows Installer das Installationsskript für die Installation eines Produkts oder einer Anwendung verarbeitet, generiert es gleichzeitig ein Rollback-Skript und speichert eine Kopie jeder Datei, die während der Installation gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="bf6a9-105">Diese Dateien werden in einem verborgenen System Verzeichnis gespeichert und automatisch gelöscht, sobald die Installation erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="bf6a9-106">Wenn die Installation jedoch nicht erfolgreich ist, führt das Installationsprogramm automatisch eine Rollback-Installation durch, bei der das System in seinen ursprünglichen Zustand zurückversetzt wird.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="bf6a9-107">Das automatische Rollback einer nicht erfolgreichen Installation ist das Standardverhalten des Installers.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="bf6a9-108">Um das Rollback während einer Installation zu deaktivieren, verwenden Sie eine der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="bf6a9-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="bf6a9-109">**DISABLEROLLBACK (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="bf6a9-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="bf6a9-110">**Promptrollbackcost (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="bf6a9-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="bf6a9-111">DISABLEROLLBACK-Aktion</span><span class="sxs-lookup"><span data-stu-id="bf6a9-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="bf6a9-112">DISABLEROLLBACK</span><span class="sxs-lookup"><span data-stu-id="bf6a9-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="bf6a9-113">Enablerollback-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="bf6a9-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="bf6a9-114">Wenn Rollback deaktiviert ist, legt das Installationsprogramm die [**rollbackdeaktiviert**](rollbackdisabled.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="bf6a9-115">Wenn eine Installation [benutzerdefinierte Aktionen](custom-actions.md)verwendet, ist eine zusätzliche Erstellung des Installationspakets erforderlich, um die Roll Back Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf6a9-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="bf6a9-116">Weitere Informationen finden Sie unter [Rollback für benutzerdefinierte Aktionen](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bf6a9-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



