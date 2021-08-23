---
description: Debuggen von Ausgabefunktionen
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debuggen von Ausgabefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252e1020ca99bd5b4f2f46d7f2169fa6835dea83a25d599dba142f370bb794f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537740"
---
# <a name="debug-output-functions"></a>Debuggen von Ausgabefunktionen

Die [DirectShow-Basisklassen](directshow-base-classes.md) stellen mehrere Makros zum Anzeigen von Debuginformationen bereit.



| Funktion                                               | Beschreibung                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Überprüft, ob die Protokollierung für die angegebenen Nachrichtentypen und -ebenen aktiviert ist.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Zeigt Informationen zu aktiven Objekten an.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Initialisiert die Debugbibliothek.                                                                       |
| [**DbgLog**](dbglog.md)                               | Sendet eine Zeichenfolge an den Debugausgabespeicherort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. |
| [**DbgOutString**](dbgoutstring.md)                   | Sendet eine Zeichenfolge an den Debugausgabespeicherort.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Legt den Protokolliergrad für einen oder mehrere Nachrichtentypen fest.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Bereinigt die Debugbibliothek.                                                                         |
| [**DisplayType**](displaytype.md)                     | Sendet Informationen zu einem Medientyp an den Debugausgabespeicherort.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Sendet Informationen zu einem Filterdiagramm an den Debugausgabespeicherort.                                 |
| [**GuidNames**](guidnames.md)                         | Globales Array, das Zeichenfolgen enthält, die die in Uuids.h definierten GUIDs darstellen.                        |
| [**Namen**](name.md)                                   | Generiert eine Nur-Debug-Zeichenfolge.                                                                       |
| [**Hinweis**](note.md)                                   | Sendet eine Zeichenfolge an den Debugausgabespeicherort.                                                         |
| [**Erinnern**](remind.md)                               | Generiert zur Kompilierzeit eine Erinnerung.                                                                |



 

**Registrierungsschlüssel**

Die Debugausgabefunktion in DirectShow verwendet einen Satz von Registrierungsschlüsseln. Der Speicherort dieser Registrierungsschlüssel hängt von der Version der Windows ab.

*Vor Windows Vista* befinden sich die Debugschlüssel unter folgendem Pfad:

**HKEY \_ \_** \\  \\ **SOFTWAREdebuggen** AUF DEM LOKALEN COMPUTER

In Windows Vista oder höher befinden sie sich unter dem folgenden Pfad:

**HKEY \_ LOKALE \_ COMPUTERSOFTWARE** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**

Bei Filtern von Drittanbietern hängt der Speicherort davon ab, welche Version der [DirectShow-Basisklassen](directshow-base-classes.md) zum Erstellen des Filters verwendet wurde. Die version, die im Windows SDK für Windows Vista enthalten ist, verwendet den neueren Pfad. Frühere Versionen verwendeten den älteren Pfad.

In den folgenden Hinweisen wird die Bezeichnung *<DebugRoot>* verwendet, um diese beiden Pfade anzugeben. Ersetzen Sie den richtigen Pfad abhängig von der Version von Windows oder der Version der Basisklassen.

**Debugprotokollierung**

DirectShow definiert mehrere Nachrichtentypen, wie in der folgenden Tabelle gezeigt.



| Wert                   | Beschreibung                                             |
|-------------------------|---------------------------------------------------------|
| \_PROTOKOLLFEHLER              | Fehlerbenachrichtigung.                                     |
| \_PROTOKOLLSPERREN            | Sperren und Entsperren kritischer Abschnitte.             |
| \_PROTOKOLLSPEICHER             | Speicherbelegung und Objekterstellung und -zerstörung. |
| \_PROTOKOLLIERUNGSZEIT             | Zeit- und Leistungsmessungen.                    |
| \_PROTOKOLLABLAUFVERFOLGUNG              | Allgemeine Aufrufablaufverfolgung.                                   |
| CUSTOM1 bis CUSTOM5 | Verfügbar für benutzerdefinierte Debugmeldungen                     |



 

Jede der DirectShow-Debugprotokollierungsfunktionen gibt einen Nachrichtentyp und einen Protokolliergrad an. Die Debugmeldung wird nur angezeigt, wenn die aktuelle Debugebene für diesen Meldungstyp gleich oder größer als die in der Protokollierungsfunktion angegebene Ebene ist. Andernfalls wird die Nachricht ignoriert.

Der folgende Code gibt beispielsweise die Zeichenfolge "This is a debug message" (Dies ist eine Debugmeldung) aus, wenn die LOG \_ TRACE-Ebene 3 oder höher ist:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Jedes Modul kann für jeden Nachrichtentyp eine eigene Debugebene festlegen. (Ein *Modul* ist eine DLL oder ausführbare Datei, die mit der **LoadLibrary-Funktion** geladen werden kann.) Die Debugebenen eines Moduls werden in der Registrierung unter dem folgenden Schlüssel angezeigt:

**HKEY \_ LOCAL \_ MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

dabei *<Message Type>* ist der Nachrichtentyp minus dem anfänglichen "LOG", \_ z. B. **LOCKING** für LOG \_ LOCKING-Nachrichten. Wenn ein Modul geladen wird, findet die Debugbibliothek die Protokolliergrade des Moduls in der Registrierung. Wenn die Registrierungsschlüssel nicht vorhanden sind, werden sie von der Debugbibliothek erstellt.

Ein Modul kann mithilfe der [**DbgSetModuleLevel-Funktion**](dbgsetmodulelevel.md) auch eigene Ebenen zur Laufzeit festlegen. Um eine Nachricht an die Debugausgabe zu senden, rufen Sie das [**DbgLog-Makro**](dbglog.md) auf. Im folgenden Beispiel wird eine Meldung der Ebene 3 vom Typ LOG \_ TRACE erstellt:

Sie können auch globale Protokolliergrade mit dem folgenden Registrierungsschlüssel angeben:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



Die Debugbibliothek verwendet die höhere Ebene, die globale Ebene oder die Modulebene.

**Debugausgabespeicherort**

Der Speicherort der Debugausgabe wird durch einen anderen Registrierungsschlüssel bestimmt:

**HKEY \_ LOCAL \_ MACHINE** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**

Wenn der Wert dieses Schlüssels `Console` ist, wird die Ausgabe an das Konsolenfenster ausgegeben. Wenn der Wert `Deb` , , oder eine leere Zeichenfolge `Debug` `Debugger` ist, wird die Ausgabe an das Debuggerfenster ausgegeben. Andernfalls wird die Ausgabe in eine Datei geschrieben, die durch den Registrierungsschlüssel angegeben wird.

Bevor eine ausführbare Datei die DirectShow-Debugbibliothek verwendet, muss sie die [**DbgInitialise-Funktion**](dbginitialise.md) aufrufen. Anschließend muss die [**DbgTerminate-Funktion**](dbgterminate.md) aufgerufen werden. DLLs müssen diese Funktionen nicht aufrufen, da sie vom DLL-Einstiegspunkt (definiert in der Basisklassenbibliothek) automatisch aufgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Hilfsprogrammen](debugging-utilities.md)
</dt> </dl>

 

 



