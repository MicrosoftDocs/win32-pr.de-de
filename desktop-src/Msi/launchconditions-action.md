---
description: Mit der LaunchConditions-Aktion wird die LaunchCondition-Tabelle abgefragt und jede aufgezeichnete bedingte Anweisung ausgewertet. Wenn eine dieser Bedingungs Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: LaunchConditions-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350449"
---
# <a name="launchconditions-action"></a><span data-ttu-id="7e7cb-104">LaunchConditions-Aktion</span><span class="sxs-lookup"><span data-stu-id="7e7cb-104">LaunchConditions Action</span></span>

<span data-ttu-id="7e7cb-105">Mit der LaunchConditions-Aktion wird die [LaunchCondition-Tabelle](launchcondition-table.md) abgefragt und jede aufgezeichnete bedingte Anweisung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="7e7cb-106">Wenn eine dieser Bedingungs Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7e7cb-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7e7cb-107">Sequence Restrictions</span></span>

<span data-ttu-id="7e7cb-108">Die Aktion "LaunchConditions" ist optional.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="7e7cb-109">Diese Aktion ist normalerweise die erste in der Sequenz, aber die [AppSearch-Aktion](appsearch-action.md) kann vor der Aktion "LaunchConditions" sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="7e7cb-110">Wenn Startbedingungen nicht auf alle Installations Modi zutreffen, sollte die entsprechende Eigenschaft für den Installationsmodus in einem bedingten Ausdruck in der entsprechenden Sequenz Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7e7cb-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="7e7cb-111">ActionData Messages</span></span>

<span data-ttu-id="7e7cb-112">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7e7cb-112">There are no ActionData messages.</span></span>

 

 



