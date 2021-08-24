---
description: Die folgenden Hilfsfunktionen werden von Parsern aufgerufen.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Parserfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d70c3ad44ad809a323af8acde732af3b142759d3686d78c496f47e92cb8e209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676840"
---
# <a name="parser-functions"></a>Parserfunktionen

Die folgenden Hilfsfunktionen werden von Parsern aufgerufen.



| Funktion                                                 | Beschreibung                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Konvertiert eine Adresse in eine Zeichenfolge.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Ruft die Zeichenfolge ab, die dem angegebenen Wert eines bezeichneten Sets entspricht.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Erfasst einen Kontextinstanzzeiger.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Konvertiert eine Zeichenfolge in eine Adresse.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Konvertiert eine kleine ganze Zahl variabler Länge in einen **DWORD-Wert.**                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Ruft die Zeichenfolge ab, die dem angegebenen Wert eines bezeichneten Sets entspricht.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Ruft die Zeichenfolge ab, die dem angegebenen Wert aus einem bezeichneten Satz entspricht.                                      |
| [BERGetHeader](bergetheader.md)                         | Decodiert einen Auswahlheader.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Decodiert eine BER-codierte ganze Zahl.                                                                                 |
| [BERGetString](bergetstring.md)                         | Decodiert eine BER-codierte Zeichenfolge.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Ordnet Arbeitsspeicher auf Capture-by-Capture-Basis zu.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Gibt den von der **CCHeapAlloc-Funktion zugeordneten Arbeitsspeicher** frei.                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Reserviert den von der **CCHeapAlloc-Funktion zugewiesenen Arbeitsspeicher neu.**                                                  |
| [CCHeapSize](ccheapsize.md)                             | Ruft die Größe des von der **CCHeapAlloc-Funktion zugeordneten Arbeitsspeichers** ab.                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Ruft den Zeiger auf die Instanzdaten ab, die dem Erfassungskontext hinzugefügt wurden.                                       |
| [CreateProtocol](createprotocol.md)                     | Informiert die Netzwerkmonitor-API darüber, dass ein bestimmter Protokollparser vorhanden ist.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Zerstört das von der **CreateProtocol-Funktion erstellte** Protokoll.                                              |
| [BuildINIPath](buildinipath.md)                         | Ruft einen vollqualifizierten Pfad zur Initialisierungsdatei (INI) ab, der den von Ihnen eingeben Informationen entspricht.   |
| [CreateHandoffTable](createhandofftable.md)             | Erstellt eine Übergabetabelle basierend auf Informationen in einer bestimmten INI-Datei.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Zerstört eine mit der **CreateHandoffTable-Funktion erstellte Übergabetabelle.**                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Ruft das Protokoll einer angegebenen Übergabetabelle ab.                                                               |
| [Addproperty](/previous-versions/bb251873(v=msdn.10))                           | Fügt der Eigenschaftendatenbank eine **PROPERTYINFO-Struktur** hinzu.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Angefügt eine Eigenschafteninstanz an einen Frame.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Angefügt eine Eigenschafteninstanz an einen Frame.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Erstellt eine Eigenschaftendatenbank, die Eigenschaften beschreibt, die der Parser zum Beschreiben seiner Daten verwendet.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Zerstört eine Eigenschaftendatenbank, die durch Aufrufe der **Funktionen CreatePropertyDatabase und** **AddProperty erstellt** wurde. |
| [FindNextFrame](findnextframe.md)                       | Sucht den nächsten Frame im aktuellen Erfassungskontext, der einem bestimmten Filter entspricht.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Sucht den vorherigen Frame im aktuellen Erfassungskontext, der einem bestimmten Filter entspricht.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Formatiert die Eigenschafteninstanz auf generische Weise.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Ruft die Zieladresse eines Frames ab.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Ruft die Quelladresse eines Frames ab.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Ruft den Offset zu einem bestimmten Protokoll im Frame ab.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Sperrt einen Frame, wenn er in einen Parser eintritt, und entsperrt den Frame, wenn er beendet wird.                                     |



 

Informationen zu Exportfunktionen (Hilfsfunktionen, die von Experten und Parsern aufgerufen werden können), Strukturen und Enumerationen finden Sie in den folgenden Themen.



| Informationen über                                  | Finden Sie unter                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funktionen, die Parser exportieren.                         | [Parser-DLL-Exportfunktionen](parser-dll-export-functions.md)               |
| Strukturen, die von Parserfunktionen verwendet werden.                  | [Parserstrukturen](parser-structures.md)                                   |
| Allgemeine Hilfsfunktionen, die Parser und Experten aufrufen. | [Allgemeine Funktionen von Experten und Parsern](expert-and-parser-common-functions.md) |



 

 

 
