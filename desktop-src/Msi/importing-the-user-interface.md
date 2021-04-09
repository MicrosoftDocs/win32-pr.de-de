---
description: Zusätzlich zu den Informationen, die in den vorherigen Abschnitten erläutert wurden, enthält uisample.msi auch Daten für eine Beispiel Benutzeroberfläche.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importieren der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863039"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="9adf7-103">Importieren der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="9adf7-103">Importing the User Interface</span></span>

<span data-ttu-id="9adf7-104">Zusätzlich zu den Informationen, die in den vorherigen Abschnitten erläutert wurden, enthält uisample.msi auch Daten für eine Beispiel Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="9adf7-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="9adf7-105">Wenn Sie uisample.msi im Abschnitt [Importieren einer leeren Datenbank](importing-a-blank-database.md)in MNP2000.msi zusammengeführt haben, sind diese Informationen auch in MNP2000.msi vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9adf7-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="9adf7-106">Die Informationen für die Beispiel Benutzeroberfläche finden Sie in den folgenden Tabellen.</span><span class="sxs-lookup"><span data-stu-id="9adf7-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="9adf7-107">Tabelle "aktiontext"</span><span class="sxs-lookup"><span data-stu-id="9adf7-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="9adf7-108">Binäre Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="9adf7-109">Steuerungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="9adf7-110">ControlEvent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="9adf7-111">Dialog Feld Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="9adf7-112">Fehler Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="9adf7-113">EventMapping-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="9adf7-114">RadioButton-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="9adf7-115">TextStyle-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="9adf7-116">UIText-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="9adf7-117">Der Datenbank-Editor, der mit dem Installationsprogramm bereitgestellt wird, enthält eine Dialogfeld Vorschau-Option, mit der Sie eine Vorschau der Dialogfelder der Benutzeroberfläche anzeigen können, die in den obigen Tabellen in den Daten angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9adf7-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="9adf7-118">Das Beispiel Installationspaket MNP2000.msi ist jetzt für die Paketüberprüfung bereit.</span><span class="sxs-lookup"><span data-stu-id="9adf7-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="9adf7-119">Führen Sie die Überprüfung immer für ein neues Paket aus, bevor Sie das Paket zum ersten Mal installieren.</span><span class="sxs-lookup"><span data-stu-id="9adf7-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="9adf7-120">Dies wird unter Validieren des Installations Beispiels erläutert.</span><span class="sxs-lookup"><span data-stu-id="9adf7-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="9adf7-121">Wenn Sie die Benutzeroberfläche nicht in das Beispiel Paket einschließen möchten, können Sie alle Informationen in den oben gezeigten Tabellen weglassen oder entfernen, mit Ausnahme der [TextStyle-Tabelle](textstyle-table.md) (die zum Definieren der [**defaultuifont**](defaultuifont.md) -Eigenschaft erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="9adf7-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="9adf7-122">Sie sollten auch die Eigenschaften der Benutzeroberfläche aus der Eigenschaften [Tabelle](property-table.md)entfernen.</span><span class="sxs-lookup"><span data-stu-id="9adf7-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="9adf7-123">Im folgenden wird eine Beispiel Eigenschaften Tabelle für das Notepad-Beispiel ohne Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9adf7-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="9adf7-124">Verwenden Sie die in der Tabelle gezeigten GUIDs nicht erneut, wenn Sie dieses Beispiel kopieren.</span><span class="sxs-lookup"><span data-stu-id="9adf7-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="9adf7-125">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="9adf7-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="9adf7-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9adf7-126">Property</span></span>                                   | <span data-ttu-id="9adf7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9adf7-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="9adf7-128">**Defaultuifont**</span><span class="sxs-lookup"><span data-stu-id="9adf7-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="9adf7-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="9adf7-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="9adf7-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="9adf7-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="9adf7-131">3</span><span class="sxs-lookup"><span data-stu-id="9adf7-131">3</span></span>                                      |
| [<span data-ttu-id="9adf7-132">**Limitui**</span><span class="sxs-lookup"><span data-stu-id="9adf7-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="9adf7-133">1</span><span class="sxs-lookup"><span data-stu-id="9adf7-133">1</span></span>                                      |
| [<span data-ttu-id="9adf7-134">**Hersteller**</span><span class="sxs-lookup"><span data-stu-id="9adf7-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="9adf7-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="9adf7-135">Microsoft</span></span>                              |
| [<span data-ttu-id="9adf7-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="9adf7-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="9adf7-137">{18a9233c-0b34-4127-a966-c257386270bc}</span><span class="sxs-lookup"><span data-stu-id="9adf7-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="9adf7-138">**Productlanguage**</span><span class="sxs-lookup"><span data-stu-id="9adf7-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="9adf7-139">1033</span><span class="sxs-lookup"><span data-stu-id="9adf7-139">1033</span></span>                                   |
| [<span data-ttu-id="9adf7-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="9adf7-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="9adf7-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="9adf7-141">MNP2000</span></span>                                |
| [<span data-ttu-id="9adf7-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="9adf7-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="9adf7-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="9adf7-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="9adf7-144">**UpgradeCode auch**</span><span class="sxs-lookup"><span data-stu-id="9adf7-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="9adf7-145">{908e378a-9551-4772-BF1D-5cfaf6fd9cb4}</span><span class="sxs-lookup"><span data-stu-id="9adf7-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="9adf7-146">Ein Paket ohne Benutzeroberfläche kann von der Befehlszeile oder von einem Programm installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9adf7-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="9adf7-147">Verwenden Sie die unter [Befehlszeilenoptionen](command-line-options.md)beschriebenen Methoden, um ein Paket über die Befehlszeile zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9adf7-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="9adf7-148">Verwenden Sie zum Installieren eines Pakets von einem Programm die unter [using Installer Functions](using-installer-functions.md)beschriebenen Methoden.</span><span class="sxs-lookup"><span data-stu-id="9adf7-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="9adf7-149">Führen Sie die Überprüfung immer für ein neues Paket aus, bevor Sie ein neues Paket zum ersten Mal installieren.</span><span class="sxs-lookup"><span data-stu-id="9adf7-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="9adf7-150">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="9adf7-150">Continue</span></span>](validating-an-installation-database.md)

 

 



