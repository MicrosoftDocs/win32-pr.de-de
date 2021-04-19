---
description: Wenn Sie Änderungen am Paket vornehmen, sollten Entwickler von Upgradepaketen stets die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren und die Überprüfung erneut auszuführen.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Überprüfen eines Installations Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369907"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="e18b1-103">Überprüfen eines Installations Upgrades</span><span class="sxs-lookup"><span data-stu-id="e18b1-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="e18b1-104">Wenn Sie Änderungen am Paket vornehmen, sollten Entwickler von Upgradepaketen stets die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren und die Überprüfung erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e18b1-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="e18b1-105">Führen Sie die Überprüfung für ein Upgradepaket auf die gleiche Weise wie für ein-Installationspaket aus.</span><span class="sxs-lookup"><span data-stu-id="e18b1-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="e18b1-106">Weitere Informationen finden Sie unter [Validieren einer Installations Datenbank](validating-an-installation-database.md).</span><span class="sxs-lookup"><span data-stu-id="e18b1-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="e18b1-107">Dadurch wird das Beispiel Aktualisierungs Paket abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e18b1-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="e18b1-108">Um das Upgrade zu installieren, installieren Sie zunächst MNP2000.msi, und installieren Sie dann MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="e18b1-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="e18b1-109">Bei der Deinstallation von MNP2001 werden sowohl die ursprünglichen Produkte als auch die upgradeprodukte von Ihrem Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="e18b1-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="e18b1-110">Nächstes Beispiel</span><span class="sxs-lookup"><span data-stu-id="e18b1-110">Next example</span></span>

[<span data-ttu-id="e18b1-111">Beispiel für eine Anpassungs Transformation</span><span class="sxs-lookup"><span data-stu-id="e18b1-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



