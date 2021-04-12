---
description: Mit der Ereignisprotokollierung für das Herunterfahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345708"
---
# <a name="shutdown-event-tracker"></a>Ereignisprotokollierung

Mit der Ereignisprotokollierung für das *herunter* fahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren. Der Benutzer wird aufgefordert, Informationen einzugeben, wenn Sie im **Startmenü** **herunter** fahren oder Shutdown.exe verwenden. Entwickler können einen Grund Code beim Aufrufen der Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) einschließen. Die Informationen werden im Ereignisprotokoll gespeichert.

**Windows XP:** Diese Funktion ist zwar standardmäßig ab Windows Server 2003 aktiviert, aber Sie müssen Sie unter Windows XP aktivieren. Weitere Informationen finden Sie in der Dokumentation für das Herunterfahren der Ereignisprotokollierung, die im System oder auf TechNet enthalten ist.

Die Funktionen " [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) " und " [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) " wurden aktualisiert, um die Ursache für das Herunterfahren im *dwReason* -Parameter zu unterstützen. Verwenden Sie die Werte, die in Reason. h definiert sind, um den Grund für das Herunterfahren zu erstellen, oder definieren Sie einen benutzerdefinierten Grund Der Grund für das Herunterfahren wird aus einem hauptflag, einem nebenflag und zwei optionalen Flags erstellt. Weitere Informationen finden Sie unter [Grund Codes](system-shutdown-reason-codes.md)für das Herunterfahren des Systems.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignisprotokollierung für Herunterfahren (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
