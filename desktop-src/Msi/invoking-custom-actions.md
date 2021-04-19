---
description: Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standard Aktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenz Tabelle.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Aufrufen von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349681"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="07e55-103">Aufrufen von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="07e55-103">Invoking Custom Actions</span></span>

<span data-ttu-id="07e55-104">Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standard Aktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenz Tabelle.</span><span class="sxs-lookup"><span data-stu-id="07e55-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="07e55-105">Es gibt zwei Methoden zum Aufrufen von Aktionen:</span><span class="sxs-lookup"><span data-stu-id="07e55-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="07e55-106">Die angegebene Aktion wird direkt mit der [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="07e55-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="07e55-107">Durch eine Aktion der obersten Ebene wird die Sequenz Tabelle aufgerufen, die die benutzerdefinierte Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="07e55-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="07e55-108">Weitere Informationen zum Planen einer benutzerdefinierten Aktion in einer Sequenz Tabelle finden Sie unter [Sequenzieren von benutzerdefinierten Aktionen](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="07e55-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="07e55-109">Wenn das Installationsprogramm einen Aktions Namen aus der [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion oder aus einer Sequenz Tabelle erhält, sucht er zuerst nach einer Standardaktion mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="07e55-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="07e55-110">Wenn die Standardaktion nicht gefunden werden kann, fragt das Installationsprogramm die [Tabelle CustomAction](customaction-table.md) ab, um zu überprüfen, ob die angegebene Aktion eine benutzerdefinierte Aktion ist.</span><span class="sxs-lookup"><span data-stu-id="07e55-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="07e55-111">Wenn es sich bei der angegebenen Aktion nicht um eine benutzerdefinierte Aktion handelt, fragt das Installationsprogramm die [Dialogfeld Tabelle](dialog-table.md) nach einem Dialogfeld ab.</span><span class="sxs-lookup"><span data-stu-id="07e55-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



