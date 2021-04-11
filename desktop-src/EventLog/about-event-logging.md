---
description: Wenn ein Fehler auftritt, muss der Systemadministrator oder der Supportmitarbeiter feststellen, was den Fehler verursacht hat. es muss versucht werden, verlorene Daten wiederherzustellen und den Fehler zu verhindern.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Informationen zur Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041843"
---
# <a name="about-event-logging"></a><span data-ttu-id="4eded-103">Informationen zur Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="4eded-103">About Event Logging</span></span>

<span data-ttu-id="4eded-104">Wenn ein Fehler auftritt, muss der Systemadministrator oder der Supportmitarbeiter feststellen, was den Fehler verursacht hat. es muss versucht werden, verlorene Daten wiederherzustellen und den Fehler zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4eded-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="4eded-105">Es ist hilfreich, wenn Anwendungen, das Betriebssystem und andere Systemdienste wichtige Ereignisse aufzeichnen, z. b. Bedingungen mit geringem Arbeitsspeicher oder übermäßig viele Zugriffsversuche auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4eded-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="4eded-106">Der Systemadministrator kann dann das Ereignisprotokoll verwenden, um zu bestimmen, welche Bedingungen den Fehler verursacht haben, und den Kontext zu identifizieren, in dem er aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4eded-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="4eded-107">Wenn Sie das Ereignisprotokoll in regelmäßigen Abständen anzeigen, kann der Systemadministrator möglicherweise Probleme erkennen (z. b. eine fehlerhafte Festplatte), bevor diese Schaden anrichten.</span><span class="sxs-lookup"><span data-stu-id="4eded-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="4eded-108">Die Ereignis Protokollierungs-API wurde für Anwendungen entwickelt, die auf dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4eded-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="4eded-109">In Windows Vista wurde die Infrastruktur zur Ereignisprotokollierung umgestaltet.</span><span class="sxs-lookup"><span data-stu-id="4eded-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="4eded-110">Anwendungen, die für die Betriebssysteme Windows Vista oder höher entwickelt wurden, sollten jetzt das [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) verwenden, um Ereignisse zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="4eded-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="4eded-111">In diesem Abschnitt wird die Programmierschnittstelle zum Schreiben und Verarbeiten von Ereignissen mithilfe der Ereignisprotokollierung erläutert.</span><span class="sxs-lookup"><span data-stu-id="4eded-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="4eded-112">Ereignistypen</span><span class="sxs-lookup"><span data-stu-id="4eded-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="4eded-113">Protokollierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4eded-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="4eded-114">Ereignis Protokollierungs Elemente</span><span class="sxs-lookup"><span data-stu-id="4eded-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="4eded-115">Ereignis Protokollierungs Vorgänge</span><span class="sxs-lookup"><span data-stu-id="4eded-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="4eded-116">Ereignis Protokollierungs Modell</span><span class="sxs-lookup"><span data-stu-id="4eded-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="4eded-117">Sicherheit der Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="4eded-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="4eded-118">Anwendungen, die Ereignisse veröffentlichen, die auf einem Computer mit Windows Server 2003, Windows XP oder Windows 2000 mehr als 64 Kilobyte haben, können Ereignisse auf Computern mit Windows Vista oder höher nicht veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4eded-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
