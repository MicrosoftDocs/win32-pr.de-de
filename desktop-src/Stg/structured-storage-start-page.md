---
title: Strukturierter Speicher
description: Die strukturierte Speicherung bietet Datei-und Daten Persistenz in com, indem eine einzelne Datei als strukturierte Auflistung von Objekten behandelt wird, die als Speicher und Streams bezeichnet werden.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strukturierter Speicherplatz-STG
- Strukturierter Speicherplatz Halter-STG, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315705"
---
# <a name="structured-storage"></a>Strukturierter Speicher

## <a name="purpose"></a>Zweck

Die strukturierte Speicherung bietet Datei-und Daten Persistenz in com, indem eine einzelne Datei als strukturierte Auflistung von Objekten behandelt wird, die als Speicher und Streams bezeichnet werden.

Der Zweck der strukturierten Speicherung besteht darin, die Leistungseinbußen und den Aufwand für das Speichern von separaten Objekten in einer einzelnen Datei zu verringern. Die strukturierte Speicherung bietet eine Lösung, indem definiert wird, wie eine einzelne Datei Entität als strukturierte Auflistung von zwei Typen von Objekten verarbeitet und durch eine Standard Implementierung mit dem Namen "Verbund Dateien" gestreamt wird. Dies ermöglicht es dem Benutzer, mit einer Verbund Datei zu interagieren und diese zu verwalten, als ob es sich um eine einzelne Datei und nicht um eine geschachtelte Hierarchy von separaten Objekten handelt.

## <a name="where-applicable"></a>Anwendungsbereich

Strukturierter Speicher kann auf Microsoft com-basierten Betriebssystemen verwendet werden.

## <a name="developer-audience"></a>Entwicklergruppe

Die strukturierte Speicher Dokumentation ist für erfahrene C-und C++-Programmierer und com-basierte Systementwickler gedacht.

Die strukturierte Speicherung unterstützt hauptsächlich C-und C++-Programmiersprachen, aber alle COM-basierten Technologien unterstützen auch jede Programmiersprache, die Schnittstellen Zeiger verwendet.

Ein solides Verständnis der com-Technologien ist eine Voraussetzung für die Entwicklungs Verwendung von strukturiertem Speicher.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Weitere Informationen zu den Betriebssystemen, die für die Verwendung eines bestimmten API-Elements erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für das-Element.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Übersicht](about-structured-storage.md)<br/>                 | Allgemeine Informationen über die strukturierte Speicherung.<br/>                                                                                                                                                                                                                                                 |
| [Verwenden von strukturierter Speicherung](using-structured-storage.md)<br/> | Verwenden von Informationen für die strukturierte Speicherung.<br/>                                                                                                                                                                                                                                                     |
| [Verweis](structured-storage-reference.md)<br/>            | Dokumentation zu strukturierten Speicher spezifischen Schnittstellen, Funktionen, Strukturen und Enumerationen.<br/>                                                                                                                                                                                             |
| [Beispiele](samples.md)<br/>                                   | In C++ geschriebene Code Beispiele. Weitere Informationen finden Sie unter [Namen in IStorage](names-in-istorage.md), [Eigenschaften Satz Header](property-set-header.md), [Abschnitt](section.md), [Speichern von Eigenschafts Sätzen](storing-property-sets.md)und [Verwenden von strukturiertem Speicher](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Component Object Model](../com/the-component-object-model.md)
</dt> </dl>

 

