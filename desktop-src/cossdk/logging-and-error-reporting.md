---
description: Protokollierung und Fehlerberichterstattung
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Protokollierung und Fehlerberichterstattung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341157"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="6670f-103">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="6670f-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="6670f-104">Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="6670f-104">Log file</span></span>

<span data-ttu-id="6670f-105">Comrepl generiert eine Protokolldatei mit Status-und Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="6670f-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="6670f-106">Diese Datei wird auf dem Computer gespeichert, auf dem Comrepl in% systemdir% \\ com \\ Replication \\ Comrepl. log gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="6670f-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="6670f-107">Diese Protokolldatei wird gelöscht, wenn eine Kopier Phase gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6670f-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="6670f-108">Die nachfolgende Installation der Ziele wird an die Datei angehängt.</span><span class="sxs-lookup"><span data-stu-id="6670f-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="6670f-109">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="6670f-109">Error handling</span></span>

<span data-ttu-id="6670f-110">Fehler werden in der oben beschriebenen Protokolldatei angegeben.</span><span class="sxs-lookup"><span data-stu-id="6670f-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="6670f-111">Ausführliche Fehlerinformationen finden Sie möglicherweise auch im Ereignisprotokoll auf Quell-oder Ziel Computern.</span><span class="sxs-lookup"><span data-stu-id="6670f-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6670f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6670f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6670f-113">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="6670f-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="6670f-114">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="6670f-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="6670f-115">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="6670f-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="6670f-116">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="6670f-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



