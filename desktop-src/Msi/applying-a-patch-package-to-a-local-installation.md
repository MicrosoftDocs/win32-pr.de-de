---
description: Sie können das kleine Update auf eine lokale Installation von MNP2000 mit dem Beispiel Patch mnppatch. msp anwenden, der beim Erstellen eines Patchpakets erstellt wurde.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Anwenden eines Patchpakets auf eine lokale Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215721"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="47087-103">Anwenden eines Patchpakets auf eine lokale Installation</span><span class="sxs-lookup"><span data-stu-id="47087-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="47087-104">Sie können das kleine Update auf eine lokale Installation von MNP2000 mit dem Beispiel Patch mnppatch. msp anwenden, der beim [Erstellen eines Patchpakets](generating-a-patch-package.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="47087-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="47087-105">Das allgemeine Verfahren wird im Abschnitt Anwenden von [kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="47087-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="47087-106">Installieren Sie das ursprüngliche MNP2000-Produkt lokal auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="47087-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="47087-107">Vergewissern Sie sich, dass die Fehlermeldung Concert.txt, die durch das kleine Update behoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="47087-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="47087-108">Starten Sie als nächstes die Installation, indem Sie die folgende Befehlszeile eingeben.</span><span class="sxs-lookup"><span data-stu-id="47087-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="47087-109">**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**</span><span class="sxs-lookup"><span data-stu-id="47087-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="47087-110">Überprüfen Sie die Concert.txt zu "MNP2000", um sicherzustellen, dass das Installationsprogramm das kleine Update angewendet hat, um diese Datei zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="47087-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="47087-111">Informationen zum Anwenden des kleinen Updates auf ein administratives Image finden Sie unter [Anwenden eines Patchpakets auf eine administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="47087-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="47087-112">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="47087-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 



