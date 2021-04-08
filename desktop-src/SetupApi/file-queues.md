---
description: Die Setup Funktionen umfassen Funktionen der Datei Warteschlange.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Datei Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960111"
---
# <a name="file-queues"></a><span data-ttu-id="685de-103">Datei Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="685de-103">File Queues</span></span>

<span data-ttu-id="685de-104">Die Setup Funktionen umfassen Funktionen der Datei Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="685de-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="685de-105">Eine Datei Warteschlange ist eine Liste von Datei Kopier-, Umbenennungs-und Lösch Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="685de-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="685de-106">Diese Vorgänge können in beliebiger Reihenfolge an die Warteschlange gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="685de-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="685de-107">Wenn für die Warteschlange ein Commit ausgeführt wird, werden diese Vorgänge in der Reihenfolge des Vorgangs Typs als Batch verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="685de-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="685de-108">In den folgenden Abschnitten wird erläutert, was eine Warteschlange ist und wie Sie beim Erstellen einer Setup Anwendung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="685de-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="685de-109">Außerdem wird die Reihenfolge erläutert, in der die in die Warteschlange eingereihten Datei Vorgänge in der Warteschlange verarbeitet werden, und die Benachrichtigungen, die die Warteschlange in jeder Phase an eine Rückruf Routine sendet.</span><span class="sxs-lookup"><span data-stu-id="685de-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="685de-110">Informationen zu Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="685de-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="685de-111">Verwenden von Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="685de-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="685de-112">Datei Warteschlangen Verweis</span><span class="sxs-lookup"><span data-stu-id="685de-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



