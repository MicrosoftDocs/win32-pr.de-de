---
description: Setupfunktionen können Dialogfelder generieren, um häufige Installationssituationen zu behandeln und Informationen vom Benutzer zu sammeln.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Informationen zur Datenträgeraufforderung und Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9aa7a43cc0efd81f066872a55cde20b66bb13d1c117153606f4b9fe2dd2e58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887963"
---
# <a name="about-disk-prompting-and-error-handling"></a>Informationen zur Datenträgeraufforderung und Fehlerbehandlung

Obwohl die Setupfunktionen keine Benutzeroberfläche bereitstellen, gibt es vier Setupfunktionen, die Dialogfelder generieren, um häufige Installationssituationen zu behandeln und Informationen vom Benutzer zu sammeln. Dies sind: [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)und [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Rückrufroutinen können diese Funktionen aufrufen, um Dialogfelder zu erstellen, die bei der Verarbeitung von Benachrichtigungen helfen, die von anderen Setupfunktionen wie [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) und [**SetupInstallFile gesendet werden.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)

Die [**SetupPromptForDisk-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) fordert den Benutzer auf, Wechselmedien einlegen, einen neuen Quellpfad anzugeben oder die Installation abzubricht. Die Anwendung kann dem Benutzer zusätzliche Optionen anbieten, abhängig von den Flags, die beim Aufgerufenen der Funktion angegeben werden. Dazu gehört das Überspringen der aktuellen Datei oder das Suchen nach einem neuen Quellpfad.

Die drei Funktionen [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)und [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)erstellen Dialogfelder, die mit dem Benutzer interagieren, um Informationen vom Benutzer zum Fortfahren zu sammeln, wenn ein Fehler aufgetreten ist.

Die [**Funktion SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) generiert ein Dialogfeld, in dem der Benutzer gefragt wird, wie er nach einem Kopierfehler wiederhergestellt werden soll. Der Benutzer kann einen neuen Quellpfad für den Kopiervorgang angeben oder die Installation abbrechen. Abhängig von den Flags, die während des Aufrufs von **SetupCopyError** angegeben wurden, kann der Benutzer möglicherweise auch nach einem neuen Quellpfad suchen, Fehlerdetails anzeigen oder die aktuelle Datei überspringen.

Ein Dialogfeld, in dem der Benutzer aufgefordert wird, Fehler zu verarbeiten, die während eines Datei-Umbenennungsvorgangs auftreten, kann durch Aufrufen von [**SetupRenameError generiert werden.**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora) Mit diesem Dialogfeld kann der Benutzer den Vorgang wiederholen, den aktuellen Umbenennungsvorgang überspringen oder abbrechen.

Die [**SetupDeleteError-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) generiert ein Dialogfeld, das eingaben kann, wie der Benutzer einen Fehler behandeln möchte, der während eines Dateilöschungsvorgang aufgetreten ist. Der Benutzer hat die Möglichkeit, den Vorgang erneut zu versuchen, den aktuellen Löschvorgang zu überspringen oder den Vorgang zu abbrechen.

Die Standardroutine für den Warteschlangenrückruf [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)verwendet die zuvor genannten vier Funktionen, um Teile der Benutzeroberfläche zu generieren und Fehler zu behandeln und neue Medien anfordern.

 

 



