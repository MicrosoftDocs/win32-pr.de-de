---
description: In diesem Abschnitt werden die Strukturen beschrieben, die Sie zum Entwickeln von-Parser verwenden können. Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie verwenden können, um entweder Parser oder Experten zu entwickeln.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Parserstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961001"
---
# <a name="parser-structures"></a>Parserstrukturen

In diesem Abschnitt werden die Strukturen beschrieben, die Sie zum Entwickeln von-Parser verwenden können. Diese Strukturen werden von Funktionen verwendet, die Sie verwenden können, um Parser und Funktionen zu entwickeln, die Sie verwenden können, um entweder Parser oder Experten zu entwickeln.



| Struktur                                 | BESCHREIBUNG                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Macframe](macframe.md)                  | Definiert die am häufigsten verwendeten anfänglichen Protokolle.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Gibt Zeiger auf die Einstiegspunkte für die Parser-DLL an.                                                                      |
| [PF-nach \_ Verfolgung](pf-followentry.md)     | Gibt das Protokoll an, das auf das aktuelle Protokoll folgt.                                                                       |
| [PF-nach \_ Verfolgung](pf-followset.md)         | Gibt die Gruppe von Protokollen an, die auf das aktuelle Protokoll folgt.                                                               |
| [PF- \_ handoffentry](pf-handoffentry.md)   | Gibt entweder das Protokoll an, das das aktuelle Protokoll übergibt, oder das Protokoll, an das das aktuelle Protokoll übergibt.    |
| [PF- \_ handoffset](pf-handoffset.md)       | Gibt den Satz von Protokollen an, die an das aktuelle Protokoll oder den Satz von Protokollen übergeben werden, an die das aktuelle Protokoll übergibt. |
| [PF- \_ Parser (Parser)](pf-parserdllinfo.md) | Gibt die Anzahl der Parser in der Parser-DLL und die Informationen zu den einzelnen Parser an.                                            |
| [PF-Parameter \_ Info](pf-parserinfo.md)       | Gibt Informationen zu einem bestimmten Parser an.                                                                                  |
| [beschriftetes \_ Bit](labeled-bit.md)           | Gibt Handles, Bitfelder oder Flags an.                                                                                        |
| [beschriftete \_ Byte](labeled-byte.md)         | Gibt ein **Byte** Bezeichnungs Paar an.                                                                                                |
| [gekennzeichnete \_ DWORD](labeled-dword.md)       | Gibt ein **DWORD** -Bezeichnungs Paar an.                                                                                               |
| [gekennzeichnete \_ Word](labeled-word.md)         | Gibt ein **Wort** Bezeichnungs Paar an.                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | Gibt die Eigenschaften an, die der Protokoll Parser zum Beschreiben von Frames benötigt.                                                  |
| [Propertyinst](propertyinst.md)          | Gibt eine Instanz einer Eigenschaft in einem Frame an.                                                                                 |
| [Propertyinstex](propertyinstex.md)      | Gibt eine frei Form erweiterte Eigenschafts Instanz an.                                                                              |
| [Protocolinfo](protocolinfo.md)          | Gibt ein Protokoll an.                                                                                                           |
| [Bereich](range.md)                        | Gibt einen Bereich für eine Zahl an.                                                                                                 |
| [SET](set.md)                            | Gibt eine Tabelle mit Werten für eine Eigenschaft an.                                                                                     |



 

Informationen zu den Funktionen, die zum Entwickeln von Parser-DLLs verwendet werden, finden Sie in den folgenden Themen.



| Informationen über                                         | Finden Sie unter                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funktionen, die vom Parser exportiert werden.                        | [Export Funktionen der Parser-DLL](parser-dll-export-functions.md)               |
| Funktionen, die Sie verwenden können, um Parser-DLLs zu entwickeln.            | [Parser-Funktionen](parser-functions.md)                                     |
| Funktionen, die Sie verwenden können, um Parser-und Experten-DLLs zu entwickeln. | [Allgemeine Funktionen für Experten und Parser](expert-and-parser-common-functions.md) |



 

 

 



