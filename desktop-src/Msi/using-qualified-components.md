---
description: Qualifizierte Komponenten sind eine Dekonstruktionsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Verwenden von qualifizierten Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c92d165bc06640efea4b8678eeaefa5eb04c36f1b47b6c965faeea00c66adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622946"
---
# <a name="using-qualified-components"></a>Verwenden von qualifizierten Komponenten

Qualifizierte Komponenten sind eine Dekonstruktionsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.

Um den vollständigen Pfad zurückzugeben und eine [qualifizierte Komponente](qualified-components.md)zu installieren, rufen [**Sie MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) oder [**MsiProvideQualifiedComponentEx auf.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

Um alle qualifizierten Komponentenqualifizierer und beschreibenden Zeichenfolgen aufzuzählen, rufen Sie [**MsiEnumComponentQualifiers auf.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)

**So gruppieren Sie Komponenten in einer Kategorie mit qualifizierten Komponenten**

1.  In der [Tabelle Komponente](component-table.md) muss für jede Komponente, die in der neuen Kategorie der qualifizierten Komponenten enthalten ist, ein Datensatz vorhanden sein. Erstellen Sie die Felder in der Tabelle Komponente genauso wie für gewöhnliche Komponenten. Beachten Sie, dass jede qualifizierte Komponente über eine eindeutige GUID für die Komponenten-ID verfügen muss, die in die ComponentId-Spalte der Component-Tabelle eingegeben wurde.
2.  Generieren Sie eine Qualifizierertextzeichenfolge für jede qualifizierte Komponente. Der Qualifizierer muss eine eindeutige Textzeichenfolge sein, die bei der Suche nach einer qualifizierten Komponente leicht generiert werden kann. Wenn die Komponenten in der Kategorie beispielsweise nach Sprache qualifiziert werden, ist der numerische Gebietsschemabezeichner (LCID) eine angemessene Qualifiziererzeichenfolge.
3.  Fügen Sie einen Datensatz in der [PublishComponent-Tabelle](publishcomponent-table.md) für jede qualifizierte Komponente hinzu. Geben Sie die Bezeichner der qualifizierten Komponente aus der Spalte Komponente der Tabelle Komponente in die Spalte Komponente \_ der PublishComponent-Tabelle ein. Geben Sie die Qualifiziererzeichenfolgen für jede qualifizierte Komponente in die Spalte Qualifizierer ein. Geben Sie eine lokalisierte Zeichenfolge ein, die dem Benutzer angezeigt werden soll, und beschreiben Sie die qualifizierte Komponente in der optionalen Spalte AppData. Eine erläuternde Zeichenfolge sollte in das Feld AppData eingefügt werden, z. B. "Französisches Wörterbuch", anstatt nur die numerische LCID. Geben Sie den Namen des Features, das diese Komponente verwendet, in die Spalte Feature \_ ein. Der Featurebezeichner in diesem Feld muss auch in der Spalte Feature der [Featuretabelle](feature-table.md)aufgeführt werden.
4.  Generieren Sie eine Kategorie-GUID für diese Kategorie von qualifizierten Komponenten. Dies muss eine gültige [GUID](guid.md)sein. Wenn Sie ein Hilfsprogramm wie GUIDGEN verwenden, um die GUID zu generieren, stellen Sie sicher, dass sie nur Großbuchstaben enthält. Geben Sie für jede qualifizierte Komponente in dieser Kategorie die Kategorie-GUID in das Feld ComponentId der [PublishComponent-Tabelle](publishcomponent-table.md)ein.

Im folgenden Beispiel wird veranschaulicht, wie die Kategorie "FAX-Vorlagen" der qualifizierten Komponenten in den Tabellen Component, Feature und PublishComponent erstellt wird.

[PublishComponent-Tabelle](publishcomponent-table.md)



| Componentid                  | Qualifizierer | AppData             | Feature\_   | Komponente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {FAX Template Category GUID} | 1033      | Vorlage für Englisch (USA) | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Japanische Vorlage   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Thailändische Vorlage       | FAXTemplate | FAXTemplateKOPIE |
|                              | 1031      | Vorlage "Deutsch"     | FAXTemplate | FAXTemplateDEU |



 

[Komponententabelle](component-table.md) (partielle Tabelle)



| Komponente      | Componentid                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*FAX Template (US English) component GUID*} |
| FAXTemplateJPN | {*FAX Template (Japanese) component GUID*}   |
| FAXTemplateKOPIE | {*FAX Template (Thai) component GUID*}       |
| FAXTemplateDEU | {*FAX Template (German) component GUID*}     |



 

[Featuretabelle](feature-table.md) (partielle Tabelle)



| Funktion     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



