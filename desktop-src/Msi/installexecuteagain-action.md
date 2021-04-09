---
description: Mit der InstallExecuteAgain-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecuteAgain-Aktion oder der letzten InstallExecute-Aktion enthält.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: InstallExecuteAgain-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958852"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="10b74-103">InstallExecuteAgain-Aktion</span><span class="sxs-lookup"><span data-stu-id="10b74-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="10b74-104">Mit der InstallExecuteAgain-Aktion wird ein Skript ausgeführt, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der letzten InstallExecuteAgain-Aktion oder der letzten [InstallExecute](installexecute-action.md)-Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="10b74-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="10b74-105">Die InstallExecute-Aktion aktualisiert das System, ohne die Transaktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="10b74-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="10b74-106">InstallExecuteAgain führt den gleichen Vorgang wie die [InstallExecute-Aktion](installexecute-action.md) aus, sollte jedoch nur nach InstallExecute verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10b74-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="10b74-107">InstallExecuteAgain sollte immer so festgelegt werden, dass Sie nicht während des Entfernens ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10b74-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="10b74-108">Weitere Informationen finden [Sie unter Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="10b74-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="10b74-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="10b74-109">Sequence Restrictions</span></span>

<span data-ttu-id="10b74-110">Die InstallExecute-Aktion erfolgt zwischen der Aktion [InstallInitialize](installinitialize-action.md) und der [InstallFinalize](installfinalize-action.md)-Aktion.</span><span class="sxs-lookup"><span data-stu-id="10b74-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="10b74-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="10b74-111">ActionData Messages</span></span>

<span data-ttu-id="10b74-112">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="10b74-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b74-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10b74-113">Remarks</span></span>

<span data-ttu-id="10b74-114">Die InstallExecuteAgain-Aktion bewirkt dasselbe wie die [InstallExecute-Aktion](installexecute-action.md).</span><span class="sxs-lookup"><span data-stu-id="10b74-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="10b74-115">Da die Sequenz Tabellen nur über einen Primärschlüssel verfügen, kann die Aktionsspalte nicht in einer bestimmten Sequenz Tabelle wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="10b74-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="10b74-116">Es gibt zwei Aktionen, die dasselbe tun, InstallExecute und InstallExecuteAgain, in Fällen, in denen die Funktionalität von InstallExecute zweimal in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="10b74-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="10b74-117">Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="10b74-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



