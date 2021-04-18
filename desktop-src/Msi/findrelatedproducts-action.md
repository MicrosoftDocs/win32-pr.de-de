---
description: Die Aktion FindRelatedProducts wird nacheinander durch jeden Datensatz der upgradetabelle durchlaufen und vergleicht den UpgradeCode, die Produktversion und die Sprache in jeder Zeile mit den auf dem System installierten Produkten.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: FindRelatedProducts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347168"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="d4bdf-103">FindRelatedProducts-Aktion</span><span class="sxs-lookup"><span data-stu-id="d4bdf-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="d4bdf-104">Die Aktion FindRelatedProducts wird nacheinander durch jeden Datensatz der [upgradetabelle](upgrade-table.md) durchlaufen und vergleicht den UpgradeCode, die Produktversion und die Sprache in jeder Zeile mit den auf dem System installierten Produkten.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="d4bdf-105">Wenn "FindRelatedProducts" eine Übereinstimmung zwischen den Upgradeinformationen und einem installierten Produkt erkennt, fügt Sie den Produktcode an die Eigenschaft an, die in der Spalte "Aktions Eigenschaft" von "upgradetable" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="d4bdf-106">Die Aktion "FindRelatedProducts" wird nur bei der erstmaligen Installation des Produkts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="d4bdf-107">Die Aktion "FindRelatedProducts" wird während des Wartungsmodus oder der nicht Installation nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="d4bdf-108">Abgefragte Datenbanktabellen</span><span class="sxs-lookup"><span data-stu-id="d4bdf-108">Database Tables Queried</span></span>

<span data-ttu-id="d4bdf-109">Mit dieser Aktion wird die folgende Tabelle abgefragt:</span><span class="sxs-lookup"><span data-stu-id="d4bdf-109">This action queries the following table:</span></span>

[<span data-ttu-id="d4bdf-110">Upgradetabelle</span><span class="sxs-lookup"><span data-stu-id="d4bdf-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="d4bdf-111">Verwendete Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4bdf-111">Properties Used</span></span>

<span data-ttu-id="d4bdf-112">Die Aktion FindRelatedProducts verwendet die [**UpgradeCode**](upgradecode.md) -Eigenschaft und die in der upgradetabelle erstellten Versions-und Sprachinformationen, um installierte Produkte zu erkennen, die von dem ausstehenden Upgrade betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="d4bdf-113">Der Produktcode der erkannten Produkte wird an die Eigenschaft in der Spalte "Aktions Eigenschaft" von "upgradetable" angehängt.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="d4bdf-114">FindRelatedProducts erkennt nur vorhandene Produkte, die mithilfe des Windows Installer mit einer MSI-Datei installiert wurden, die eine [**UpgradeCode**](upgradecode.md) -Eigenschaft definiert, eine [**ProductVersion**](productversion.md) -Eigenschaft und einen Wert für die [**productlanguage**](productlanguage.md) -Eigenschaft, die eine der in der [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft aufgelisteten Sprachen ist.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="d4bdf-115">Beachten Sie, dass "FindRelatedProducts" die von " [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)" zurückgegebene Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="d4bdf-116">Damit FindRelatedProducts ordnungsgemäß funktioniert, muss der Paket Ersteller sicherstellen, dass die [**productlanguage**](productlanguage.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) auf eine Sprache festgelegt ist, die auch in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="d4bdf-117">Weitere [wichtige Upgrades finden Sie unter Vorbereiten einer Anwendung](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d4bdf-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d4bdf-118">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d4bdf-118">Sequence Restrictions</span></span>

<span data-ttu-id="d4bdf-119">FindRelatedProducts muss in der Tabelle " [InstallUISequence](installuisequence-table.md) " und in [InstallExecuteSequence](installexecutesequence-table.md) -Tabellen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="d4bdf-120">Das Installationsprogramm verhindert, dass findrelated-Produkte in InstallExecuteSequence ausgeführt werden, wenn die Aktion bereits in InstallUISequence ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="d4bdf-121">Die FindRelatedProducts-Aktion muss vor der Aktion " [MigrateFeatureStates](migratefeaturestates-action.md) " und der [Aktion "RemoveExistingProducts](removeexistingproducts-action.md)" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d4bdf-122">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="d4bdf-122">ActionData Messages</span></span>

<span data-ttu-id="d4bdf-123">FindRelatedProducts sendet eine Aktions Daten Nachricht für jedes zugehörige Produkt, das auf dem System erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="d4bdf-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



