---
description: Die standardmäßige Warteschlangen Rückruf-Routine kann angegeben werden, um Benachrichtigungen zu verarbeiten, die von setupcommitfilequeue gesendet werden, oder Sie kann von einer benutzerdefinierten Rückruf Routine aufgerufen werden, die auf der Funktionalität der Standard Warteschlangen-Rückruf Routine basiert.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Verwenden der Standard Warteschlangen-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347578"
---
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="6d930-103">Verwenden der Standard Warteschlangen-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="6d930-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="6d930-104">Die standardmäßige Warteschlangen Rückruf-Routine kann angegeben werden, um Benachrichtigungen zu verarbeiten, die von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)gesendet werden, oder Sie kann von einer benutzerdefinierten Rückruf Routine aufgerufen werden, die auf der Funktionalität der Standard Warteschlangen-Rückruf Routine basiert.</span><span class="sxs-lookup"><span data-stu-id="6d930-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="6d930-105">In den folgenden Abschnitten wird erläutert, wie Sie den Kontext initialisieren und beenden, der von einer Standard Warteschlangen-Rückruf Routine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d930-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="6d930-106">Außerdem wird beschrieben, wie die Standard Warteschlangen-Rückruf Routine mit [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) oder einer benutzerdefinierten Rückruf Routine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d930-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="6d930-107">Initialisieren und Beenden des Rückruf Kontexts</span><span class="sxs-lookup"><span data-stu-id="6d930-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="6d930-108">Aufrufen der Standard Warteschlangen-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="6d930-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



