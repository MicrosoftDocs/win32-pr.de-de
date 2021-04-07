---
description: Die Terminal Objekt Schnittstellen stellen dem Anwendungs Zugriff zum Bearbeiten von Geräten zur Verfügung, die zum Erstellen oder empfangen von Mediendaten strömen verwendet werden.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Terminal Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760789"
---
# <a name="terminal-object-interfaces"></a>Terminal Objekt Schnittstellen

Die [Terminal Objekt](terminal-object.md) Schnittstellen stellen dem Anwendungs Zugriff zum Bearbeiten von Geräten zur Verfügung, die zum Erstellen oder empfangen von Mediendaten strömen verwendet werden.

Diese Schnittstellen werden von einem MSP implementiert und sind nicht verfügbar, wenn die Adresse von einem Medien Dienstanbieter nicht unterstützt wird. Wenn ein zugeordnetes MSP vorhanden ist, wird die [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) -Schnittstelle für das [Address-Objekt](address-object.md)verfügbar gemacht.

Die [**ienumterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) -und [**ienumterminalclass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) -Schnittstellen werden nicht direkt für das Terminal Objekt verfügbar gemacht, sind aber eng damit verknüpft und werden hier zur Verfügung gestellt.



| Schnittstelle                                                                  | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Basisschnittstelle für das Terminal Objekt. Es bietet Methoden zum Abrufen von Informationen, wie z. b. Terminal Klasse und unterstützte Medien. |
| [**Itammediaformat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Legt das DirectShow-Medienformat fest und ruft es ab.                                                                                            |
| [**Itbasicaudioterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Stellt Methoden bereit, mit denen die standardmäßigen audioterminalmerkmale, wie z. b. Volume                                          |
| [**Ienumterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Listet [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)auf.                                                                                      |
| [**Ienumterminalclass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Listet die [**Terminal Klasse**](terminal-class.md)auf.                                                                              |
| [**Ienumpluggablesuperclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Listet [**itpluggableterminalsuperclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)auf.                                        |
| [**Ienumpluggableterminalclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Listet [**itpluggableterminalclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)auf.                                                  |
| [**Itfiletrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Ruft Informationen über Datei Terminal Titel ab und legt Sie fest.                                                                   |
| [**Itasrterminalevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Ruft die Beschreibung der automatischen sprechererkennungs-Terminal Ereignisse ab.                                                        |
| [**Itfileterminalevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Ruft die Beschreibung der Datei Terminal Ereignisse ab.                                                                                |
| [**Itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Listet auf Multitrack-Terminals auf, erstellt oder entfernt Sie.                                                                   |



 



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Itpluggableterminalclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Ruft Informationen zu einem austauschbaren Terminal ab.                                                                       |
| [**Itpluggableterminalclassregistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Erstellt, ändert oder löscht den Registrierungs Eintrag für ein austauschbares Terminal.                                                   |
| [**Itpluggableterminalinitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Führt die primäre Terminal Objekt Erstellung für austauschbare Terminals aus, sodass der Terminal-Manager das Terminal initialisieren kann. |
| [**Itpluggableterminalsuperclassinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Ruft den Namen und die CLSID einer austauschbaren Terminal Klasse ab.                                                                  |
| [**Itpluggableterminalsuperclassregistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Ruft Informationen zu einer Terminal übergeordneten Klasse (Name und CLSID) ab und legt Sie fest.                                                 |
| [**Itpluggableterminaleventsink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Benachrichtigt Client Anwendungen über Änderungen in einem austauschbaren Terminal.                                                          |
| [**Itpluggableterminaleventsink Registration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Registriert eine Client Anwendung und hebt die Registrierung für Benachrichtigungen über austauschbare Terminal Ereignisse auf.                             |



 



| Schnittstelle                                            | BESCHREIBUNG                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**Itttsterminalevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Ruft die Beschreibung der Terminal Ereignisse von Text-zu-Sprache (TTS) ab. |
| [**Ittonedetectionevent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Ruft Informationen zu einem Tone-Erkennungs Ereignis ab.                |
| [**Ittoneterminalevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Ruft die Beschreibung der Tone-Terminal Ereignisse ab.                 |



 

 

 
