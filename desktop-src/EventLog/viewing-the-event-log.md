---
description: Wenn der Benutzer Ereignisanzeige startet, um die Ereignisprotokoll Einträge anzuzeigen, ruft er die ReadEventLog-Funktion auf, um die EventLogRecord-Strukturen abzurufen.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Anzeigen des Ereignis Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215569"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="8a537-103">Anzeigen des Ereignis Protokolls</span><span class="sxs-lookup"><span data-stu-id="8a537-103">Viewing the Event Log</span></span>

<span data-ttu-id="8a537-104">Wenn der Benutzer Ereignisanzeige startet, um die Ereignisprotokoll Einträge anzuzeigen, ruft er die [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion auf, um die [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Strukturen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a537-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="8a537-105">Der Ereignisanzeige verwendet die Ereignis Quelle und den Ereignis Bezeichner, um den Nachrichtentext für jedes Ereignis aus der registrierten Nachrichtendatei (angegeben durch den **EventMessageFile** -Registrierungs Wert für die Quelle) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a537-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="8a537-106">Der Ereignisanzeige verwendet die [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) -Funktion, um die Nachrichtendatei zu laden.</span><span class="sxs-lookup"><span data-stu-id="8a537-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="8a537-107">Der Ereignisanzeige verwendet dann die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion, um die Basis Beschreibungs Zeichenfolge aus dem geladenen Modul abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a537-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="8a537-108">Schließlich ersetzt das Ereignisanzeige die Einfügeparameter in der Basis Beschreibungs Zeichenfolge, um die endgültige Nachrichten Zeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a537-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
