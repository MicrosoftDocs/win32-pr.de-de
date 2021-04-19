---
description: Debug-Ausgabefunktionen
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debug-Ausgabefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342965"
---
# <a name="debug-output-functions"></a>Debug-Ausgabefunktionen

Die [DirectShow-Basisklassen](directshow-base-classes.md) stellen mehrere Makros zum Anzeigen von Debuginformationen bereit.



| Funktion                                               | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Dbgcheckmodulelevel**](dbgcheckmodulelevel.md)     | Überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und die angegebene Ebene aktiviert ist.                             |
| [**Dbgdumpobjectregiester**](dbgdumpobjectregister.md) | Zeigt Informationen zu aktiven Objekten an.                                                           |
| [**Dbginitialise**](dbginitialise.md)                 | Initialisiert die Debugbibliothek.                                                                       |
| [**Dbglog**](dbglog.md)                               | Sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. |
| [**Dbgoutstring**](dbgoutstring.md)                   | Sendet eine Zeichenfolge an den debugausgabespeicherort.                                                         |
| [**Dbgsetmodulelevel**](dbgsetmodulelevel.md)         | Legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest.                                                |
| [**Dbgbeenden**](dbgterminate.md)                   | Bereinigt die Debug-Bibliothek.                                                                         |
| [**Display Type**](displaytype.md)                     | Sendet Informationen über einen Medientyp an den debugausgabespeicherort.                                   |
| [**Dumpgraph**](dumpgraph.md)                         | Sendet Informationen zu einem Filter Diagramm an den debugausgabespeicherort.                                 |
| [**Guidnames**](guidnames.md)                         | Globales Array, das Zeichen folgen enthält, die die in "UUIDs. h" definierten GUIDs darstellen.                        |
| [**Benennen**](name.md)                                   | Generiert eine reine debugzeichenfolge.                                                                       |
| [**Nebenbei**](note.md)                                   | Sendet eine Zeichenfolge an den debugausgabespeicherort.                                                         |
| [**Erinnern**](remind.md)                               | Generiert zum Zeitpunkt der Kompilierung eine Erinnerung.                                                                |



 

**Registrierungsschlüssel**

Die Debug-Ausgabefunktion in DirectShow verwendet einen Satz von Registrierungs Schlüsseln. Der Speicherort dieser Registrierungsschlüssel hängt von der Windows-Version ab.

*Vor Windows Vista* befinden sich die debugschlüssel unter folgendem Pfad:

**HKEY \_ \_** \\ **Software** \\ **Debuggen** des lokalen Computers

In Windows Vista oder höher befinden sich diese unter folgendem Pfad:

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**

Für Filter von Drittanbietern hängt der Speicherort davon ab, welche Version der [DirectShow-Basisklassen](directshow-base-classes.md) verwendet wurde, um den Filter zu erstellen. Die Version, die im Windows SDK für Windows Vista enthalten ist, verwendet den neueren Pfad. In früheren Versionen wurde der ältere Pfad verwendet.

In den folgenden Anmerkungen wird die Bezeichnung *<DebugRoot>* verwendet, um diese beiden Pfade anzugeben. Ersetzen Sie abhängig von der Windows-Version oder der-Version der Basisklassen den korrekten Pfad.

**Debugprotokollierung**

In DirectShow werden mehrere Nachrichten Typen definiert, die in der folgenden Tabelle aufgeführt sind.



| Wert                   | BESCHREIBUNG                                             |
|-------------------------|---------------------------------------------------------|
| Protokoll \_ Fehler              | Fehler Benachrichtigung.                                     |
| Protokoll \_ Sperren            | Sperren und entsperren kritischer Abschnitte.             |
| Protokoll \_ Speicher             | Speicher Belegung und Objekt Erstellung und-Zerstörung. |
| Protokoll \_ zeitliche Steuerung             | Zeitliche Steuerung und Leistungsmessungen.                    |
| Protokoll Ablauf \_ Verfolgung              | Allgemeine Rückruf-Ablauf Verfolgung.                                   |
| CUSTOM1 bis CUSTOM5 | Verfügbar für benutzerdefinierte Debugmeldungen                     |



 

Jede der DirectShow-Debug-Protokollierungsfunktionen gibt einen Nachrichtentyp und eine Protokollebene an. Die Debugmeldung wird nur angezeigt, wenn die aktuelle Debugebene für diesen Nachrichtentyp größer oder gleich der in der Protokollierungsfunktion angegebenen Ebene ist. Andernfalls wird die Meldung ignoriert.

Der folgende Code gibt beispielsweise die Zeichenfolge "This is a Debug Message" aus, wenn die Protokoll Ablauf \_ Verfolgungs Ebene 3 oder höher ist:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Jedes Modul kann seine eigene Debugebene für jeden Nachrichtentyp festlegen. (Ein *Modul* ist eine DLL-Datei oder ausführbare Datei, die mithilfe der **LoadLibrary** -Funktion geladen werden kann.) Die debugebenen eines Moduls werden in der Registrierung unter dem folgenden Schlüssel angezeigt:

**lokaler HKEY- \_ \_ Computer**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

dabei *<Message Type>* ist der Nachrichtentyp abzüglich des anfänglichen "Protokolls \_ ", z. b. **Sperren** für Protokoll \_ Sperr Nachrichten. Wenn ein Modul geladen wird, sucht die Debugbibliothek die Protokolliergrade des Moduls in der Registrierung. Wenn die Registrierungsschlüssel nicht vorhanden sind, werden Sie von der Debugbibliothek erstellt.

Ein Modul kann mithilfe der [**dbgsetmodulelevel**](dbgsetmodulelevel.md) -Funktion auch seine eigenen Ebenen zur Laufzeit festlegen. Um eine Nachricht an die Debugausgabe zu senden, nennen Sie das [**dbglog**](dbglog.md) -Makro. Im folgenden Beispiel wird eine Nachricht der Ebene 3 des Typs log \_ Trace erstellt:

Sie können auch globale Protokollierungs Stufen mit dem folgenden Registrierungsschlüssel angeben:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



Die Debug-Bibliothek verwendet, je nachdem, auf welcher Ebene größer, auf der globalen Ebene oder auf der Modulebene.

**Ausgabepfad Debuggen**

Der Speicherort der Debugausgabe wird durch einen anderen Registrierungsschlüssel bestimmt:

**HKEY \_ \_** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **Protokolldatei** des lokalen Computers

Wenn der Wert dieses Schlüssels ist `Console` , wird die Ausgabe in das Konsolenfenster ausgegeben. Wenn der Wert `Deb` , `Debug` , `Debugger` oder eine leere Zeichenfolge ist, wird die Ausgabe an das Debuggerfenster weitergeleitet. Andernfalls wird die Ausgabe in eine Datei geschrieben, die durch den Registrierungsschlüssel angegeben wird.

Bevor eine ausführbare Datei die DirectShow-Debugbibliothek verwendet, muss Sie die [**dbginitialise**](dbginitialise.md) -Funktion aufruft. Danach muss Sie die [**dbgend**](dbgterminate.md) -Funktion abrufen. DLLs müssen diese Funktionen nicht aufrufen, da Sie vom DLL-Einstiegspunkt (in der Basisklassen Bibliothek definiert) automatisch aufgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugging-Hilfsprogramme](debugging-utilities.md)
</dt> </dl>

 

 



