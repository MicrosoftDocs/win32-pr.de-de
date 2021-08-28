---
description: Debugausgabefunktionen
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debugausgabefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee1bdbc9cce98ce1704b62a8354b81951df33c4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884238"
---
# <a name="debug-output-functions"></a>Debugausgabefunktionen

Die [DirectShow-Basisklassen](directshow-base-classes.md) stellen mehrere Makros zum Anzeigen von Debuginformationen zur Verfügung.



| Funktion                                               | Beschreibung                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Überprüft, ob die Protokollierung für die angegebenen Nachrichtentypen und -ebene aktiviert ist.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Zeigt Informationen zu aktiven Objekten an.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Initialisiert die Debugbibliothek.                                                                       |
| [**DbgLog**](dbglog.md)                               | Sendet eine Zeichenfolge an den Debugausgabespeicherort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. |
| [**DbgOutString**](dbgoutstring.md)                   | Sendet eine Zeichenfolge an den Debugausgabespeicherort.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Legt den Protokollierungsgrad für einen oder mehrere Nachrichtentypen fest.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Bereinigt die Debugbibliothek.                                                                         |
| [**DisplayType**](displaytype.md)                     | Sendet Informationen zu einem Medientyp an den Debugausgabespeicherort.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Sendet Informationen zu einem Filterdiagramm an den Debugausgabespeicherort.                                 |
| [**GuidNames**](guidnames.md)                         | Globales Array, das Zeichenfolgen enthält, die die in Uuids.h definierten GUIDs darstellen.                        |
| [**NAMEN**](name.md)                                   | Generiert eine Zeichenfolge, die nur debuggt.                                                                       |
| [**HINWEIS**](note.md)                                   | Sendet eine Zeichenfolge an den Debugausgabespeicherort.                                                         |
| [**ERINNERN**](remind.md)                               | Generiert eine Erinnerung zur Kompilierzeit.                                                                |



 

**Registrierungsschlüssel**

Die Debugausgabefunktion in DirectShow verwendet einen Satz von Registrierungsschlüsseln. Der Speicherort dieser Registrierungsschlüssel hängt von der Version des Windows.

*Vor der Windows Vista* befinden sich die Debugschlüssel unter dem folgenden Pfad:

**HKEY \_ DEBUGGEN \_ DER** \\ **SOFTWARE AUF DEM LOKALEN** \\ **COMPUTER**

In Windows Vista oder höher befinden sie sich unter dem folgenden Pfad:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectShow** \\ **Debug**

Bei Filtern von Drittanbietern hängt der Speicherort davon ab, welche Version der [DirectShow-Basisklassen](directshow-base-classes.md) zum Erstellen des Filters verwendet wurde. Die version, die im Windows SDK für Windows Vista enthalten ist, verwendet den neueren Pfad. Frühere Versionen verwendeten den älteren Pfad.

In den folgenden Hinweisen wird die Bezeichnung *&lt; DebugRoot &gt;* verwendet, um diese beiden Pfade anzugeben. Ersetzen Sie den richtigen Pfad, je nach Version Windows oder der Version der Basisklassen.

**Debugprotokollierung**

DirectShow definiert mehrere Nachrichtentypen, wie in der folgenden Tabelle gezeigt.



| Wert                   | Beschreibung                                             |
|-------------------------|---------------------------------------------------------|
| \_PROTOKOLLFEHLER              | Fehlerbenachrichtigung.                                     |
| \_PROTOKOLLSPERREN            | Sperren und Entsperren kritischer Abschnitte.             |
| \_PROTOKOLLSPEICHER             | Speicherzuweisung und Objekterstellung und -zerstörung. |
| \_PROTOKOLLZEITSTEUERUNG             | Zeitsteuerungs- und Leistungsmessungen.                    |
| \_PROTOKOLL-ABLAUFVERFOLGUNG              | Allgemeine Aufrufablaufverfolgung.                                   |
| CUSTOM1 bis CUSTOM5 | Verfügbar für benutzerdefinierte Debugmeldungen                     |



 

Jede der DirectShow-Debugprotokollierungsfunktionen gibt einen Nachrichtentyp und eine Protokollebene an. Die Debugmeldung wird nur angezeigt, wenn die aktuelle Debugebene für diesen Nachrichtentyp gleich oder größer als die in der Protokollierungsfunktion angegebene Ebene ist. Andernfalls wird die Meldung ignoriert.

Der folgende Code gibt beispielsweise die Zeichenfolge "This is a debug message" (Dies ist eine Debugmeldung) aus, wenn die LOG \_ TRACE-Ebene 3 oder höher ist:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Jedes Modul kann für jeden Nachrichtentyp eine eigene Debugebene festlegen. (Ein *Modul ist* eine DLL oder ausführbare Datei, die mit der **LoadLibrary-Funktion geladen werden** kann.) Die Debugebenen eines Moduls werden in der Registrierung unter dem folgenden Schlüssel angezeigt:

**HKEY \_ LOCAL \_ MACHINE** \\ **&lt; DebugRoot &gt;** \\ **&lt; ModuleName &gt;** \\ **&lt; MessageType &gt;**

Dabei *<Message Type>* ist der Nachrichtentyp abzüglich der anfänglichen "LOG", z. \_ B. **LOCKING** für LOG \_ LOCKING-Meldungen. Wenn ein Modul geladen wird, sucht die Debugbibliothek die Protokolliergrade des Moduls in der Registrierung. Wenn die Registrierungsschlüssel nicht vorhanden sind, werden sie von der Debugbibliothek erstellt.

Ein Modul kann zur Laufzeit auch eigene Ebenen festlegen, indem es die [**DbgSetModuleLevel-Funktion**](dbgsetmodulelevel.md) verwendet. Um eine Nachricht an die Debugausgabe zu senden, rufen Sie das [**DbgLog-Makro**](dbglog.md) auf. Im folgenden Beispiel wird eine Meldung der Ebene 3 vom Typ LOG \_ TRACE erstellt:

Sie können auch globale Protokollierungsebenen mit dem folgenden Registrierungsschlüssel angeben:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



Die Debugbibliothek verwendet die ebene, die größer ist, die globale Ebene oder die Modulebene.

**Debugausgabespeicherort**

Der Debugausgabespeicherort wird durch einen anderen Registrierungsschlüssel bestimmt:

**HKEY \_ LOCAL \_ MACHINE** \\ **&lt; DebugRoot &gt;** \\ **<Modile Name>** \\ **LogToFile**

Wenn der Wert dieses Schlüssels `Console` ist, wird die Ausgabe an das Konsolenfenster ausgegeben. Wenn der Wert `Deb` , , oder eine leere `Debug` `Debugger` Zeichenfolge ist, wird die Ausgabe an das Debuggerfenster gesendet. Andernfalls wird die Ausgabe in eine Datei geschrieben, die durch den Registrierungsschlüssel angegeben wird.

Bevor eine ausführbare Datei die DirectShow-Debugbibliothek verwendet, muss sie die [**DbgInitialise-Funktion**](dbginitialise.md) aufrufen. Anschließend muss die [**DbgTerminate-Funktion aufrufen.**](dbgterminate.md) DLLs müssen diese Funktionen nicht aufrufen, da der DLL-Einstiegspunkt (definiert in der Basisklassenbibliothek) sie automatisch aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Hilfsprogrammen](debugging-utilities.md)
</dt> </dl>

 

 



