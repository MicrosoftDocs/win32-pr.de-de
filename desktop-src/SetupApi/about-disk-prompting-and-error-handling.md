---
description: Setup Funktionen können Dialogfelder generieren, um häufige Installationssituationen zu behandeln und Informationen vom Benutzer zu erfassen.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: Informationen zu Datenträger-und Fehlerbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6c171d1e479d5d16198ba6d632848ff152f4ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347738"
---
# <a name="about-disk-prompting-and-error-handling"></a>Informationen zu Datenträger-und Fehlerbehandlung

Obwohl die Setup Funktionen keine Benutzeroberfläche bereitstellen, gibt es vier Setup Funktionen, die Dialogfelder generieren, um häufige Installationssituationen zu behandeln und Informationen vom Benutzer zu erfassen. Dies sind: [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**setupcopyerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**setuprenameerror**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)und [**setupdeleteerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Rückruf Routinen können diese Funktionen aufrufen, um Dialogfelder zu erstellen, die bei der Verarbeitung von Benachrichtigungen helfen, die von anderen Setup Funktionen wie [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) und [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)gesendet werden.

Die [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) -Funktion fordert den Benutzer auf, Wechselmedien einzufügen, einen neuen Quellpfad anzugeben oder die Installation abzubrechen. Die Anwendung kann dem Benutzer zusätzliche Optionen anbieten, abhängig von den Flags, die beim Aufrufen der Funktion angegeben werden. Dazu gehört das Überspringen der aktuellen Datei oder das Suchen nach einem neuen Quellpfad.

Die drei Funktionen [**setupcopyerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**setuprenameerror**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)und [**setupdeleteerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)erstellen Dialogfelder, die mit dem Benutzer interagieren, um Informationen vom Benutzer zu sammeln, wenn ein Fehler aufgetreten ist.

Die [**setupcopyerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) -Funktion generiert ein Dialogfeld, in dem der Benutzer gefragt wird, wie nach einem Kopierfehler eine Wiederherstellung durchführt. Der Benutzer kann einen neuen Quellpfad für den Kopiervorgang angeben oder die Installation abbrechen. Abhängig von den Flags, die während des Aufrufes **setupcopyerror** angegeben wurden, kann der Benutzer möglicherweise auch nach einem neuen Quellpfad suchen, Fehlerdetails anzeigen oder die aktuelle Datei überspringen.

Ein Dialogfeld, in dem der Benutzer gefragt wird, wie Fehler verarbeitet werden können, die während eines Datei Umbenennungs Vorgangs auftreten, können durch Aufrufen von [**setuprenameerror**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)generiert werden. In diesem Dialogfeld hat der Benutzer die Möglichkeit, den Vorgang zu wiederholen, den aktuellen Umbenennungs Vorgang zu überspringen oder den Vorgang abzubrechen.

Die [**setupdeleteerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) -Funktion generiert ein Dialogfeld, in dem die Eingabe eines Fehlers erfasst werden kann, der während eines Datei Löschvorgangs aufgetreten ist. Der Benutzer erhält die Möglichkeit, den Vorgang zu wiederholen, den aktuellen Löschvorgang zu überspringen oder den Vorgang abzubrechen.

Die standardmäßige Warteschlangen Rückruf Routine [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)verwendet die zuvor erwähnten vier Funktionen, um Teile der Benutzeroberfläche zu generieren und Fehler zu behandeln und neue Medien einzugeben.

 

 



