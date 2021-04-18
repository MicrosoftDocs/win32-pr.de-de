---
description: Das Einreihen von Datei Vorgängen in der Warteschlange ist nützlich, da es Ihnen ermöglicht, die Installation als Ganzes anstelle des INF-Abschnitts zu verarbeiten.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Erstellen von Warteschlangen-und Warteschlangen Datei Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347437"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="1b2fd-103">Erstellen von Warteschlangen-und Warteschlangen Datei Vorgängen</span><span class="sxs-lookup"><span data-stu-id="1b2fd-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="1b2fd-104">Das Einreihen von Datei Vorgängen in der Warteschlange ist nützlich, da es Ihnen ermöglicht, die Installation als Ganzes anstelle des INF-Abschnitts zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="1b2fd-105">Zum Erstellen einer Datei Warteschlange deklarieren Sie eine Variable zum Speichern des Warteschlangen Handles, und rufen Sie dann die [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="1b2fd-106">Nachdem die Warteschlange erstellt wurde, können Sie Kopier-, Umbenennungs-und Löschvorgänge in die Warteschlange stellen und die Datei Warteschlange überprüfen, um in die Warteschlange eingereihte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="1b2fd-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="1b2fd-107">Verwenden Sie die Funktionen [**setupqueuecopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**setupqueuerename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)und [**setupqueuedelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) , um der Warteschlange einzelne Datei Vorgänge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="1b2fd-108">Alle Datei Vorgänge, die im Abschnitt **Kopieren von Dateien**, **Löschen von Dateien** oder **Umbenennen** von Dateien aufgelistet sind, können der Warteschlange mithilfe von [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**setupqueuedeletesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)bzw. [**setupqueuerenamesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="1b2fd-109">Eine weitere Möglichkeit, alle Dateien in den in einem **Installations** Abschnitt von inf aufgelisteten Dateien in der **Kopier Datei** in eine Warteschlange zu stellen, ist die Verwendung der Funktion [**setupinstallfilesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="1b2fd-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="1b2fd-110">Im folgenden Beispiel wird die [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) -Funktion verwendet, um Kopiervorgänge für alle Dateien in die Warteschlange zu stellen, die im Abschnitt **Kopieren von Dateien** einer INF-Datei aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="1b2fd-111">In dem Beispiel ist myQueue die Warteschlange zum Hinzufügen von Kopier Vorgängen, "A: \\ " gibt den Pfad zur Quelle an, und myinf ist das Handle der geöffneten INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="1b2fd-112">Der Parameter *listinfhandle* ist auf **null** festgelegt und gibt an, dass der Abschnitt zum Kopieren in myinf ist.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="1b2fd-113">MySection ist der Abschnitt in myinf, der die zu kopierenden Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="1b2fd-114">Die Flags SP \_ Copy \_ noSkip und SP \_ Copy \_ nobrowse wurden mit einem or-Operator kombiniert, um anzugeben, dass dem Benutzer keine Optionen angeboten werden sollten, um Dateien zu überspringen oder zu durchsuchen, wenn Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="1b2fd-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



