---
description: Bevor Sie Datei Vorgänge in die Warteschlange stellen können, müssen Sie eine Datei Warteschlange öffnen. Durch Aufrufen der setupopenfilequeue-Funktion wird ein Handle für eine Warteschlangen Datei zurückgegeben. Dieses Handle wird von nachfolgenden Warteschlangen Funktionen verwendet, um auf die geöffnete Warteschlange zu verweisen und Vorgänge hinzuzufügen oder Sie zu scannen.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Öffnen und Schließen einer Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357922"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="7954a-105">Öffnen und Schließen einer Warteschlange</span><span class="sxs-lookup"><span data-stu-id="7954a-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="7954a-106">Bevor Sie Datei Vorgänge in die Warteschlange stellen können, müssen Sie eine Datei Warteschlange öffnen.</span><span class="sxs-lookup"><span data-stu-id="7954a-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="7954a-107">Durch Aufrufen der [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion wird ein Handle für eine Warteschlangen Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7954a-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="7954a-108">Dieses Handle wird von nachfolgenden Warteschlangen Funktionen verwendet, um auf die geöffnete Warteschlange zu verweisen und Vorgänge hinzuzufügen oder Sie zu scannen.</span><span class="sxs-lookup"><span data-stu-id="7954a-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="7954a-109">Nachdem alle angegebenen Datei Vorgänge in die Warteschlange eingereiht und ein Commit ausgeführt wurden, müssen Sie die Funktion [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) aufrufen, um beim Aufrufen von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)zugeordnete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7954a-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="7954a-110">Die Funktion " [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) " führt keinen Commit für die Datei Warteschlange aus.</span><span class="sxs-lookup"><span data-stu-id="7954a-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="7954a-111">Alle Vorgänge, für die ein Commit ausgeführt wird, wenn **setupclosefilequeue** aufgerufen wird, werden nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7954a-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



