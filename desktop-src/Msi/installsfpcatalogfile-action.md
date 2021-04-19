---
description: Mit der Aktion installsfpcatalogfile werden die von Windows Me für den Windows-Datei Schutz verwendeten Kataloge installiert.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Installsfpcatalogfile-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343234"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="fafe0-103">Installsfpcatalogfile-Aktion</span><span class="sxs-lookup"><span data-stu-id="fafe0-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="fafe0-104">Mit der Aktion installsfpcatalogfile werden die von Windows Me für den Windows-Datei Schutz verwendeten Kataloge installiert.</span><span class="sxs-lookup"><span data-stu-id="fafe0-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="fafe0-105">Installsfpcatalogfile fragt die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die [filesfpcatalog-Tabelle](filesfpcatalog-table.md) und die [sfpcatalog-Tabelle](sfpcatalog-table.md)ab.</span><span class="sxs-lookup"><span data-stu-id="fafe0-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="fafe0-106">Kataloge werden installiert, wenn Sie einer Datei in einer-Komponente zugeordnet sind, die für die lokale Installation festgelegt ist, oder wenn Sie einer Datei zugeordnet sind, die in einer lokal installierten Komponente repariert wird.</span><span class="sxs-lookup"><span data-stu-id="fafe0-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fafe0-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fafe0-107">Sequence Restrictions</span></span>

<span data-ttu-id="fafe0-108">Die Aktion installsfpcatalogfile muss vor " [InstallFiles](installfiles-action.md) " und nach " [costfinalize](costfinalize-action.md)" sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="fafe0-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fafe0-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="fafe0-109">ActionData Messages</span></span>



| <span data-ttu-id="fafe0-110">Feld</span><span class="sxs-lookup"><span data-stu-id="fafe0-110">Field</span></span> | <span data-ttu-id="fafe0-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="fafe0-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="fafe0-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fafe0-112">\[1\]</span></span> | <span data-ttu-id="fafe0-113">Der Name des zu installierenden Katalogs.</span><span class="sxs-lookup"><span data-stu-id="fafe0-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="fafe0-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fafe0-114">\[2\]</span></span> | <span data-ttu-id="fafe0-115">Der Name des Katalogs, von dem die Installation dieses Katalogs abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="fafe0-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fafe0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fafe0-116">Remarks</span></span>

<span data-ttu-id="fafe0-117">Ein Katalog, der von einem anderen Katalog abhängig ist, der nach dem übergeordneten Katalog installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fafe0-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



