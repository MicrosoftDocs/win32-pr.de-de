---
description: Eine Datei Warteschlange ist eine Liste von Datei Vorgängen, die gleichzeitig verarbeitet werden. Die Datei Vorgänge in der Warteschlange sind möglicherweise Kopier-, Umbenennungs-oder Löschvorgänge. Die Datei Warteschlange organisiert Datei Vorgänge nach Typ, das Kopieren, umbenennen und Löschen von unter Warteschlangen.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Informationen zu Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348762"
---
# <a name="about-file-queues"></a><span data-ttu-id="bcfaf-105">Informationen zu Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="bcfaf-105">About File Queues</span></span>

<span data-ttu-id="bcfaf-106">Eine Datei Warteschlange ist eine Liste von Datei Vorgängen, die gleichzeitig verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="bcfaf-107">Die Datei Vorgänge in der Warteschlange sind möglicherweise Kopier-, Umbenennungs-oder Löschvorgänge.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="bcfaf-108">Die Datei Warteschlange organisiert Datei Vorgänge nach Typ, das Kopieren, umbenennen und Löschen von unter Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="bcfaf-109">Diese Vorgänge können in beliebiger Reihenfolge an die Warteschlange gesendet werden, und der in die Warteschlange eingereihte Prozess muss nicht zusammenhängend sein.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="bcfaf-110">Wenn für die Warteschlange ein Commit ausgeführt wird, führt die [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion Datei Vorgänge in der Reihenfolge des Vorgangs Typs aus.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="bcfaf-111">Normalerweise werden alle für eine gesamte Installation erforderlichen Datei Vorgänge in die Warteschlange eingereiht und dann in einem einzelnen Batch verarbeitet, wenn ein Commit für die Warteschlange ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="bcfaf-112">Der Vorteil, dass Datei Vorgänge in der Warteschlange über die Installation von Dateien in einer INF-Datei durchgeführt werden, besteht darin, den Installationsvorgang zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="bcfaf-113">Anstatt für jeden zu installierenden Abschnitt Informationen vom Benutzer abrufen zu müssen, können Sie beim Aufbau der Warteschlange Installationsinformationen vom Benutzer abrufen, damit alle Dateien installiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="bcfaf-114">Dadurch wird der Benutzer zur Verfolgung anderer Aktivitäten freigegeben, während die zeitintensiven Kopiervorgänge von der [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) -Funktion verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="bcfaf-115">Ein weiterer Vorteil von Datei Warteschlangen besteht darin, dass Sie den Fortschritt der Installation als Ganzes verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="bcfaf-116">Bei der Installation von "section-by-Section" aus einer INF-Datei können Status Indikatoren wie z. b. Status anzeigen nur den aktuellen INF-Abschnitt nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="bcfaf-117">Wenn der nächste Abschnitt installiert ist, beginnt die Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="bcfaf-118">Bei einer Warteschlange ist die Gesamtanzahl der Dateien, die während der gesamten Installation verarbeitet werden müssen, bekannt, bevor ein Commit für die Warteschlange ausgeführt wird. auf diese Weise kann eine Statusanzeige generiert werden, um die gesamte Installation zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="bcfaf-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="bcfaf-119">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="bcfaf-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="bcfaf-120">Reihenfolge der Warteschlangen Verpflichtung</span><span class="sxs-lookup"><span data-stu-id="bcfaf-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="bcfaf-121">Warteschlangen Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bcfaf-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



