---
description: Ein großes Upgrade kann durch Installieren des neuen Installationspakets für das aktualisierte Produkt angewendet werden.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Anwenden von größeren Upgrades durch Installieren des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347123"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="42ef7-103">Anwenden von größeren Upgrades durch Installieren des Produkts</span><span class="sxs-lookup"><span data-stu-id="42ef7-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="42ef7-104">Ein großes Upgrade kann durch Installieren des neuen Installationspakets für das aktualisierte Produkt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="42ef7-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="42ef7-105">Da größere Upgrades einen anderen Produktcode als das ursprüngliche Produkt erhalten, muss die Installation des Upgrades als Installation eines neuen Produkts behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="42ef7-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="42ef7-106">Das Upgrade kann einfach wie ein anderes Produkt installiert werden.</span><span class="sxs-lookup"><span data-stu-id="42ef7-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="42ef7-107">Das neue Installationspaket kann das Entfernen des alten Produkts durch einschließen der [upgradetabelle](upgrade-table.md) und der Aktion [FindRelatedProducts](findrelatedproducts-action.md) und [RemoveExistingProducts](removeexistingproducts-action.md)verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="42ef7-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="42ef7-108">**So verteilen Sie ein großes Upgrade an aktuelle Benutzer über die Befehlszeile**</span><span class="sxs-lookup"><span data-stu-id="42ef7-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="42ef7-109">Verwenden Sie in der Befehlszeile: **msiexec/i \[** _path to aktualisierte msi file_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="42ef7-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="42ef7-110">**So verteilen Sie ein großes Upgrade an aktuelle Benutzer von einem Programm**</span><span class="sxs-lookup"><span data-stu-id="42ef7-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="42ef7-111">Geben Sie in einem Programm [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ein, und geben Sie den Pfad zur aktualisierten MSI-Datei an.</span><span class="sxs-lookup"><span data-stu-id="42ef7-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



