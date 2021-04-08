---
description: Die standardmäßige Warteschlangen Rückruf Routine verarbeitet von setupcommitfilequeue gesendete Benachrichtigungen auf generische Weise.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Informationen zur Standard Warteschlangen Rückruf-Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862379"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="f05e6-103">Informationen zur Standard Warteschlangen Rückruf-Routine</span><span class="sxs-lookup"><span data-stu-id="f05e6-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="f05e6-104">Die standardmäßige Warteschlangen Rückruf Routine verarbeitet von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gesendete Benachrichtigungen auf generische Weise.</span><span class="sxs-lookup"><span data-stu-id="f05e6-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="f05e6-105">Wenn Sie die Standard Routine verwenden, erhalten Sie eine vorgefertigte Benutzeroberfläche, um allgemeine Setup Dialogfelder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f05e6-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="f05e6-106">Es wird empfohlen, dass Sie die standardmäßige Warteschlangen Rückruf Routine verwenden, um die Benutzerfreundlichkeit zu vereinfachen und eine konsistente Darstellung und das Verhalten von Dialogfeldern sicherzustellen, die während der Installation generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f05e6-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="f05e6-107">Die Standard Rückruf Routine erfordert eine Kontext Struktur für die interne Daten Satz Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="f05e6-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="f05e6-108">Außerdem übergibt die Warteschlange zusätzliche Informationen, die für die aktuelle Benachrichtigung relevant sind, in einer Reihe von Parametern, *param1* und *Param2*.</span><span class="sxs-lookup"><span data-stu-id="f05e6-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="f05e6-109">Wenn die Warteschlange z. b. eine spfilenotify- \_ needmedia-Benachrichtigung an die standardmäßige Rückruf Routine sendet, verweist *param1* auf eine [**Quell \_ Medien**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) Struktur, die Informationen über das benötigte Medium enthält, und *Param2* verweist auf ein Zeichen Array, das neue Pfadinformationen vom Benutzer empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="f05e6-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="f05e6-110">Die Standard Rückruf Routine verwendet diese Informationen, um den Benutzer aufzufordern, entweder die erforderlichen Quell Medien einzufügen, einen neuen Pfad anzugeben, das Kopieren der aktuellen Datei zu überspringen oder den aktuellen Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="f05e6-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="f05e6-111">Die Standard Warteschlangen Rückruf-Routine gibt fileOp \_ NewPath, fileOp \_ doit, fileOp \_ Skip oder fileOp \_ Abbruch an die Warteschlange zurück, abhängig von der Aktion, die der Benutzer ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="f05e6-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="f05e6-112">Informationen dazu, wie die Standard Warteschlangen-Rückruf Routine jede Warteschlangen Benachrichtigung verarbeitet, finden Sie unter [Benachrichtigungen zu Datei Warteschlangen](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f05e6-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="f05e6-113">Informationen zu benutzerdefinierten Warteschlangen Rückruf Routinen finden Sie unter [Erstellen einer benutzerdefinierten Warteschlangen Rückruf-Routine](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="f05e6-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



