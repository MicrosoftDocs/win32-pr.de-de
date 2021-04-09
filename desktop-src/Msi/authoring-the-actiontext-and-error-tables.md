---
description: Die Beispiel Spezifikationen umfassen das Senden von Action Data-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und meldet einen Fehler, wenn ein Konto nicht erstellt werden kann.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Erstellen der Aktions Text-und Fehler Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864452"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="93495-103">Erstellen der Aktions Text-und Fehler Tabellen</span><span class="sxs-lookup"><span data-stu-id="93495-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="93495-104">Die Beispiel Spezifikationen umfassen das Senden von Action Data-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und meldet einen Fehler, wenn ein Konto nicht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="93495-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="93495-105">Geben Sie die folgenden Einträge in die Tabelle "aktiontext" ein, um von den Aktions Textnachrichten verwendete Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93495-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="93495-106">Tabelle "aktiontext"</span><span class="sxs-lookup"><span data-stu-id="93495-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="93495-107">Aktion</span><span class="sxs-lookup"><span data-stu-id="93495-107">Action</span></span>            | <span data-ttu-id="93495-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93495-108">Description</span></span>                                                       | <span data-ttu-id="93495-109">Vorlage</span><span class="sxs-lookup"><span data-stu-id="93495-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="93495-110">Processaccounts</span><span class="sxs-lookup"><span data-stu-id="93495-110">ProcessAccounts</span></span>   | <span data-ttu-id="93495-111">Aktionen zum Erstellen von Benutzerkonten auf dem lokalen Computer werden erzeugt.</span><span class="sxs-lookup"><span data-stu-id="93495-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="93495-112">Konto: \[ 1 \] , Attribute: \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="93495-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="93495-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="93495-113">CreateAccount</span></span>     | <span data-ttu-id="93495-114">Das Benutzerkonto wird auf dem lokalen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="93495-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="93495-115">Konto: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="93495-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="93495-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="93495-116">RemoveAccount</span></span>     | <span data-ttu-id="93495-117">Das Benutzerkonto wird aus dem lokalen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="93495-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="93495-118">Konto: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="93495-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="93495-119">Rollbackaccount</span><span class="sxs-lookup"><span data-stu-id="93495-119">RollbackAccount</span></span>   | <span data-ttu-id="93495-120">Rollback der Erstellung von Benutzerkonten auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="93495-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="93495-121">Konto: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="93495-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="93495-122">Nicht installaccounts</span><span class="sxs-lookup"><span data-stu-id="93495-122">UninstallAccounts</span></span> | <span data-ttu-id="93495-123">Aktionen zum Entfernen von Benutzerkonten auf dem lokalen Computer werden erzeugt.</span><span class="sxs-lookup"><span data-stu-id="93495-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="93495-124">Konto: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="93495-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="93495-125">Geben Sie die folgenden Einträge in die Fehler Tabelle ein, um die von der Fehlerberichterstattung verwendeten Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="93495-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="93495-126">Fehler Tabelle</span><span class="sxs-lookup"><span data-stu-id="93495-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="93495-127">Fehler</span><span class="sxs-lookup"><span data-stu-id="93495-127">Error</span></span> | <span data-ttu-id="93495-128">`Message`</span><span class="sxs-lookup"><span data-stu-id="93495-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="93495-129">25001</span><span class="sxs-lookup"><span data-stu-id="93495-129">25001</span></span> | <span data-ttu-id="93495-130">Das Benutzerkonto " \[ 2" kann nicht \] auf dem lokalen Computer erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="93495-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="93495-131">Fehler Code: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="93495-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="93495-132">25002</span><span class="sxs-lookup"><span data-stu-id="93495-132">25002</span></span> | <span data-ttu-id="93495-133">Das Benutzerkonto " \[ 2 \] " ist bereits auf dem lokalen Computer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93495-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="93495-134">25003</span><span class="sxs-lookup"><span data-stu-id="93495-134">25003</span></span> | <span data-ttu-id="93495-135">Das Benutzerkonto " \[ 2 \] " auf dem lokalen Computer kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="93495-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="93495-136">Fehler Code: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="93495-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="93495-137">25004</span><span class="sxs-lookup"><span data-stu-id="93495-137">25004</span></span> | <span data-ttu-id="93495-138">Das Benutzerkonto " \[ 2 \] " ist auf dem lokalen Computer nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93495-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="93495-139">Fahren Sie mit [dem Erstellen der InstallExecuteSequence-Tabelle](authoring-the-installexecutesequence-table.md)fort.</span><span class="sxs-lookup"><span data-stu-id="93495-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



