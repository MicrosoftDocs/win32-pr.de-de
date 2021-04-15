---
description: Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der ExecuteAction-Eigenschaft, um zu bestimmen, welcher Installationstyp ausgeführt werden soll.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: ExecuteAction-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485387"
---
# <a name="executeaction-action"></a><span data-ttu-id="38dc5-103">ExecuteAction-Aktion</span><span class="sxs-lookup"><span data-stu-id="38dc5-103">ExecuteAction Action</span></span>

<span data-ttu-id="38dc5-104">Die ExecuteAction-Aktion initiiert die Ausführungssequenz mithilfe der [**ExecuteAction**](executeaction.md) -Eigenschaft, um zu bestimmen, welcher Installationstyp ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38dc5-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="38dc5-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="38dc5-105">Sequence Restrictions</span></span>

<span data-ttu-id="38dc5-106">Diese Aktion sollte nacheinander ausgeführt werden, nachdem alle für den Beginn der Installation erforderlichen Informationen zum Sammeln von Informationen vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="38dc5-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="38dc5-107">Weitere Aktionen können nach der ExecuteAction-Aktion in der [Tabelle "InstallUISequence](installuisequence-table.md)" und der [Tabelle "AdminUISequence](adminuisequence-table.md)" sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="38dc5-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="38dc5-108">Eine Sequenz beginnt in der Regel mit [*Kosten*](c-gly.md) Vorgängen, wie z. b. der [Aktion "costinitialize](costinitialize-action.md)", gefolgt von den Aktionen der Benutzeroberfläche und der ExecuteAction-Aktion.</span><span class="sxs-lookup"><span data-stu-id="38dc5-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="38dc5-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="38dc5-109">ActionData Messages</span></span>

<span data-ttu-id="38dc5-110">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="38dc5-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="38dc5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38dc5-111">Remarks</span></span>

<span data-ttu-id="38dc5-112">Die ExecuteAction-Aktion wird mit System Berechtigungen ausgeführt, wenn der Installer-Dienst aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="38dc5-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="38dc5-113">Die Aktionen der obersten Ebene, z. b. [Installations Aktion](install-action.md), Ankündigungs [Aktion](advertise-action.md)und [Administrator Aktion](admin-action.md) , enthalten interne Logik, die bestimmt, ob das Aufrufen der ExecuteAction-Aktion erfordert, dass entweder die Ausführungssequenz oder die Benutzeroberflächen Sequenz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38dc5-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38dc5-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38dc5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38dc5-115">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="38dc5-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="38dc5-116">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="38dc5-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="38dc5-117">Costinitialize-Aktion</span><span class="sxs-lookup"><span data-stu-id="38dc5-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



