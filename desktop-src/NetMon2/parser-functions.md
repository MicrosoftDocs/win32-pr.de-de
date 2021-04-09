---
description: Die folgenden Hilfsfunktionen werden von den-Parametern aufgerufen.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Parser-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a502778247a3daad5f11dd8d0e2a3312d586d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128317"
---
# <a name="parser-functions"></a>Parser-Funktionen

Die folgenden Hilfsfunktionen werden von den-Parametern aufgerufen.



| Funktion                                                 | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| ["Adresssstostring"](addresstostring.md)                   | Konvertiert eine Adresse in eine Zeichenfolge.                                                                               |
| [Lookupbytesetstring](lookupbytesetstring.md)           | Ruft die Zeichenfolge ab, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.                                    |
| [Setccinstptr](setccinstptr.md)                         | Erfasst einen Kontext Instanz-Zeiger.                                                                           |
| [Stringto Address](stringtoaddress.md)                   | Konvertiert eine Zeichenfolge in eine Adresse.                                                                               |
| [Varlensmallinttodword](varlensmallinttodword.md)       | Konvertiert eine kleine Ganzzahl mit variabler Länge in ein **DWORD**-Zeichen.                                                      |
| [Lookupdwordsetstring](lookupdwordsetstring.md)         | Ruft die Zeichenfolge ab, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.                                    |
| [Lookupwordsetstring](lookupwordsetstring.md)           | Ruft die Zeichenfolge ab, die dem angegebenen Wert aus einer gekennzeichneten Menge entspricht.                                      |
| [Bergedorfer Leser](bergetheader.md)                         | Decodiert einen Auswahl Header.                                                                                       |
| [Bergetinteger](bergetinteger.md)                       | Decodiert eine BER-codierte Ganzzahl.                                                                                 |
| [Bergetstring](bergetstring.md)                         | Decodiert eine BER-codierte Zeichenfolge.                                                                                  |
| [Ccheap-Zuweisung](ccheapalloc.md)                           | Belegt Speicher auf Erfassungs Basis.                                                                |
| [Ccheapfree](ccheapfree.md)                             | Gibt den Arbeitsspeicher frei, der von der **ccheap-Zuordnungs** Funktion zugeordnet wurde.                                                 |
| [Ccheaprezuweisung](ccheaprealloc.md)                       | Reserviert den von der **ccheapbelegc** -Funktion zugewiesenen Arbeitsspeicher neu.                                                  |
| [Ccheapsize](ccheapsize.md)                             | Ruft die Größe des Arbeitsspeichers ab, der von der **ccheap-Zuordnungs** Funktion zugeordnet wurde.                                    |
| [Getccinstptr](getccinstptr.md)                         | Ruft den Zeiger auf die Instanzdaten ab, die dem Aufzeichnungs Kontext hinzugefügt wurden.                                       |
| ["Kreateprotocol"](createprotocol.md)                     | Informiert den Netzwerkmonitor-API, dass ein bestimmter Protokoll Parser vorhanden ist.                                        |
| [Destroyprotocol](destroyprotocol.md)                   | Zerstört das Protokoll **, das von der Funktion "** -Funktion" erstellt wurde.                                              |
| [Buildinipath](buildinipath.md)                         | Ruft einen voll qualifizierten Pfad zur-Initialisierungsdatei (INI-Datei) ab, die den von Ihnen eingegebenen Informationen entspricht.   |
| ["Kreatehandofftable"](createhandofftable.md)             | Erstellt eine Übergabe Tabelle basierend auf Informationen in einer angegebenen ini-Datei.                                             |
| [Destroyhandofftable](destroyhandofftable.md)           | Zerstört eine mit der Funktion "-Funktion" erstellte **handofftabelle** .                                     |
| [Getprotocolfromtable](getprotocolfromtable.md)         | Ruft das Protokoll einer gegebenen Übergabe-Tabelle ab.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Fügt der Eigenschaften Datenbank eine **PropertyInfo** -Struktur hinzu.                                                    |
| [Attachpropertyinstance](attachpropertyinstance.md)     | Fügt eine Eigenschaften Instanz an einen Frame an.                                                                       |
| [Attachpropertyinstanceex](attachpropertyinstanceex.md) | Fügt eine Eigenschaften Instanz an einen Frame an.                                                                       |
| ["Kreatepropertydatabase"](createpropertydatabase.md)     | Erstellt eine Eigenschaften Datenbank, in der die Eigenschaften beschrieben werden, die der Parser zum Beschreiben der Daten verwendet.               |
| [Destroypropertydatabase](destroypropertydatabase.md)   | Zerstört eine Eigenschaften Datenbank, die durch Aufrufe der Funktionen " **deatepropertydatabase** " und " **AddProperty** " erstellt wurde. |
| [Findnextframe](findnextframe.md)                       | Sucht den nächsten Frame im aktuellen Aufzeichnungs Kontext, der mit einem angegebenen Filter übereinstimmt.                               |
| [Findpreviousframe](findpreviousframe.md)               | Sucht den vorherigen Frame im aktuellen Aufzeichnungs Kontext, der mit einem angegebenen Filter übereinstimmt.                           |
| [Formatpropertyinstance](formatpropertyinstance.md)     | Formatiert die Eigenschaften Instanz auf generische Weise.                                                             |
| [Getframeumstaddress](getframedestaddress.md)           | Ruft die Zieladresse eines Frames ab.                                                                  |
| [Getframesourceaddress](getframesourceaddress.md)       | Ruft die Quelladresse eines Frames ab.                                                                       |
| [Getprotocolstartffset](getprotocolstartoffset.md)     | Ruft den Offset für ein bestimmtes Protokoll im Frame ab.                                                         |
| [Parametertemporarylockframe](parsertemporarylockframe.md) | Sperrt einen Frame, wenn er in einen Parser Eintritt und entsperrt den Frame, wenn er beendet wird.                                     |



 

Informationen zu Exportfunktionen (Hilfsfunktionen, die von Experten und Parser aufgerufen werden können), Strukturen und Enumerationen finden Sie in den folgenden Themen.



| Informationen über                                  | Finden Sie unter                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funktionen, mit denen der Export exportiert wird.                         | [Export Funktionen der Parser-DLL](parser-dll-export-functions.md)               |
| Strukturen, die von Parserfunktionen verwendet werden.                  | [Parserstrukturen](parser-structures.md)                                   |
| Allgemeine Hilfsfunktionen, die von Parser und Experten aufgerufen werden. | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |



 

 

 
