---
description: 'Windows Vista und höher: NLS definiert mehrere Pseudo-Locales, die zusätzlich zu den vorhandenen lokalen Windows verwendet werden können.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e099ee2af283c38aff3de7813fec64b5d43c6ac5873549856b27fd224c3e0d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390414"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista und höher:** NLS definiert mehrere Pseudo-Locales, die zusätzlich zu den vorhandenen lokalen Windows verwendet werden können. Verwenden Sie diese Pseudo-Locales, um die Lokalisierung Ihrer Anwendungen zu testen. Implementierungsdetails finden Sie unter Using Pseudo-Locales for Localization Testing (Verwenden [von Pseudo-Locales für Lokalisierungstests).](using-pseudo-locales-for-localization-testing.md)

## <a name="supported-pseudo-locales"></a>Unterstützte Pseudo-Locales

Die von NLS unterstützten Pseudo-Locales sind:

-   Basis-Pseudo-Locale
-   Gespiegelte Pseudo-Locale (von rechts nach links)
-   Pseudo-Locale in ostasiatischer Sprache

Wählen Sie das bestimmte Pseudo-Locale aus, das basierend auf den Codepagezuweisungen und den Zeichenfolgen für die Lokalisierung verwendet werden soll, z. B. Monatsnamen, Tagnamen. Die Daten für jedes Pseudo-Locale enthalten nicht nur relevante Codepages und Tag- und Monatszeichenfolgen für die Lokalisierung, sondern auch Daten für mehrere andere Testfälle für NLS. In den Testfällen werden die folgenden Datentypen untersucht:

-   [9-Bit-Locale-Bezeichner.](locale-identifiers.md) Pseudo-Locales bieten eine gute Möglichkeit, den Betrieb von 9-Bit-Locale-Bezeichnern zu testen.
-   Zeichenfolgen aus Sprachen, die kleine Schriftarten verwenden müssen. Aufgrund von Einschränkungen in der Grafikgeräteschnittstelle (GDI) ist die Schriftart der Benutzeroberfläche für einige Sprachen kleiner als optimal. Pseudo-Locales enthalten mehrere Zeichenfolgen aus diesen Sprachen, kombiniert mit Zeichenfolgen aus Sprachen mit einer standarderen Schriftartbehandlung. Sie können diese Zeichenfolgen beim Testen verwenden, um zu bestimmen, wie eine GDI-eingeschränkte Schriftart gerendert wird.
-   Ungewöhnliche Zeichenfolgenlängen. Einige Locale Information-Konstanten, z. B. [LOCALE \_ SLIST](locale-slist.md) und [LOCALE \_ ICURRENCY,](locale-icurrency.md)haben konventionelle Grenzwerte für die Zeichenfolgengröße. Die Pseudo-Locales unterstützen die Untersuchung unterschiedlicher Zeichenfolgenlängen.
-   Alternative Sortierungen. Pseudo-Locales können verwendet werden, um alternative [](sort-order-identifiers.md) Sortierfunktionen zu testen, wenn sich der bezeichner der alternativen Sortierreihenfolge von dem Basisbezeichner der Sortierreihenfolge unterscheidet, der normalerweise dem -Locale zugeordnet ist.

## <a name="pseudo-locale-names-and-identifiers"></a>Pseudo-locale Names and Identifiers

Die Pseudogebietsgebietsnamen verfügen über [Locale-Namen,](locale-names.md) die aus dem privaten Verwendungsraum ausgewählt werden, um Konflikte mit möglichen Zeichenfolgen zu vermeiden, die in die standards Internationale Organisation für Normung (ISO) 639 und ISO 3166 eingeführt wurden. Jedes Pseudo-Locale verfügt auch über einen eigenen Locale-Bezeichner. Die folgende Tabelle enthält die Namen und Bezeichner für die definierten Pseudo-Locales.



| Pseudo-Locale       | Name des Locale | Locale Identifier |
|---------------------|-------------|-------------------|
| Basis                | qps-ploc    | 0501              |
| Gespiegelt            | qps-sollcm   | 09ff              |
| Ostasiatische Sprache | qps-dochca   | 05fe              |



 

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt Text, der für ein Basis-Pseudo-Locale angezeigt wird:

\[Шěđлеśđαỳ !!! , \] 8 ): \[ Μäŕςћ © ' \] 2006

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokal und Sprachen](locales-and-languages.md)
</dt> <dt>

[Locale Identifiers](locale-identifiers.md)
</dt> <dt>

[Locale Names](locale-names.md)
</dt> <dt>

[Bezeichner der Sortierreihenfolge](sort-order-identifiers.md)
</dt> <dt>

[Verwenden Pseudo-Locales für Lokalisierungstests](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



