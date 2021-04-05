---
description: Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der Ausführung der InstallExecute-oder InstallExecuteAgain-Aktionen enthält.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: InstallFinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753520"
---
# <a name="installfinalize-action"></a><span data-ttu-id="3cffc-103">InstallFinalize-Aktion</span><span class="sxs-lookup"><span data-stu-id="3cffc-103">InstallFinalize Action</span></span>

<span data-ttu-id="3cffc-104">Die InstallFinalize-Aktion führt ein Skript aus, das alle Vorgänge in der Aktions Sequenz seit dem Start der Installation oder der Ausführung der [InstallExecute](installexecute-action.md) -oder [InstallExecuteAgain](installexecuteagain-action.md) -Aktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="3cffc-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="3cffc-105">Diese Aktion markiert das Ende einer Transaktion, die mit der [InstallInitialize](installinitialize-action.md) -Aktion beginnt.</span><span class="sxs-lookup"><span data-stu-id="3cffc-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3cffc-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3cffc-106">Sequence Restrictions</span></span>

<span data-ttu-id="3cffc-107">Die [InstallInitialize](installinitialize-action.md) -Aktion muss vor der InstallFinalize-Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="3cffc-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3cffc-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="3cffc-108">ActionData Messages</span></span>

<span data-ttu-id="3cffc-109">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3cffc-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cffc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cffc-110">Remarks</span></span>

<span data-ttu-id="3cffc-111">Wenn erkannt wird, dass das Produkt zum Abschluss der Löschung markiert ist, werden die Vorgänge automatisch dem Skript hinzugefügt, um die Software in den **System Steuerungs** Informationen für das Produkt zu entfernen, die Registrierung aufzuheben und die **Veröffentlichung aufzuheben und** die zwischengespeicherte lokale Datenbank aus% Windows% zu entfernen, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3cffc-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="3cffc-112">System Änderungen, die vor der Aktion vorgenommen wurden, werden möglicherweise nach dem Ausführen der Aktion "InstallFinalize" nicht wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="3cffc-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="3cffc-113">Die InstallFinalize-Aktion aktualisiert das System mit allen Vorgängen, die bis zu diesem Zeitpunkt festgelegt wurden, und beendet dann die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="3cffc-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



