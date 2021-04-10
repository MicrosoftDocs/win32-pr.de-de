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
# <a name="viewing-the-event-log"></a>Anzeigen des Ereignis Protokolls

Wenn der Benutzer Ereignisanzeige startet, um die Ereignisprotokoll Einträge anzuzeigen, ruft er die [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion auf, um die [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Strukturen abzurufen. Der Ereignisanzeige verwendet die Ereignis Quelle und den Ereignis Bezeichner, um den Nachrichtentext für jedes Ereignis aus der registrierten Nachrichtendatei (angegeben durch den **EventMessageFile** -Registrierungs Wert für die Quelle) zu erhalten. Der Ereignisanzeige verwendet die [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) -Funktion, um die Nachrichtendatei zu laden. Der Ereignisanzeige verwendet dann die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion, um die Basis Beschreibungs Zeichenfolge aus dem geladenen Modul abzurufen. Schließlich ersetzt das Ereignisanzeige die Einfügeparameter in der Basis Beschreibungs Zeichenfolge, um die endgültige Nachrichten Zeichenfolge zu erhalten.

 

 
