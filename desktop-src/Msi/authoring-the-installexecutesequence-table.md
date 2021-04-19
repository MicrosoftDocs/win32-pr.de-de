---
description: Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts generieren die verzögerten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder zurücksetzen.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Erstellen der InstallExecuteSequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358852"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="0d9c7-103">Erstellen der InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0d9c7-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="0d9c7-104">Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts generieren die verzögerten benutzerdefinierten Aktionen, die Benutzerkonten erstellen, entfernen oder zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="0d9c7-105">Die benutzerdefinierten Aktionen processaccounts und uninstallaccounts müssen in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) eingegeben werden, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="0d9c7-106">Fügen Sie die folgenden Einträge der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="0d9c7-107">Da diese benutzerdefinierten Aktionen Teil der Skript Generierung sein müssen, müssen beide benutzerdefinierten Aktionen nach der [InstallInitialize-Aktion](installinitialize-action.md)sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="0d9c7-108">Die Bedingung für processaccounts stellt Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="0d9c7-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="0d9c7-109">Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="0d9c7-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="0d9c7-110">Processaccounts wird nur ausgeführt, wenn die Komponente Testaccount lokal auf dem Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="0d9c7-111">Das Komponenten Test Konto ist zurzeit nicht installiert oder wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="0d9c7-112">Die Bedingung für uninstallaccount stellt Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="0d9c7-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="0d9c7-113">Uninstallaccounts werden nur ausgeführt, wenn die Komponente Testaccount lokal auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="0d9c7-114">Das Komponenten Test Konto wird entfernt oder zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="0d9c7-115">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0d9c7-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="0d9c7-116">Aktion</span><span class="sxs-lookup"><span data-stu-id="0d9c7-116">Action</span></span>            | <span data-ttu-id="0d9c7-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="0d9c7-117">Condition</span></span>                                                           | <span data-ttu-id="0d9c7-118">Sequenz</span><span class="sxs-lookup"><span data-stu-id="0d9c7-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="0d9c7-119">Processaccounts</span><span class="sxs-lookup"><span data-stu-id="0d9c7-119">ProcessAccounts</span></span>   | <span data-ttu-id="0d9c7-120">VersionNT und (? Testaccount = 2 oder? Testaccount = 4) und $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="0d9c7-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="0d9c7-121">1550</span><span class="sxs-lookup"><span data-stu-id="0d9c7-121">1550</span></span>     |
| <span data-ttu-id="0d9c7-122">Nicht installaccounts</span><span class="sxs-lookup"><span data-stu-id="0d9c7-122">UninstallAccounts</span></span> | <span data-ttu-id="0d9c7-123">VersionNT und? Testaccount = 3 und ($TestAccount = 4 oder $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="0d9c7-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="0d9c7-124">1560</span><span class="sxs-lookup"><span data-stu-id="0d9c7-124">1560</span></span>     |



 

<span data-ttu-id="0d9c7-125">Erstellen Sie [die Benutzeroberfläche für die Kenn Wort Eingabe](authoring-the-user-interface-for-password-input.md)weiter.</span><span class="sxs-lookup"><span data-stu-id="0d9c7-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



