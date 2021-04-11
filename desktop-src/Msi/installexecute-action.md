---
description: Mit der InstallExecute-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder InstallExecuteAgain-Aktion enthält.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: InstallExecute-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128380"
---
# <a name="installexecute-action"></a><span data-ttu-id="88ad7-103">InstallExecute-Aktion</span><span class="sxs-lookup"><span data-stu-id="88ad7-103">InstallExecute Action</span></span>

<span data-ttu-id="88ad7-104">Mit der InstallExecute-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecute-Aktion oder [InstallExecuteAgain](installexecuteagain-action.md)-Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="88ad7-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="88ad7-105">Die InstallExecute-Aktion aktualisiert das System, ohne die Transaktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="88ad7-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="88ad7-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="88ad7-106">Sequence Restrictions</span></span>

<span data-ttu-id="88ad7-107">Die InstallExecute-Aktion erfolgt zwischen der Aktion [InstallInitialize](installinitialize-action.md) und der [InstallFinalize](installfinalize-action.md)-Aktion.</span><span class="sxs-lookup"><span data-stu-id="88ad7-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="88ad7-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="88ad7-108">ActionData Messages</span></span>

<span data-ttu-id="88ad7-109">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="88ad7-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ad7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88ad7-110">Remarks</span></span>

<span data-ttu-id="88ad7-111">Die [InstallExecuteAgain-Aktion](installexecuteagain-action.md) bewirkt dasselbe wie die InstallExecute-Aktion.</span><span class="sxs-lookup"><span data-stu-id="88ad7-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="88ad7-112">Da die Sequenz Tabellen nur über einen Primärschlüssel verfügen, kann die Aktionsspalte nicht in einer bestimmten Sequenz Tabelle wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="88ad7-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="88ad7-113">Es gibt zwei Aktionen, die dasselbe tun, InstallExecute und InstallExecuteAgain, in Fällen, in denen die Funktionalität von InstallExecute zweimal in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="88ad7-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="88ad7-114">Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="88ad7-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



