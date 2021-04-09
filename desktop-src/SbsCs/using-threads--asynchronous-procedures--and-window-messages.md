---
description: Aktivierungs Kontexte sind während des gesamten Prozesses sichtbar.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Threads, asynchrone Prozeduren und Fenster Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e615eb9795ba32bcf4bd227a4933e890e9b89055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862328"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Verwenden von Threads, asynchronen Prozeduren und Fenster Meldungen

Aktivierungs Kontexte sind während des gesamten Prozesses sichtbar. Die Aktivierungs Kontext Stapel sind jedoch pro Thread, und zwei Threads im gleichen Prozess können unterschiedliche Aktivierungs Stapel aufweisen. Der aktuelle Aktivierungs Kontext wird von [**kreatethread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) automatisch an den Anfang des Aktivierungs Stapels des neuen Threads eingefügt. Dies kann das Aktualisieren von vorhandenem Code für die Verwendung paralleler Komponenten vereinfachen, da der neue Thread sofort im aktuellen Aktivierungs Kontext ausgeführt werden kann.

Asynchrone Prozedur Aufrufe, Vervollständigungs Port Rückrufe und andere Rückrufe für andere Threads rufen automatisch den Aktivierungs Kontext der Quelle ab. Wenn der Rückruf aufgerufen wird, wird der Aktivierungs Stapel bereinigt. Dies bedeutet, dass Ihre Anwendung asynchrone Prozedur Aufrufe und Rückrufe verwenden kann, ohne explizit einen Kontext zu aktivieren, da die Kontext Verwaltung von der zugrunde liegenden parallelen Infrastruktur durchgeführt wird. Damit andere Kontexte während eines Rückrufs oder eines neuen Threads aktiv sind, kann Ihre Anwendung eine eigene Kontext Verwaltung durchführen. In diesem Fall muss das Programm die ordnungsgemäße Sequenz von Aktivierungs Kontext-Funktionen zum Aktivieren und Deaktivieren von Funktionen verwenden.

Aktivierungs Kontexte sind Thread neutral. Durch das Aktivieren eines Kontexts wird nur der Stapel des aktuellen Threads geändert, und es ist nicht möglich, einen Kontext Thread übergreifend zu aktivieren. Thread a kann einen Kontext auf Thread B nicht erzwingen. Die Funktionen der Aktivierungs Kontext-API sind ebenfalls Threading fähig.

Wenn Sie [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) oder [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) verwenden, um eine Fenster Nachricht an eine andere Fenster Prozedur in Ihrem Prozess zu senden, wird der aktuelle Aktivierungs Kontext aktiviert, bevor die Nachricht an die Ziel Prozedur weitergeleitet wird. Der aktuelle Aktivierungs Kontext wird zusammen mit der Nachricht angezeigt. Dadurch wird sichergestellt, dass Nachrichten, die auf COM-Objekte, DLL-Namen oder andere Seite-an-Seite-Ressourcen verweisen, ihre korrekten Kontextinformationen beibehalten.

 

 
