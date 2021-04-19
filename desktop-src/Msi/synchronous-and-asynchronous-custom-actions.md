---
description: Der Windows Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Haupt Installation.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Synchrone und asynchrone benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372896"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="98ed7-103">Synchrone und asynchrone benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="98ed7-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="98ed7-104">Der Windows Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Haupt Installation.</span><span class="sxs-lookup"><span data-stu-id="98ed7-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="98ed7-105">Beim synchronen Ausführen einer benutzerdefinierten Aktion wartet das Installationsprogramm darauf, dass der Thread der benutzerdefinierten Aktion vollständig ausgeführt wird, bevor die Haupt Installation fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="98ed7-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="98ed7-106">Während der asynchronen Ausführung führt das Installationsprogramm die benutzerdefinierte Aktion gleichzeitig aus, da die aktuelle Installation fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="98ed7-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="98ed7-107">Autoren benutzerdefinierter Aktionen müssen daher alle asynchronen Threads beachten, die möglicherweise Änderungen an der Installations Datenbank zwischen Funktionsaufrufen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="98ed7-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="98ed7-108">Insbesondere sollten Aufrufe von [**msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) und [**msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) in asynchronen benutzerdefinierten Aktionen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="98ed7-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="98ed7-109">Verwenden Sie stattdessen [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) zum Abrufen eines Zielpfads.</span><span class="sxs-lookup"><span data-stu-id="98ed7-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="98ed7-110">Massendaten Bank Vorgänge, z. b. Import-, Export-und Transformations Vorgänge, sollten in jeder Art von benutzerdefinierter Aktion vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="98ed7-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="98ed7-111">Optionsflags können im type-Feld der [CustomAction-Tabelle](customaction-table.md) festgelegt werden, um anzugeben, dass die Haupt-und benutzerdefinierten aktionsthreads synchron oder asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="98ed7-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="98ed7-112">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="98ed7-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="98ed7-113">Das Installationsprogramm kann [benutzerdefinierte Rollbacks-Aktionen](rollback-custom-actions.md) und [gleichzeitige Installations](concurrent-installations.md) Aktionen nur als synchrone benutzerdefinierte Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="98ed7-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 



