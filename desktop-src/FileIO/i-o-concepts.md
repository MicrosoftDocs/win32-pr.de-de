---
description: Beschreibt grundlegende e/a-Konzepte.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: E/a-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353936"
---
# <a name="io-concepts"></a><span data-ttu-id="c87be-103">E/a-Konzepte</span><span class="sxs-lookup"><span data-stu-id="c87be-103">I/O Concepts</span></span>

<span data-ttu-id="c87be-104">Die folgenden e/a-Konzepte werden in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c87be-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c87be-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c87be-105">In this section</span></span>



| <span data-ttu-id="c87be-106">Thema</span><span class="sxs-lookup"><span data-stu-id="c87be-106">Topic</span></span>                                                                               | <span data-ttu-id="c87be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c87be-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c87be-108">Dateipufferung</span><span class="sxs-lookup"><span data-stu-id="c87be-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="c87be-109">Beschreibt Überlegungen zur Anwendungssteuerung der Datei Pufferung, auch bekannt als nicht gepufferte Dateieingabe/-Ausgabe (e/a).</span><span class="sxs-lookup"><span data-stu-id="c87be-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="c87be-110">Dateizwischenspeicherung</span><span class="sxs-lookup"><span data-stu-id="c87be-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="c87be-111">Windows speichert Datei Daten, die von Datenträgern gelesen und auf Datenträger geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c87be-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c87be-112">Synchrone und asynchrone e/a</span><span class="sxs-lookup"><span data-stu-id="c87be-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="c87be-113">Es gibt zwei Arten der Eingabe-/ausgabesynchronisierung (e/a): Synchrone e/a-Vorgänge und asynchrone e/a-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c87be-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="c87be-114">Asynchrone e/a-Vorgänge werden auch als überlappende e/a-Vorgänge bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c87be-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="c87be-115">Abbrechen von ausstehenden e/a-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="c87be-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="c87be-116">Benutzern das Abbrechen von e/a-Anforderungen, die langsam oder blockiert sind, kann die Benutzerfreundlichkeit und Stabilität Ihrer Anwendung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="c87be-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="c87be-117">Warn Bare e/a</span><span class="sxs-lookup"><span data-stu-id="c87be-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="c87be-118">Warn Bare e/a ist die Methode, mit der Anwendungsthreads asynchrone e/a-Anforderungen verarbeiten, wenn Sie sich in einem wartungstabellenzustand befinden.</span><span class="sxs-lookup"><span data-stu-id="c87be-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="c87be-119">E/a-Abschlussports</span><span class="sxs-lookup"><span data-stu-id="c87be-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="c87be-120">E/a-Abschlussports stellen ein effizientes Threading Modell für die Verarbeitung mehrerer asynchroner e/a-Anforderungen auf einem Multiprozessorsystem dar.</span><span class="sxs-lookup"><span data-stu-id="c87be-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




