---
description: Eine Aktion wird in der Windows Installer ausgeführt, indem entweder die msidoaction-Funktion aufgerufen oder die Aktion in einer Sequenz Tabelle eingeschlossen wird.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Verwenden von Standard Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360173"
---
# <a name="using-standard-actions"></a><span data-ttu-id="90247-103">Verwenden von Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="90247-103">Using Standard Actions</span></span>

<span data-ttu-id="90247-104">Eine Aktion wird in der Windows Installer ausgeführt, indem entweder die [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufgerufen oder die Aktion in einer Sequenz Tabelle eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="90247-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="90247-105">Da die meisten Aktionen einen einzigen Zweck Kapseln, besteht die gängigste Methode zum Verwenden von Aktionen darin, eine Reihe von Aktionen in einer Sequenz zu sortieren, um eine größere Aufgabe zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="90247-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="90247-106">Das Installationsprogramm verfügt über drei Standard Aktionen auf oberster Ebene, die einen zugeordneten Satz von Sequenz Tabellen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="90247-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="90247-107">Diese zugeordneten Sequenz Tabellen können Standard Aktionen, benutzerdefinierte Aktionen und Benutzeroberflächen Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="90247-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="90247-108">Jede Aktion in einer Sequenz Tabelle verfügt über eine zugeordnete Sequenznummer und kann auch über einen zugeordneten bedingten Ausdruck verfügen.</span><span class="sxs-lookup"><span data-stu-id="90247-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="90247-109">Alle Aktionen in einer Sequenz Tabelle werden in der angegebenen Reihenfolge besucht und nur ausgeführt, wenn der bedingte Ausdruck true ergibt.</span><span class="sxs-lookup"><span data-stu-id="90247-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="90247-110">Während einer Standardaktion eine beliebige Sequenznummer zugeordnet werden kann, haben viele Sequenz Beschränkungen, die befolgt werden müssen, damit die Aktion ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="90247-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="90247-111">Beispielsweise muss die [filecost-Aktion](filecost-action.md)nach der [costinitialize-Aktion](costinitialize-action.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="90247-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="90247-112">Weitere Informationen zu den standardmäßigen Aktions Sequenz Beschränkungen finden Sie unter [Aktionen mit Sequenz Einschränkungen](actions-with-sequencing-restrictions.md), [Aktionen ohne Sequenz Beschränkungen](actions-without-sequencing-restrictions.md)oder [Referenz zu Standard Aktionen](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="90247-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="90247-113">Die folgenden Themen enthalten weitere Informationen zur Verwendung von Standard Aktionen.</span><span class="sxs-lookup"><span data-stu-id="90247-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="90247-114">Veröffentlichen von Produkten, Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="90247-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="90247-115">Dateisuche</span><span class="sxs-lookup"><span data-stu-id="90247-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="90247-116">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="90247-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="90247-117">Datei Installation</span><span class="sxs-lookup"><span data-stu-id="90247-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="90247-118">Ändern der Registrierung</span><span class="sxs-lookup"><span data-stu-id="90247-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="90247-119">Ausführen von Aktionen</span><span class="sxs-lookup"><span data-stu-id="90247-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="90247-120">Weitere Informationen finden Sie unter [Standard Aktionen](about-standard-actions.md) oder [Referenz zu Standard Aktionen](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="90247-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



