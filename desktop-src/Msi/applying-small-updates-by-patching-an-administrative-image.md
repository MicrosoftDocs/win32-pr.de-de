---
description: Bei einer administrativen Installation wird ein Quell Abbild einer Anwendung oder eines Produkts in einem Netzwerk erstellt.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959534"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="a6b1b-103">Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds</span><span class="sxs-lookup"><span data-stu-id="a6b1b-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="a6b1b-104">Bei einer [administrativen Installation](administrative-installation.md) wird ein Quell Abbild einer Anwendung oder eines Produkts in einem Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="a6b1b-105">Benutzer in einer Arbeitsgruppe, die Zugriff auf dieses administrative image haben, können das Produkt aus dieser Quelle installieren.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="a6b1b-106">Das Aktualisieren der Anwendung für diese Arbeitsgruppe erfolgt in zwei Schritten:</span><span class="sxs-lookup"><span data-stu-id="a6b1b-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="a6b1b-107">Zuerst kann der Patch für kleine Updates auf das administrative Abbild angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="a6b1b-108">Zweitens müssen die Änderungen am kleinen Update an die Benutzer weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="a6b1b-109">**So wenden Sie einen kleinen Update Patch auf ein administratives Image an**</span><span class="sxs-lookup"><span data-stu-id="a6b1b-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="a6b1b-110">Abrufen des kleinen Updates in Form eines [Patchpakets](patch-packages.md)</span><span class="sxs-lookup"><span data-stu-id="a6b1b-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="a6b1b-111">Beispielsweise das kleine Update mit dem Namen Patch. msp.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="a6b1b-112">Abrufen des Pfads zum administrativen Image.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="a6b1b-113">Verwenden Sie in der Befehlszeile Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6b1b-113">From the command line use:</span></span>

    <span data-ttu-id="a6b1b-114">**msiexec/a** *\[ Pfad zur \] Datei "administrativer Image. msi* " **/p** *Patch. msp*</span><span class="sxs-lookup"><span data-stu-id="a6b1b-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="a6b1b-115">Dadurch werden die Anwendungs Dateien und die MSI-Datei des administrativen Abbilds aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="a6b1b-116">Eine Liste der Optionen, die mit Msiexec.exe verwendet werden können, finden Sie unter [Befehlszeilenoptionen](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="a6b1b-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="a6b1b-117">Windows Installer ermittelt automatisch, ob das administrative image kurze Dateinamen verwendet, und legt die [**shortfileames**](shortfilenames.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="a6b1b-118">Das resultierende administrative image ist identisch mit dem, das von einer administrativen Installation mithilfe einer vollständigen Produkt-CD-ROM erstellt wurde, die das Update enthält.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="a6b1b-119">Wenn neue Benutzer die Anwendung aus dieser Quelle installieren, erhalten Sie die aktualisierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="a6b1b-120">**So verteilen Sie das kleine Update an die Arbeitsgruppe**</span><span class="sxs-lookup"><span data-stu-id="a6b1b-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="a6b1b-121">Mitglieder der Arbeitsgruppe erhalten die Änderungen, indem Sie die Anwendung über das administrative image neu installieren. verwenden Sie hierzu das unter [Anwenden von kleinen Updates durch Neuinstallieren des Produkts](applying-small-updates-by-reinstalling-the-product.md)beschriebene Verfahren.</span><span class="sxs-lookup"><span data-stu-id="a6b1b-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



