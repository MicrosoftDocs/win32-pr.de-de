---
description: Nachdem Sie durch Aufrufen der setupopenfilequeue-Funktion ein Handle für eine Datei Warteschlange erhalten haben, können Sie der Warteschlange Datei Vorgänge hinzufügen, entweder Datei-für-Datei oder alle Dateien in einem INF-Abschnitt in die Warteschlange stellen.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Warteschlangen Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865420"
---
# <a name="queuing-files"></a><span data-ttu-id="9a68c-103">Warteschlangen Dateien</span><span class="sxs-lookup"><span data-stu-id="9a68c-103">Queuing Files</span></span>

<span data-ttu-id="9a68c-104">Nachdem Sie durch Aufrufen der [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion ein Handle für eine Datei Warteschlange erhalten haben, können Sie der Warteschlange Datei Vorgänge hinzufügen, entweder Datei-für-Datei oder alle Dateien in einem INF-Abschnitt in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="9a68c-104">After you have obtained a handle to a file queue by calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function, you can add file operations to the queue, either file-by-file, or by queuing all the files in an INF section.</span></span>

<span data-ttu-id="9a68c-105">Wenn Sie der Datei Warteschlange einen Kopiervorgang für eine einzelne Datei hinzufügen möchten, rufen Sie die [**setupqueuecopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9a68c-105">To add a copy operation for an individual file to the file queue, call the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) function.</span></span> <span data-ttu-id="9a68c-106">Wenn Sie einen Datei Kopiervorgang mithilfe der in einer INF-Datei angegebenen standardmäßigen Quell Medien und Ziel Ziele in die Warteschlange stellen möchten, können Sie die [**setupqueuedefaultcopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a68c-106">If you want to queue a file copy operation using the default source media and target destinations specified in an INF file, you can call the [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) function.</span></span>

<span data-ttu-id="9a68c-107">Durch Aufrufen der Funktion [**setupqueuedelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) oder [**setupqueuerename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) können Sie der geöffneten Datei Warteschlange einen einzelnen Vorgang zum Löschen oder Umbenennen einer Datei hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9a68c-107">You can add an individual file delete or rename operation to the open file queue, by calling the [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) or [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) function.</span></span>

 

 



