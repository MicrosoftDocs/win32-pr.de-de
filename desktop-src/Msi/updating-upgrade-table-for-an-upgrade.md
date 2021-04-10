---
description: Zum Anwenden eines größeren Upgrades mithilfe von Windows Installer muss das ursprüngliche Produkt Installationspaket eine UpgradeCode-Eigenschaft angeben, die unter Vorbereiten einer Anwendung für zukünftige größere Upgrades beschrieben wird, und das Upgradepaket muss eine upgradetabelle aufweisen.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aktualisieren der upgradetabelle für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131196"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="bb90d-103">Aktualisieren der upgradetabelle für ein Upgrade</span><span class="sxs-lookup"><span data-stu-id="bb90d-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="bb90d-104">Zum Anwenden eines größeren Upgrades mithilfe von Windows Installer muss das ursprüngliche Produkt Installationspaket eine UpgradeCode-Eigenschaft angeben, die unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)beschrieben wird, und das [**Upgradepaket muss eine upgradetabelle**](upgradecode.md) aufweisen. [](upgrade-table.md)</span><span class="sxs-lookup"><span data-stu-id="bb90d-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="bb90d-105">Weitere Informationen zu größeren Upgrades finden Sie unter [wichtige Upgrades](major-upgrades.md) bei [Patching und Upgrades](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="bb90d-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="bb90d-106">Dem Installationspaket MNP2000.msi wurde eine [**UpgradeCode**](upgradecode.md) -Eigenschaft zugewiesen, wie im Abschnitt Angeben von [Eigenschaften](specifying-properties.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bb90d-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="bb90d-107">Windows Installer wendet das Upgrade an, wenn der Benutzer bereits die Versionen 1,0 bis 1,4 (einschließlich) der englischen Sprache MNP2000 installiert hat.</span><span class="sxs-lookup"><span data-stu-id="bb90d-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="bb90d-108">Windows Installer migriert alle Funktionseinstellungen des ursprünglichen Produkts zum aktualisierten Produkt.</span><span class="sxs-lookup"><span data-stu-id="bb90d-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="bb90d-109">Das Installationsprogramm entfernt die Dateien, die zu den ursprünglichen Produkten gehören, die nicht von der Aktualisierung des Produkts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb90d-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="bb90d-110">Wenn Ihre Kopie von MNP2001.msi keine [upgradetabelle](upgrade-table.md)enthält, verwenden Sie "Orca" oder einen anderen Tabellen-Editor, um eine leere upgradetabelle aus Schema.msi in die-Datenbank zu importieren.</span><span class="sxs-lookup"><span data-stu-id="bb90d-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="bb90d-111">Das SDK stellt eine Kopie Schema.msi bereit.</span><span class="sxs-lookup"><span data-stu-id="bb90d-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="bb90d-112">Öffnen Sie MNP2001.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere upgradetabelle ein.</span><span class="sxs-lookup"><span data-stu-id="bb90d-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="bb90d-113">UpgradeCode auch</span><span class="sxs-lookup"><span data-stu-id="bb90d-113">UpgradeCode</span></span>                            | <span data-ttu-id="bb90d-114">Versionmin</span><span class="sxs-lookup"><span data-stu-id="bb90d-114">VersionMin</span></span> | <span data-ttu-id="bb90d-115">Versionmax</span><span class="sxs-lookup"><span data-stu-id="bb90d-115">VersionMax</span></span> | <span data-ttu-id="bb90d-116">Sprache</span><span class="sxs-lookup"><span data-stu-id="bb90d-116">Language</span></span> | <span data-ttu-id="bb90d-117">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb90d-117">Attributes</span></span> | <span data-ttu-id="bb90d-118">Entfernen</span><span class="sxs-lookup"><span data-stu-id="bb90d-118">Remove</span></span> | <span data-ttu-id="bb90d-119">Aktions Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bb90d-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="bb90d-120">{908e378a-9551-4772-BF1D-5cfaf6fd9cb4}</span><span class="sxs-lookup"><span data-stu-id="bb90d-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="bb90d-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="bb90d-121">01.00.0000</span></span> | <span data-ttu-id="bb90d-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="bb90d-122">01.40.0000</span></span> | <span data-ttu-id="bb90d-123">1033</span><span class="sxs-lookup"><span data-stu-id="bb90d-123">1033</span></span>     | <span data-ttu-id="bb90d-124">769</span><span class="sxs-lookup"><span data-stu-id="bb90d-124">769</span></span>        |        | <span data-ttu-id="bb90d-125">Oldappfound</span><span class="sxs-lookup"><span data-stu-id="bb90d-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="bb90d-126">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="bb90d-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



