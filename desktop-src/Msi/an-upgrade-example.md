---
description: In den folgenden Abschnitten finden Sie ein Beispiel für die Erstellung eines upgradepakets für die Anwendung, die in einem Installations Beispiel beschrieben wird.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Ein upgradebeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362425"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="36f8f-103">Ein upgradebeispiel</span><span class="sxs-lookup"><span data-stu-id="36f8f-103">An Upgrade Example</span></span>

<span data-ttu-id="36f8f-104">In den folgenden Abschnitten finden Sie ein Beispiel für die Erstellung eines upgradepakets für die Anwendung, die in [einem Installations Beispiel](an-installation-example.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="36f8f-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="36f8f-105">Ein Beispiel für eine minimale Benutzeroberfläche für dieses Beispiel wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) als Datei Uisample.msi bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="36f8f-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="36f8f-106">Wenn Sie über das SDK verfügen, haben Sie Zugriff auf alle Tools und Daten, die für die Reproduktion des Beispiel Installationspakets, der Benutzeroberfläche und des beispielupgradepakets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="36f8f-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="36f8f-107">In diesem Beispiel wird veranschaulicht, wie ein Windows Installer Paket erstellt wird, das das hypothetische Product MNP2000 auf ein neues Produkt mit dem Namen MNP2001 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="36f8f-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="36f8f-108">Das Upgradepaket für das Beispiel wendet ein großes Upgrade auf das Produkt an, das das Ändern des Produktcodes erfordert.</span><span class="sxs-lookup"><span data-stu-id="36f8f-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="36f8f-109">Weitere Informationen zu größeren Upgrades finden Sie im Thema zu den [wichtigsten Upgrades](major-upgrades.md) im Abschnitt " [Patching und Upgrades](patching-and-upgrades.md) ".</span><span class="sxs-lookup"><span data-stu-id="36f8f-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="36f8f-110">Das Beispiel Aktualisierungs Paket verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="36f8f-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="36f8f-111">Um dieses Upgrade auf MNP2001 zu qualifizieren, muss ein Benutzer die Versionen 1,0 bis 1,4 (einschließlich) der englischen Sprache MNP2000 mit Windows Installer installiert haben.</span><span class="sxs-lookup"><span data-stu-id="36f8f-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="36f8f-112">Wenn ein Benutzer versucht, das Upgradepaket zu installieren, durchsucht die upgradefunktion von Windows Installer den Computer des Benutzers nach allen Produkten, die für das Upgrade qualifiziert sind.</span><span class="sxs-lookup"><span data-stu-id="36f8f-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="36f8f-113">Windows Installer migriert alle der Funktionseinstellungen des ursprünglichen Produkts zu dem aktualisierten Produkt.</span><span class="sxs-lookup"><span data-stu-id="36f8f-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="36f8f-114">Das Installationsprogramm entfernt alle veralteten Features vom Computer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="36f8f-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="36f8f-115">Das Installationsprogramm installiert alle neuen Features, die zum Upgrade gehören.</span><span class="sxs-lookup"><span data-stu-id="36f8f-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="36f8f-116">Durch eine Deinstallation des upgradepakets wird das Produkt auf dem Computer des Benutzers entfernt, und die frühere Version des Produkts wird nicht wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="36f8f-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="36f8f-117">Das Beispiel Upgrade aktualisiert Verknüpfungen zu neuen Dateien und Features.</span><span class="sxs-lookup"><span data-stu-id="36f8f-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="36f8f-118">Planen eines größeren Upgrades</span><span class="sxs-lookup"><span data-stu-id="36f8f-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="36f8f-119">Importieren der ursprünglichen Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="36f8f-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="36f8f-120">Aktualisieren der Verzeichnisstruktur für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-121">Aktualisieren von Dateien und Dateiattributen für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-122">Aktualisieren von Komponenten für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-123">Aktualisieren von Features für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-124">Aktualisieren von Verknüpfungen für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-125">Aktualisieren der upgradetabelle für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-126">Aktualisieren von Eigenschaften für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-127">Aktualisieren von Sequenz Tabellen für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-128">Aktualisieren von Zusammenfassungs Informationen für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="36f8f-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="36f8f-129">Überprüfen eines Installations Upgrades</span><span class="sxs-lookup"><span data-stu-id="36f8f-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



