---
description: Autoren von Installationspaketen sollten immer die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung erneut ausführen, wenn Sie Änderungen am Paket vornehmen.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Überprüfen einer Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861892"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="823ec-103">Überprüfen einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="823ec-103">Validating an Installation Database</span></span>

<span data-ttu-id="823ec-104">Autoren von Installationspaketen sollten immer die Validierung Ihrer Pakete ausführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren, und die Überprüfung erneut ausführen, wenn Sie Änderungen am Paket vornehmen.</span><span class="sxs-lookup"><span data-stu-id="823ec-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="823ec-105">Die Validierung scannt die Datenbank auf Fehler, die möglicherweise einzeln angezeigt werden, aber ein falsches Verhalten im Kontext der gesamten Datenbank verursachen.</span><span class="sxs-lookup"><span data-stu-id="823ec-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="823ec-106">Wenn Sie versuchen, ein Paket zu installieren, bei dem die Überprüfung nicht erfolgreich ist, können Sie das System</span><span class="sxs-lookup"><span data-stu-id="823ec-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="823ec-107">Weitere Informationen finden Sie in den Abschnitten [Package Validation](package-validation.md) und [internal Konsistenz Evaluators-ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="823ec-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="823ec-108">Sie können das Beispiel Paket mit [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="823ec-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="823ec-109">Zum Anzeigen der Hilfe für Msival2.exe wechseln Sie in die Befehlszeile, und geben Sie ein.</span><span class="sxs-lookup"><span data-stu-id="823ec-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="823ec-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="823ec-110">Msival2 -?</span></span>

<span data-ttu-id="823ec-111">Die CUB-Datei "Darice. Cub" enthält die benutzerdefinierten Ice-Aktionen, die Msival2.exe zum Durchführen der Validierung benötigt.</span><span class="sxs-lookup"><span data-stu-id="823ec-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="823ec-112">So überprüfen Sie die MNP2000.msi EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="823ec-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="823ec-113">msival2 MNP2000.msi Darice. Cub</span><span class="sxs-lookup"><span data-stu-id="823ec-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="823ec-114">Eine Beschreibung der von der Validierung zurückgegebenen Fehler-und Warnmeldungen finden Sie in der [Ice-Referenz](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="823ec-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="823ec-115">Korrigieren Sie alle Fehler im Paket, und führen Sie die Überprüfung nach Bedarf erneut aus, bis das Paket die Überprüfung ohne Fehler bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="823ec-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="823ec-116">Sobald das Paket die Überprüfung bestanden hat, können Sie das Beispiel Paket installieren, indem Sie auf das MNP2000.msi Symbol oder über die Befehlszeile mit den [Befehlszeilenoptionen](command-line-options.md)klicken.</span><span class="sxs-lookup"><span data-stu-id="823ec-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="823ec-117">Dies schließt die Beispiel Installation ab.</span><span class="sxs-lookup"><span data-stu-id="823ec-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="823ec-118">Nächstes Beispiel</span><span class="sxs-lookup"><span data-stu-id="823ec-118">Next example</span></span>

[<span data-ttu-id="823ec-119">Ein upgradebeispiel</span><span class="sxs-lookup"><span data-stu-id="823ec-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



