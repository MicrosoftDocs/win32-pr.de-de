---
description: In den Setup Funktionen ist eine standardmäßige Rückruf Routine, setupdefaultqueuecallback, enthalten, die Sie zum Verarbeiten von Benachrichtigungen verwenden können, die von setupcommitfilequeue zurückgegeben werden.
ms.assetid: c6ba6398-4119-4bdd-b264-1bc645800b03
title: Standard Warteschlangen-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad7b192ca19a652a948f5884a9ae97295de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373155"
---
# <a name="default-queue-callback-routine"></a><span data-ttu-id="06087-103">Standard Warteschlangen-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="06087-103">Default Queue Callback Routine</span></span>

<span data-ttu-id="06087-104">In den Setup Funktionen ist eine standardmäßige Rückruf Routine, [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), enthalten, die Sie zum Verarbeiten von Benachrichtigungen verwenden können, die von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06087-104">Included with the setup functions is a default callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), that you can use to process notifications returned by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea).</span></span>

<span data-ttu-id="06087-105">In den folgenden Abschnitten wird das Format der Standard Warteschlangen Rückruf Routine erläutert. dabei wird die Standard Warteschlangen-Rückruf Routine mit [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)verwendet, und es wird beschrieben, wie eine Filter Rückruf Routine erstellt wird, die auf der Funktionalität basiert, die von der standardmäßigen Warteschlangen Rückruf-Routine</span><span class="sxs-lookup"><span data-stu-id="06087-105">The following sections discuss the format of the default queue callback routine, using the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), and how to create a filter callback routine that builds on the functionality provided by the default queue callback routine.</span></span>

-   [<span data-ttu-id="06087-106">Informationen zur Standard Warteschlangen Rückruf-Routine</span><span class="sxs-lookup"><span data-stu-id="06087-106">About the Default Queue Callback Routine</span></span>](about-the-default-queue-callback-routine.md)
-   [<span data-ttu-id="06087-107">Verwenden der Standard Warteschlangen-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="06087-107">Using the Default Queue Callback Routine</span></span>](using-the-default-queue-callback-routine.md)
-   [<span data-ttu-id="06087-108">Standard Verweis für Warteschlangen Rückruf-Routine</span><span class="sxs-lookup"><span data-stu-id="06087-108">Default Queue Callback Routine Reference</span></span>](default-queue-callback-routine-reference.md)

 

 



