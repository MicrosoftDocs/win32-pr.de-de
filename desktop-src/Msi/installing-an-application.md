---
description: Sie können ganze Produkte mit Windows Installer Funktionen installieren. In den folgenden Schritten wird beschrieben, wie Sie ein Produkt installieren.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installieren einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352273"
---
# <a name="installing-an-application"></a><span data-ttu-id="ad90b-104">Installieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="ad90b-104">Installing an Application</span></span>

<span data-ttu-id="ad90b-105">Sie können ganze Produkte mit Windows Installer Funktionen installieren.</span><span class="sxs-lookup"><span data-stu-id="ad90b-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="ad90b-106">In den folgenden Schritten wird beschrieben, wie Sie ein Produkt installieren.</span><span class="sxs-lookup"><span data-stu-id="ad90b-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="ad90b-107">**So installieren Sie ein Produkt**</span><span class="sxs-lookup"><span data-stu-id="ad90b-107">**To install a product**</span></span>

1.  <span data-ttu-id="ad90b-108">Führen Sie ein Produkt durch die Installation oder die Deinstallier Sequenz aus, indem Sie die [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad90b-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="ad90b-109">Geben Sie die Installations Ebene an, indem Sie die [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad90b-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="ad90b-110">Sie können die Parameter der [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) -Funktion verwenden, um den Installationsstatus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ad90b-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="ad90b-111">Beispielsweise können Sie den Status für die lokale Installation festlegen oder die Installation über die Quelle durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="ad90b-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="ad90b-112">Sie können den Bereich von Produktfunktionen festlegen, die eingeschlossen werden sollen, indem Sie die Ebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="ad90b-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="ad90b-113">Weitere Informationen zum Installieren einer Anwendung finden Sie unter [Resilienz](resiliency.md) und [Installationsmechanismus](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="ad90b-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



