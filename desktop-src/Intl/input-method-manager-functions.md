---
description: In diesem Abschnitt werden die Funktionen von "imm" beschrieben.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Eingabemethoden-Manager-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516a83e207434f5d8c2e073e770c878198bc98e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357795"
---
# <a name="input-method-manager-functions"></a>Eingabemethoden-Manager-Funktionen

In diesem Abschnitt werden die Funktionen von "imm" beschrieben.



| Funktion                                                           | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateifecommoninstance"**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Gibt einen Zeiger auf eine [**ifecommon**](/windows/desktop/api/Msime/nn-msime-ifecommon) -Schnittstelle zurück.                                                          |
| [**"Kreateifedifiaryinstance"**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Gibt einen Zeiger auf eine [**ifedictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary) -Schnittstelle zurück.                                                  |
| [**"Kreateifelanguageinstance"**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Gibt einen Zeiger auf eine [**ifelanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage) -Schnittstelle zurück.                                                      |
| [**Enuminputcontext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Eine Anwendungs definierte Rückruffunktion, die die von der Funktion " **immeneninputcontext** " bereitgestellten Eingabe Kontexte verarbeitet.   |
| [**Enumregisterwordproc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Eine von der Anwendung definierte Rückruffunktion, die mit der Funktion " **immenenregisterword** " verwendet wird.                                   |
| [**Immassociatecontext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Ordnet den angegebenen Eingabe Kontext dem angegebenen Fenster zu.                                                          |
| [**Immassociatecontextex**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Ändert die Zuordnung zwischen dem Eingabemethoden Kontext und dem angegebenen Fenster oder seinen untergeordneten Elementen.                         |
| [**Immconfigureime**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Zeigt das Konfigurations Dialogfeld für den IME des angegebenen Eingabe Gebiets Schema Bezeichners an.                                |
| [**Immkreatecontext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Erstellt einen neuen Eingabe Kontext, wobei der Arbeitsspeicher für den Kontext reserviert und initialisiert wird.                                        |
| [**Immdestroycontext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Gibt den Eingabe kontextfrei und gibt zugeordneten Speicher frei.                                                                    |
| [**Immdisableime**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Deaktiviert den IME für einen Thread oder für alle Threads in einem Prozess.                                                             |
| [**Immdisablelegacyime**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Gibt an, dass dieser Thread ein UI-Thread für Windows Store-Apps ist.                                                               |
| [**Immdisabletextframeservice**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Veraltet. Deaktiviert den Text Dienst für den angegebenen Thread.                                                            |
| [**Immenum inputcontext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Ruft den Eingabe Kontext für den angegebenen Thread ab.                                                                      |
| [**Immenum registerword**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Listet die Registrierungs Zeichenfolgen auf, die die angegebene Lese Zeichenfolge, den Stil und die Registrierungs Zeichenfolge aufweisen                           |
| [**Immescape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Greift auf Funktionen bestimmter IMEs zu, die über andere IME-API-Funktionen nicht verfügbar sind.                           |
| [**Immgetcandidatelist**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Ruft eine Kandidatenliste ab.                                                                                                |
| [**Immgetcandidatelistcount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Ruft die Größe der Kandidatenlisten ab.                                                                                 |
| [**Immgetcandidatewindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Ruft Informationen über das Fenster "Kandidaten" ab.                                                                         |
| [**Immgetcompositionfont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Ruft Informationen über die logische Schriftart ab, die derzeit zum Anzeigen von Zeichen im Kompositionsfenster verwendet wird.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Ruft Informationen über die Kompositionszeichenfolge ab.                                                                        |
| [**Immgetcompositionwindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Ruft Informationen zum Kompositionsfenster ab.                                                                        |
| [**Immgetcontext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Ruft den dem angegebenen Fenster zugeordneten Eingabe Kontext ab.                                                          |
| [**Immgetsystemversionlist**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Ruft die Konvertierungsergebnis Liste von Zeichen oder Wörtern ohne das Erstellen von IME-bezogenen Meldungen ab.                   |
| [**Immgetsystemversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Ruft den aktuellen Konvertierungs Status ab.                                                                                   |
| [**Immgetdefaultimewnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Ruft das Standardfenster Handle für die IME-Klasse ab.                                                                      |
| [**Immgetdescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Kopiert die Beschreibung des IME in den angegebenen Puffer.                                                                 |
| [**Immgetrichtrichtwert**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Ruft Informationen zu Fehlern ab.                                                                                        |
| [**Immgetimefilename**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Ruft den Dateinamen des IME ab, der dem angegebenen Eingabe Gebiets Schema zugeordnet ist.                                             |
| [**Immgetimemenuitems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Ruft die Menü Elemente ab, die im IME-Menü eines angegebenen Eingabe Kontexts registriert sind.                                 |
| [**Immgetopenstatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Bestimmt, ob das IME geöffnet oder geschlossen ist.                                                                              |
| [**Immgetproperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Ruft die Eigenschaft und die Funktionen des IME ab, der dem angegebenen Eingabe Gebiets Schema zugeordnet ist.                             |
| [**Immgetregisterwordstyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Ruft eine Liste der Stile ab, die von dem dem angegebenen Eingabe Gebiets Schema zugeordneten IME unterstützt werden.                            |
| [**Immgetstatus WINDOWPOS**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Ruft die Position des Status Fensters ab.                                                                               |
| [**Immgetvirtualkey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Ruft den ursprünglichen virtuellen Schlüsselwert ab, der einer Schlüsseleingabe Nachricht zugeordnet ist, die der IME bereits verarbeitet hat.           |
| [**Imminstalkalk**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Installiert ein IME.                                                                                                           |
| [**Immisime**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Bestimmt, ob das angegebene Eingabe Gebiets Schema über eine IME verfügt.                                                                       |
| [**Immisuimess Age**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Prüft, ob Nachrichten für das IME-Fenster angezeigt werden, und sendet diese Nachrichten an das angegebene Fenster.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Benachrichtigt den IME über Änderungen am Status des Eingabe Kontexts.                                                         |
| [**Immregisterword**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Registriert eine Zeichenfolge mit dem Wörterbuch des IME, das dem angegebenen Eingabe Gebiets Schema zugeordnet ist.                              |
| [**Immreleasecontext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Gibt den Eingabe kontextfrei und entsperrt den im Eingabe Kontext zugeordneten Arbeitsspeicher.                                         |
| [**Immrequestmessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Fordert eine Meldung von der Anwendung an.                                                                                   |
| [**Immsetcandidatewindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Legt Informationen zum Kandidaten Fenster fest.                                                                              |
| [**Immsetcompositionfont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Legt die logische Schriftart fest, die zum Anzeigen von Zeichen im Kompositionsfenster verwendet werden soll.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Legt die Zeichen, die Attribute und die Klauseln der Kompositions- und Lesezeichenfolgen fest.                                       |
| [**Immsetcompositionwindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Legt die Position des Kompositions Fensters fest.                                                                               |
| [**Immsetsystemversionstatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Legt den aktuellen Konvertierungs Status fest.                                                                                        |
| [**Immendstatusstatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Öffnet oder schließt den IME.                                                                                                   |
| [**Immsetstatus-WINDOWPOS**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Legt die Position des Status Fensters fest.                                                                                    |
| [**Immsimulatehotkey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simuliert die angegebene Taste für den IME-Hot-Wert und bewirkt dieselbe Antwort, als ob der Benutzer die heiße Taste im angegebenen Fenster drückt. |
| [**Immunregisterword**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Entfernt eine Register Zeichenfolge aus dem Wörterbuch des IME, das dem angegebenen Eingabe Gebiets Schema zugeordnet ist.                       |



 

 

 



