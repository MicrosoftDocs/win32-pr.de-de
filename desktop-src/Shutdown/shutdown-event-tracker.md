---
description: Mit der Ereignisnachverfolgung zum Herunterfahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2deaebde736ed2e0ba72f38e8849cf815b167da68fdddbecb92e713083699b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664360"
---
# <a name="shutdown-event-tracker"></a>Ereignisprotokollierung

Mit *der Ereignisnachverfolgung* zum Herunterfahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren. Der Benutzer wird beim Auswählen von **Herunterfahren** im **Startmenü** oder bei Verwendung von Shutdown.exe zur Eingabe von Informationen aufgefordert. Entwickler können beim Aufrufen der Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) einen Ursachencode einfügen. Die Informationen werden im Ereignisprotokoll gespeichert.

**Windows XP:** Obwohl dieses Feature ab Windows Server 2003 standardmäßig aktiviert ist, müssen Sie es auf Windows XP aktivieren. Weitere Informationen finden Sie in der Dokumentation für den Shutdown Event Tracker, der im System oder im TechNet enthalten ist.

Die Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) wurden aktualisiert, um Ursachencodes für das Herunterfahren im *dwReason-Parameter* zu unterstützen. Verwenden Sie die in Reason.h definierten Werte, um einen Grundcode zum Herunterfahren zu erstellen, oder definieren Sie einen benutzerdefinierten Ursachencode. Ein Grundcode zum Herunterfahren wird aus einem Hauptflag, einem Nebenflag und zwei optionalen Flags erstellt. Weitere Informationen finden Sie unter [Ursachencodes für das Herunterfahren](system-shutdown-reason-codes.md)des Systems.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
