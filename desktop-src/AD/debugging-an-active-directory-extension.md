---
title: Debuggen einer Active Directory-Erweiterung
description: Die in diesem Thema dokumentierten Erweiterungen für das Microsoft Active Directory Directory-Dienst-Eigenschaften Blatt, das Kontextmenü und den Objekterstellungs-Assistenten werden als com-in-proc-Server implementiert.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038776"
---
# <a name="debugging-an-active-directory-extension"></a>Debuggen einer Active Directory-Erweiterung

Die in diesem Thema dokumentierten Erweiterungen für das Microsoft Active Directory Directory-Dienst-Eigenschaften Blatt, das Kontextmenü und den Objekterstellungs-Assistenten werden als com-in-proc-Server implementiert. Das heißt, jede Erweiterung ist eine DLL, die im Kontext des Host Prozesses ausgeführt wird. Um die Erweiterung zu debuggen, ist es erforderlich, die Erweiterung einer Anwendung zuzuordnen und die Anwendung in einem Debugger auszuführen.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Debuggen Active Directory in der Windows-Shell angezeigten Erweiterungen

Active Directory Erweiterungen, die in der Windows-Shell angezeigt werden, werden im Kontext des Explorer.exe Prozesses geladen. Diese Erweiterungen können wie eine standardshellerweiterung deentschlbelt werden. Weitere Informationen zum Debuggen von Shellerweiterungen finden Sie unter [Debuggen mit der Shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Debuggen Active Directory Erweiterungen, die im Active Directory MMC angezeigt werden Snap-Ins

Active Directory Erweiterungen, die im Active Directory Verwaltungs-MMC-Snap-Ins angezeigt werden, werden im Kontext der Microsoft Management Console geladen. Um eine Erweiterung zu debuggen, suchen Sie Mmc.exe auf dem lokalen System, und legen Sie fest, dass der Debugger diese als Anwendung für das Debugging verwendet. Auf den meisten Systemen befindet sich Mmc.exe im Windows-System Verzeichnis, z. b. "C: \\ Winnt \\ system32". Abhängig vom Debugger müssen Sie die Erweiterungs-DLL möglicherweise so festlegen, dass Sie auch vom Debugger geladen wird. Viele Debugger ermöglichen auch das Anfügen des Debugger an einen laufenden MMC-Prozess. Weitere Informationen finden Sie im Benutzerhandbuch für den Debugger.

Es kann praktisch sein, dass die MMC ein bestimmtes Snap-in automatisch lädt. Legen Sie zu diesem Zweck die Anwendungs Argumente auf den Pfad und den Dateinamen einer MSC-Datei fest. Dabei kann es sich entweder um eine vom System installierte MSC-Datei oder eine von Ihnen erstellte Datei handeln. Eine MSC-Datei kann erstellt werden, indem Sie die folgenden Schritte ausführen.

1.  Führen Sie Mmc.exe aus.
2.  Laden Sie das gewünschte Snap-in, indem Sie  -  im MMC-Menü Datei auf **Snap-in hinzufügen/entfernen** auswählen, und wählen Sie das gewünschte Snap-in aus.
3.  Speichern Sie die MSC-Datei, indem Sie im MMC-Menü **Datei**  -  **Speichern unter...** auswählen.

Wenn Sie keine Start-MSC-Datei festlegen, müssen Sie das gewünschte Snap-in manuell laden, wenn Sie die Anwendung im Debugger ausführen.

Wenn die Host Anwendung im Debugger ausgeführt wird, zeigt der Debugger möglicherweise eine Warnmeldung an, die besagt, dass die ausgestellte Anwendung keine Debugsymbole enthält. Dies ist zu erwarten und kann sicher ignoriert werden, da Sie die dll tatsächlich Debuggen, nicht die Host Anwendung.

In den meisten Fällen wird die Erweiterung erst aufgerufen, wenn der Benutzer eine Aktion ausführt, die bewirkt, dass die Erweiterung geladen und initialisiert wird. Wenn Sie z. b. eine Kontextmenüerweiterung Debuggen, die für Benutzer Objekte angezeigt wird, wird die Erweiterung erst geladen, wenn das Kontextmenü für ein Benutzerobjekt zum ersten Mal angezeigt wird.

Sie sollten jetzt in der Lage sein, Breakpoints festzulegen und die Debugausgabe anzuzeigen. Wenn die Erweiterung nicht geladen werden kann, legen Sie in der [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion der Erweiterung einen Haltepunkt fest. Wenn **DllGetClassObject** nicht aufgerufen wird, ist die Erweiterung wahrscheinlich nicht ordnungsgemäß registriert.

Wenn das Debuggen beendet ist, beenden Sie MMC, und der Debugger sollte normal entladen werden.

 

 