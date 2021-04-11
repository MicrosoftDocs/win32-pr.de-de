---
description: Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise von der Befehlszeile oder von einem Programm neu installiert wird.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Anwenden von kleinen Updates durch Neuinstallation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959532"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="aae3c-103">Anwenden von kleinen Updates durch Neuinstallation des Produkts</span><span class="sxs-lookup"><span data-stu-id="aae3c-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="aae3c-104">Ein kleines Update kann auf eine Anwendung angewendet werden, indem die Anwendung vollständig oder teilweise von der Befehlszeile oder von einem Programm neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="aae3c-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="aae3c-105">**So verteilen Sie das kleine Update über die Befehlszeile an die aktuellen Benutzer (Hierbei handelt es sich um eine komplette Neuinstallation)**</span><span class="sxs-lookup"><span data-stu-id="aae3c-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="aae3c-106">Verwenden Sie in der Befehlszeile einen der folgenden Befehle: **msiexec/fvomus \[** _path to aktualisierte MSI-Datei_ *_\]_* oder **msiexec/I \[** _path to aktualisierte. msi file_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.</span><span class="sxs-lookup"><span data-stu-id="aae3c-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="aae3c-107">Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="aae3c-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="aae3c-108">Beachten Sie, dass der Benutzer das Produkt nicht mithilfe der Option "Software" erneut installieren kann, da sich die aktualisierte MSI-Datei noch nicht auf dem Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="aae3c-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="aae3c-109">**So verteilen Sie ein kleines Update von einem Programm an die aktuellen Benutzer (Dies ist eine komplette Neuinstallation)**</span><span class="sxs-lookup"><span data-stu-id="aae3c-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="aae3c-110">Geben Sie in einem Programm [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) ein, und geben Sie REINSTALLMODE \_ Package, REINSTALLMODE \_ fileolderversion, REINSTALLMODE \_ MachineData, REINSTALLMODE \_ UserData und REINSTALLMODE \_ Shortcut an.</span><span class="sxs-lookup"><span data-stu-id="aae3c-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="aae3c-111">Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="aae3c-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="aae3c-112">Mit der folgenden Methode wird eine Neuinstallation der Features oder Komponenten gestartet, die vom kleinen Update betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="aae3c-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="aae3c-113">**So übertragen Sie ein kleines Update an die aktuellen Benutzer (Hierbei handelt es sich um eine partielle Neuinstallation)**</span><span class="sxs-lookup"><span data-stu-id="aae3c-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="aae3c-114">Abrufen einer Liste der Namen von Features und Komponenten, die von dem kleinen Update betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="aae3c-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="aae3c-115">Geben Sie an der Eingabeaufforderung Folgendes ein: **msiexec/I \[** _path to aktualisierte. msi file_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.</span><span class="sxs-lookup"><span data-stu-id="aae3c-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="aae3c-116">Die aktualisierte MSI-Datei wird auf dem Computer des Benutzers zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="aae3c-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



