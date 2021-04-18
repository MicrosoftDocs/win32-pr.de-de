---
description: Viele Anwendungen erfassen Fehler und Ereignisse in proprietären Fehlerprotokollen, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Ereignisprotokollierung (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351464"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="397b5-103">Ereignisprotokollierung (Ereignisprotokollierung)</span><span class="sxs-lookup"><span data-stu-id="397b5-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="397b5-104">Viele Anwendungen erfassen Fehler und Ereignisse in proprietären Fehlerprotokollen, die jeweils über ein eigenes Format und eine eigene Benutzeroberfläche verfügen.</span><span class="sxs-lookup"><span data-stu-id="397b5-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="397b5-105">Daten aus unterschiedlichen Anwendungen können nicht einfach zu einem umfassenden Bericht zusammengeführt werden, sodass Systemadministratoren oder Supportmitarbeiter eine Vielzahl von Quellen überprüfen können, um Probleme zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="397b5-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="397b5-106">Die Ereignisprotokollierung stellt eine standardmäßige, zentralisierte Methode für Anwendungen (und das Betriebssystem) zum Aufzeichnen wichtiger Software-und Hardware Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="397b5-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="397b5-107">Der Ereignis Protokollierungs Dienst zeichnet Ereignisse aus verschiedenen Quellen auf und speichert Sie in einer einzelnen Sammlung, die als *Ereignisprotokoll* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="397b5-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="397b5-108">Der Ereignisanzeige ermöglicht Ihnen das Anzeigen von Protokollen. mithilfe der Programmierschnittstelle können Sie auch Protokolle überprüfen.</span><span class="sxs-lookup"><span data-stu-id="397b5-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="397b5-109">Informationen zur Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="397b5-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="397b5-110">Verwenden der Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="397b5-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="397b5-111">Referenz zur Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="397b5-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="397b5-112">Die Ereignis Protokollierungs-API wurde für Anwendungen entwickelt, die auf dem Betriebssystem Windows Server 2003, Windows XP oder Windows 2000 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="397b5-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="397b5-113">In Windows Vista wurde die Infrastruktur zur Ereignisprotokollierung umgestaltet.</span><span class="sxs-lookup"><span data-stu-id="397b5-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="397b5-114">Anwendungen, die für die Betriebssysteme Windows Vista oder höher entwickelt wurden, sollten Ereignisse mit dem [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) protokollieren.</span><span class="sxs-lookup"><span data-stu-id="397b5-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
