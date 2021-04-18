---
description: Die folgenden Benachrichtigungen werden von setupiteratecabinet gesendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter Benachrichtigungen.
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: CAB-Datei Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345042"
---
# <a name="cabinet-file-notifications"></a><span data-ttu-id="fadf3-104">CAB-Datei Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="fadf3-104">Cabinet File Notifications</span></span>

<span data-ttu-id="fadf3-105">Die folgenden Benachrichtigungen werden von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendet.</span><span class="sxs-lookup"><span data-stu-id="fadf3-105">The following notifications are sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="fadf3-106">Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter [Benachrichtigungen](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fadf3-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="fadf3-107">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="fadf3-107">Notification</span></span>                                                        | <span data-ttu-id="fadf3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fadf3-108">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="fadf3-109">**spfilenotifizieren von \_ fileextrahierung**</span><span class="sxs-lookup"><span data-stu-id="fadf3-109">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="fadf3-110">Die Datei wurde aus der CAB-Datei extrahiert.</span><span class="sxs-lookup"><span data-stu-id="fadf3-110">The file has been extracted from the cabinet.</span></span>                                  |
| [<span data-ttu-id="fadf3-111">**spfilenotify \_ filinput Cabinet**</span><span class="sxs-lookup"><span data-stu-id="fadf3-111">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="fadf3-112">Eine Datei ist in der CAB-Datei aufgetreten, von der Anwendung soll Sie extrahiert werden?</span><span class="sxs-lookup"><span data-stu-id="fadf3-112">A file is encountered in the cabinet, does the application want to extract it?</span></span> |
| [<span data-ttu-id="fadf3-113">**spfilenotify \_ neednewcabinet**</span><span class="sxs-lookup"><span data-stu-id="fadf3-113">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="fadf3-114">Die aktuelle Datei wird in der nächsten CAB-Datei fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fadf3-114">The current file is continued in the next cabinet.</span></span>                             |



 

 

 



