---
description: In diesem Abschnitt werden Strukturen beschrieben, die Sie zum Entwickeln von Parsern verwenden können. Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie zum Entwickeln von Parsern oder Experten verwenden können.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Parserstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d54e02e26e9874f27f49312a84b4b643cc4b3bfdb0c6056f274e4febecf0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082530"
---
# <a name="parser-structures"></a>Parserstrukturen

In diesem Abschnitt werden Strukturen beschrieben, die Sie zum Entwickeln von Parsern verwenden können. Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie zum Entwickeln von Parsern oder Experten verwenden können.



| Struktur                                 | BESCHREIBUNG                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Definiert die am häufigsten verwendeten anfänglichen Protokolle.                                                                               |
| [Entrypoints](entrypoints.md)            | Gibt Zeiger auf die Einstiegspunkte für die Parser-DLL an.                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | Gibt das Protokoll an, das dem aktuellen Protokoll folgt.                                                                       |
| [PF \_ FOLLOWSET](pf-followset.md)         | Gibt den Satz von Protokollen an, die dem aktuellen Protokoll folgen.                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | Gibt entweder das Protokoll an, das an das aktuelle Protokoll übergibt, oder das Protokoll, an das das aktuelle Protokoll übergibt.    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | Gibt den Satz von Protokollen an, die an das aktuelle Protokoll oder den Satz von Protokollen übergibt, an die das aktuelle Protokoll übergibt. |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | Gibt die Anzahl der Parser in der Parser-DLL und Informationen zu den einzelnen Parsern an.                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | Gibt Informationen zu einem bestimmten Parser an.                                                                                  |
| [BEZEICHNETES \_ BIT](labeled-bit.md)           | Gibt Handles, BIT-Felder oder Flags an.                                                                                        |
| [BEZEICHNETES \_ BYTE](labeled-byte.md)         | Gibt ein **BYTE-Bezeichnungspaar** an.                                                                                                |
| [BEZEICHNETES \_ DWORD](labeled-dword.md)       | Gibt ein **DWORD-Bezeichnungspaar** an.                                                                                               |
| [BEZEICHNETES \_ WORT](labeled-word.md)         | Gibt ein **WORD-Bezeichnungspaar** an.                                                                                                |
| [Propertyinfo](propertyinfo.md)          | Gibt die Eigenschaften an, die der Protokollparser benötigt, um Frames zu beschreiben.                                                  |
| [PROPERTYINST](propertyinst.md)          | Gibt eine Instanz einer Eigenschaft in einem Frame an.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Gibt eine Freiforminstanz einer erweiterten Eigenschaft an.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Gibt ein Protokoll an.                                                                                                           |
| [Bereich](range.md)                        | Gibt einen Bereich für eine Zahl an.                                                                                                 |
| [SET](set.md)                            | Gibt eine Tabelle mit Werten für eine Eigenschaft an.                                                                                     |



 

Informationen zu Funktionen, die zum Entwickeln von Parser-DLLs verwendet werden, finden Sie in den folgenden Themen.



| Informationen über                                         | Finden Sie unter                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funktionen, die die Parser-DLLs exportieren.                        | [Parser-DLL-Exportfunktionen](parser-dll-export-functions.md)               |
| Funktionen, die Sie zum Entwickeln von Parser-DLLs verwenden können.            | [Parserfunktionen](parser-functions.md)                                     |
| Funktionen, die Sie zum Entwickeln von Parser- und Experten-DLLs verwenden können. | [Allgemeine Funktionen von Experten und Parsern](expert-and-parser-common-functions.md) |



 

 

 



