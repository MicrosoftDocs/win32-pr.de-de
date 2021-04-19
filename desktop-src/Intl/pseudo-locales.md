---
description: 'Windows Vista und höher: nls definiert mehrere Pseudo Gebiets Schemas, die zusätzlich zu den vorhandenen Windows-Gebiets Schemas verwendet werden können.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346927"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista und höher:** NLS definiert mehrere Pseudo Gebiets Schemas, die zusätzlich zu den vorhandenen Windows-Gebiets Schemas verwendet werden können. Verwenden Sie diese Pseudo Gebiets Schemas, um die Lokalisierung Ihrer Anwendungen zu testen. Implementierungsdetails finden Sie unter [Verwenden von Pseudo-Locales für Lokalisierungstests](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Unterstützte Pseudo-Locales

Folgende Pseudo Gebiets Schemas werden von NLS unterstützt:

-   Basis Pseudo Gebiets Schema
-   Gespiegeltes (von rechts nach links) Pseudo Gebiets Schema
-   Pseudo Gebiets Schema der ostasiatischen Sprache

Wählen Sie das jeweilige zu verwendende Pseudo Gebiets Schema basierend auf den Code Page Zuweisungen und den Zeichen folgen für die Lokalisierung aus, z. b. Monatsnamen, Tagnamen. Die Daten für die einzelnen Pseudo Gebiets Schemas umfassen nicht nur relevante Codepages und Tages-und Monats Zeichenfolgen für die Lokalisierung, sondern auch Daten für verschiedene andere Testfälle für NLS. In den Testfällen werden die folgenden Datentypen untersucht:

-   9 [-Bit-](locale-identifiers.md)Gebiets Schema Bezeichner. Pseudo Gebiets Schemata bieten eine gute Möglichkeit, den Vorgang von 9-Bit-Gebiets Schema Bezeichners zu testen.
-   Zeichen folgen aus Sprachen, die kleine Schriftarten verwenden müssen. Aufgrund von Einschränkungen in der Graphics Device Interface (GDI) ist die Schriftart der Benutzeroberfläche für einige Sprachen kleiner als optimal. Pseudo Gebiets Schemas enthalten mehrere Zeichen folgen aus diesen Sprachen, kombiniert mit Zeichen folgen aus Sprachen mit mehr Standard Schriftart Behandlung. Sie können diese Zeichen folgen beim Testen verwenden, um zu bestimmen, wie eine GDI-begrenzte Schriftart gerendert wird.
-   Ungewöhnliche Zeichen folgen Längen. Einige Gebiets Schema Informations Konstanten, z. b. [locale \_ slist](locale-slist.md) und [locale \_ icurrency](locale-icurrency.md), haben konventionelle Grenzwerte für die Zeichen folgen Größe. Die Pseudo Gebiets Schemas unterstützen die Untersuchung unterschiedlicher Zeichen folgen Längen.
-   Alternative Sortierungen. Mithilfe von Pseudo Gebiets Schemas können alternative Sortierfunktionen getestet werden, wenn sich der Alternative [Sortier Auftrags Bezeichner](sort-order-identifiers.md) von der ID der Basis Sortierreihenfolge unterscheidet, die normalerweise dem Gebiets Schema zugeordnet ist.

## <a name="pseudo-locale-names-and-identifiers"></a>Pseudo Gebiets Schema-Namen und-Bezeichner

Die Pseudo Gebiets Schemas verfügen über Gebiets Schema [Namen](locale-names.md) , die aus dem privaten Verwendungsbereich ausgewählt werden, um Konflikte mit möglichen Zeichen folgen zu vermeiden, internationale Organisation für Normung die in die Standards 639 (ISO) und ISO 3166 eingeführt werden. Jedes Pseudo Gebiets Schema hat auch seinen eigenen Gebiets Schema Bezeichner. In der folgenden Tabelle finden Sie die Namen und Bezeichner für die definierten Pseudo Gebiets Schemas.



| Pseudo Gebiets Schema       | Gebiets Schema Name | Gebiets Schema Bezeichner |
|---------------------|-------------|-------------------|
| Basis                | QPS-ploc    | 0501              |
| Gespiegelt            | QPS-plocm   | 09FF              |
| Ostasiatische Sprache | QPS-Ploca   | 05fe              |



 

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt Text, der für ein basispseudo Gebiets Schema angezeigt wird:

\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[Gebiets Schema Bezeichner](locale-identifiers.md)
</dt> <dt>

[Gebiets Schema Namen](locale-names.md)
</dt> <dt>

[Sortierreihenfolge-IDs](sort-order-identifiers.md)
</dt> <dt>

[Verwenden von Pseudo-Locales für Lokalisierungstests](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



