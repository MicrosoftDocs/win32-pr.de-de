---
description: In diesem Abschnitt werden die IMM-Funktionen beschrieben.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Funktionen des Eingabemethode-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c0f03c2e6d29b262bd97729b92f9eea5fbf99d09f52ea3fe2b3579646a6fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948729"
---
# <a name="input-method-manager-functions"></a>Funktionen des Eingabemethode-Managers

In diesem Abschnitt werden die IMM-Funktionen beschrieben.



| Funktion                                                           | Beschreibung                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Gibt einen Zeiger auf eine [**IFECommon-Schnittstelle**](/windows/desktop/api/Msime/nn-msime-ifecommon) zurück.                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Gibt einen Zeiger auf eine [**IFEDictionary-Schnittstelle**](/windows/desktop/api/Msime/nn-msime-ifedictionary) zurück.                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Gibt einen Zeiger auf eine [**IFELanguage-Schnittstelle**](/windows/desktop/api/Msime/nn-msime-ifelanguage) zurück.                                                      |
| [**EnumInputContext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Eine anwendungsdefinierte Rückruffunktion, die Eingabekontexte verarbeitet, die von der **ImmEnumInputContext-Funktion bereitgestellt** werden.   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Eine anwendungsdefinierte Rückruffunktion, die mit der **ImmEnumRegisterWord-Funktion verwendet** wird.                                   |
| [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Ordnet dem angegebenen Fenster den angegebenen Eingabekontext zu.                                                          |
| [**ImmAssociateContextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Ändert die Zuordnung zwischen dem Eingabemethodenkontext und dem angegebenen Fenster oder seinen unteren Fenstern.                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Zeigt das Konfigurationsdialogfeld für den IME des angegebenen Eingabe-Locale Identifiers an.                                |
| [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Erstellt einen neuen Eingabekontext, der Arbeitsspeicher für den Kontext zuteilt und initialisiert.                                        |
| [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Gibt den Eingabekontext frei und gibt zugeordneten Arbeitsspeicher frei.                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Deaktiviert den IME für einen Thread oder für alle Threads in einem Prozess.                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Gibt an, dass dieser Thread ein benutzeroberflächenthread Windows Store App ist.                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Veraltet. Deaktiviert den Textdienst für den angegebenen Thread.                                                            |
| [**ImmEnumInputContext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Ruft den Eingabekontext für den angegebenen Thread ab.                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Enumeriert die Registerzeichenfolgen mit der angegebenen Lesezeichenfolge, dem angegebenen Format und der angegebenen Registerzeichenfolge.                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Zugriff auf Funktionen bestimmter IMEs, die nicht über andere IME-API-Funktionen verfügbar sind.                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Ruft eine Kandidatenliste ab.                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Ruft die Größe der Kandidatenlisten ab.                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Ruft Informationen zum Kandidatenfenster ab.                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Ruft Informationen über die logische Schriftart ab, die derzeit zum Anzeigen von Zeichen im Kompositionsfenster verwendet wird.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Ruft Informationen über die Kompositionszeichenfolge ab.                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Ruft Informationen zum Kompositionsfenster ab.                                                                        |
| [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Ruft den Eingabekontext ab, der dem angegebenen Fenster zugeordnet ist.                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Ruft die Liste der Konvertierungsergebniszeichen oder Wörter ab, ohne IME-bezogene Meldungen zu generieren.                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Ruft den aktuellen Konvertierungsstatus ab.                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Ruft das Standardfensterhand handle für die IME-Klasse ab.                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Kopiert die Beschreibung des IME in den angegebenen Puffer.                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Ruft Informationen zu Fehlern ab.                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Ruft den Dateinamen des IME ab, der dem angegebenen Eingabe-Locale zugeordnet ist.                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Ruft die Menüelemente ab, die im IME-Menü eines angegebenen Eingabekontexts registriert sind.                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Bestimmt, ob der IME geöffnet oder geschlossen ist.                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Ruft die -Eigenschaft und die Funktionen des IME ab, die dem angegebenen Eingabe-Locale zugeordnet sind.                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Ruft eine Liste der Stile ab, die vom IME unterstützt werden, der dem angegebenen Eingabe-Locale zugeordnet ist.                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Ruft die Position des Statusfensters ab.                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Ruft den ursprünglichen Wert des virtuellen Schlüssels ab, der einer Schlüsseleingabenachricht zugeordnet ist, die der IME bereits verarbeitet hat.           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Installiert einen IME.                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Bestimmt, ob das angegebene Eingabe-Locale über einen IME verfügt.                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Sucht nach Nachrichten, die für das IME-Fenster bestimmt sind, und sendet diese Nachrichten an das angegebene Fenster.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Benachrichtigt den IME über Änderungen am Status des Eingabekontexts.                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Registriert eine Zeichenfolge mit dem Wörterbuch des IME, das dem angegebenen Eingabe-Locale zugeordnet ist.                              |
| [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Gibt den Eingabekontext frei und entsperrt den Speicher, der im Eingabekontext zugeordnet ist.                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Fordert eine Nachricht von der Anwendung an.                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Legt Informationen zum Kandidatenfenster fest.                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Legt die logische Schriftart fest, die zum Anzeigen von Zeichen im Kompositionsfenster verwendet werden soll.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Legt die Zeichen, die Attribute und die Klauseln der Kompositions- und Lesezeichenfolgen fest.                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Legt die Position des Kompositionsfensters fest.                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Legt den aktuellen Konvertierungsstatus fest.                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Öffnet oder schließt die IME.                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Legt die Position des Statusfensters fest.                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simuliert den angegebenen IME-Hot-Schlüssel, wodurch die gleiche Antwort wie beim Drücken der Hot-Taste im angegebenen Fenster durch den Benutzer verursacht wird. |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Entfernt eine Registerzeichenfolge aus dem Wörterbuch der IME, die dem angegebenen Eingabeschema zugeordnet ist.                       |



 

 

 



