---
description: Qualifizierte Komponenten sind eine dereferenzierungsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Verwenden qualifizierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129357"
---
# <a name="using-qualified-components"></a>Verwenden qualifizierter Komponenten

Qualifizierte Komponenten sind eine dereferenzierungsmethode und können verwendet werden, um Komponenten mit paralleler Funktionalität in Kategorien zu gruppieren.

Um den vollständigen Pfad zurückzugeben und eine [qualifizierte Komponente](qualified-components.md)zu installieren, nennen Sie [**msiprovidequalifiedcomponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) oder [**msiprovidequalifiedcomponstex**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Um alle qualifizierten Komponenten Qualifizierer und beschreibenden Zeichen folgen aufzulisten, müssen Sie [**msienumcomponentqualifizierer**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)aufzurufen.

**So gruppieren Sie Komponenten in einer Kategorie qualifizierter Komponenten**

1.  In der [Komponenten Tabelle](component-table.md) muss für jede Komponente, die in der neuen Kategorie qualifizierter Komponenten enthalten ist, ein Datensatz vorhanden sein. Erstellen Sie die Felder in der Komponenten Tabelle wie für normale Komponenten. Beachten Sie, dass für jede qualifizierte Komponente eine eindeutige GUID für die Komponenten-ID in der Spalte ComponentID der Komponenten Tabelle eingegeben werden muss.
2.  Generiert eine Qualifiziererzeichenfolge für jede qualifizierte Komponente. Der Qualifizierer muss eine eindeutige Text Zeichenfolge sein, die bei der Suche nach einer qualifizierten Komponente problemlos generiert werden kann. Wenn z. b. die Komponenten in der Kategorie durch Sprache qualifiziert werden, ist der numerische Gebiets Schema Bezeichner (Locale Identifier, LCID) eine sinnvolle Qualifiziererzeichenfolge.
3.  Fügen Sie für jede qualifizierte Komponente einen Datensatz in der [Tabelle PublishComponent](publishcomponent-table.md) hinzu. Geben Sie die qualifizierten Komponenten Bezeichner aus der Spalte Komponente der Komponenten Tabelle in die Spalte Komponente \_ der Tabelle PublishComponent ein. Geben Sie die Qualifiziererzeichenfolgen für jede qualifizierte Komponente in die qualifiziererspalte Geben Sie eine lokalisierte Zeichenfolge ein, die dem Benutzer angezeigt werden soll, und beschreiben Sie die qualifizierte Komponente in der optionalen APPDATA-Spalte. Eine erklärende Zeichenfolge sollte in das APPDATA-Feld eingefügt werden, z. b. "Französisch Wörterbuch", anstelle der numerischen LCID. Geben Sie den Namen der Funktion ein, von der diese Komponente in der featurespalte verwendet wird \_ . Der Funktions Bezeichner in diesem Feld muss auch in der featurespalte der [Featuretabelle](feature-table.md)aufgeführt werden.
4.  Generieren Sie eine Kategorie-GUID für diese Kategorie qualifizierter Komponenten. Dies muss eine gültige [GUID](guid.md)sein. Wenn Sie ein Hilfsprogramm wie GUIDGEN zum Generieren der GUID verwenden, müssen Sie sicherstellen, dass es nur Großbuchstaben enthält. Geben Sie für jede qualifizierte Komponente in dieser Kategorie die Kategorie-GUID in das Feld ComponentID der [Tabelle PublishComponent](publishcomponent-table.md)ein.

Im folgenden Beispiel wird veranschaulicht, wie die Kategorie "Faxvorlagen" qualifizierter Komponenten in den Tabellen "Komponente", "Feature" und "PublishComponent" verfasst wird.

[PublishComponent-Tabelle](publishcomponent-table.md)



| ComponentID                  | Qualifizierer | AppData             | Funktion\_   | Komponente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {Faxvorlagen Kategorie GUID} | 1033      | US-englische Vorlage | Faxvorlage | Faxtemplatedeu |
|                              | 1041      | Japanische Vorlage   | Faxvorlage | Faxtemplatejpn |
|                              | 1054      | Thailändische Vorlage       | Faxvorlage | Faxtemplatetha |
|                              | 1031      | Deutsche Vorlage     | Faxvorlage | Faxtemplatedeu |



 

[Komponenten Tabelle](component-table.md) (partielle Tabelle)



| Komponente      | ComponentID                                  |
|----------------|----------------------------------------------|
| Faxtemplatedeu | {*Faxvorlage (US-Englisch) Komponenten-GUID*} |
| Faxtemplatejpn | {*Faxvorlage (Japanisch) Komponenten-GUID*}   |
| Faxtemplatetha | {*Faxvorlage (Thai)-Komponenten-GUID*}       |
| Faxtemplatedeu | {*Faxvorlage (Deutsch), Komponenten-GUID*}     |



 

[Funktions Tabelle](feature-table.md) (partielle Tabelle)



| Funktion     |
|-------------|
| Faxvorlage |
| Faxvorlage |
| Faxvorlage |
| Faxvorlage |



 

 

 



