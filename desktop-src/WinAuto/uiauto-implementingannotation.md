---
title: Annotation-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von iannotationprovider, einschließlich Informationen zu Eigenschaften und Methoden. Das Anmerkung-Steuerelement Muster wird verwendet, um die Eigenschaften einer Anmerkung in einem Dokument verfügbar zu machen.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Benutzeroberflächenautomatisierungs-Steuerelement Muster implementieren
- Benutzeroberflächenautomatisierungs-Steuerelement Muster
- UI-Automatisierung, iannotationprovider
- IAnnotationProvider
- Implementieren des Steuerelement Musters der Benutzeroberflächenautomatisierungs-Anmerkung
- Anmerkung-Steuerelement Muster
- Steuerelement Muster, iannotationprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Anmerkung
- Steuerelement Muster, Anmerkung
- Schnittstellen, iannotationprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a0441816e548faaa9076b3a9717c0aa76f08a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340922"
---
# <a name="annotation-control-pattern"></a>Annotation-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Anmerkung** -Steuerelement Muster wird verwendet, um die Eigenschaften einer Anmerkung in einem Dokument verfügbar zu machen.

Ein Beispiel hierfür ist eine Kommentar Sprechblase, die sich am Rand eines Dokuments befindet und mit einem Dokument Text oder einer Tabellen Kalkulations Zelle verbunden ist.

Die folgende Abbildung zeigt ein Beispiel für eine Anmerkung. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

![Screenshot mit einem Kommentar baloon in einem Dokument](images/annotation.png)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **iannotationprovider**](#required-members-for-iannotationprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Annotation** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Es gibt viele verschiedene Arten von Anmerkungen. Die UIAutomationClient. h-Header Datei definiert einen Satz benannter konstanter Werte, die die Typen von Anmerkungen identifizieren, die von der Microsoft-Benutzeroberflächen Automatisierung unterstützt werden. Weitere Informationen finden Sie unter [**Annotation-Typbezeichner**](uiauto-annotation-type-identifiers.md).
-   Wenn Sie den [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md)verwenden, müssen Sie die [**iannotationprovider:: annotationtykame**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) -Eigenschaft implementieren, damit Clients den Namen des Anmerkung-Typs ermitteln können. Es ist nicht erforderlich, dass Sie für einen Standard Anmerkung-Typ " **annotationtykame** " implementieren, da die Benutzeroberflächen Automatisierung einen Standardnamen bereitstellt. Sie können ihn jedoch implementieren, wenn Sie den Standardnamen überschreiben müssen.
-   Die [**iannotationprovider:: Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) -Eigenschaft ist optional.
-   Die [**iannotationprovider::D atetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) -Eigenschaft ist optional.
-   Die [**iannotationprovider:: Target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) -Eigenschaft ist erforderlich, da Sie eine Anmerkung mit einem UI-Element verknüpft, sodass ein Client von der Anmerkung zurück zum Benutzeroberflächen Element navigieren kann, auf das die Anmerkung verweist.
-   Da Anmerkungen viele verschiedene Formulare annehmen können, definiert die [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle keine Eigenschaft zum Speichern des Werts oder Texts einer Anmerkung. Eine einfache Anmerkung sollte die [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) -Schnittstelle verfügbar machen, und die [**IValueProvider:: Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) -Eigenschaft sollte einen schreibgeschützten Wert zurückgeben, der den Text der Anmerkung angibt. Eine umfangreichere Anmerkung sollte die [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) -Schnittstelle verfügbar machen, um den Clients einen umfassenderen Text bereitzustellen.
-   Die Navigation von einem Benutzeroberflächen Element zu einer Anmerkung auf dem Element hängt wie folgt von der Art des Elements ab, das mit Anmerkungen versehen wird:
    -   Implementieren Sie für Tabellenzellen die [**ispreadsheetitemprovider:: getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) -Methode, um auf die-Anmerkung zu verweisen.
    -   Implementieren Sie für Textinhalte das [**annotationobjects**](uiauto-textattribute-ids.md) -Text Attribut in der [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle, um auf die-Anmerkung zu verweisen.
-   Einige Arten von Anmerkungen erfordern keine vollständige Implementierung der [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle. Ein einfacher Rechtschreibfehler Indikator könnte z. b. dargestellt werden, indem die [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) -Schnittstelle ein [**annotationtypes**](uiauto-textattribute-ids.md) -Text Attribut von [**AnnotationType " \_ SpellingError**](uiauto-annotation-type-identifiers.md)" und einen NULL-Wert für das [**annotationobjects**](uiauto-textattribute-ids.md) -Text Attribut zurückgibt.
-   Es kann nützlich sein, die [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle für ein nicht sichtbares UI-Element zu implementieren. Beispielsweise können Sie ein nicht sichtbares Benutzeroberflächenautomatisierungs-Element erstellen, das **iannotationprovider** implementiert, um erweiterte Informationen über einen Grammatikfehler bereitzustellen.
-   Anmerkungen in einem textbasierten Steuerelement können komplex sein, wenn das Steuerelement überlappende Kommentare enthält. Verwenden Sie die folgenden Richtlinien, um komplexe Anmerkungen zu behandeln:
    -   Ein Textbereich ohne Anmerkungen sollte ein leeres Array für das [**annotationtypes**](uiauto-textattribute-ids.md) -Text Attribut und ein leeres Array für das [**annotationobjects**](uiauto-textattribute-ids.md) -Text Attribut zurückgeben.
    -   Ein Textbereich mit einer Anmerkung muss ein Array mit einem ganzzahligen Wert für das [**annotationtypes**](uiauto-textattribute-ids.md) -Text Attribut und ein Array mit einer [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle für das [**annotationobjects**](uiauto-textattribute-ids.md) -Text Attribut zurückgeben.
    -   Ein Textbereich mit mehreren Anmerkungen muss ein Array mit mehreren ganzzahligen Werten für das [**annotationtypes**](uiauto-textattribute-ids.md) -Text Attribut und ein Array mit einer übereinstimmenden Anzahl von [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstellen für das [**annotationobjects**](uiauto-textattribute-ids.md) -Text Attribut zurückgeben.
    -   Ein Textbereich mit abweichenden Anmerkungen, wie z. b. ein Bereich mit mit Anmerkungen versehene und nicht mit Anmerkungen versehene Text, sollte die [**reservedmixedattributevalue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) -Eigenschaft für " [**annotationtypes**](uiauto-textattribute-ids.md) " und " [**annotationobjects**](uiauto-textattribute-ids.md)" zurückgeben. Ein Client, der diese Antwort empfängt, kann den Textbereich unterteilen, um zu ermitteln, wo die Anmerkungen beginnen und enden.

## <a name="required-members-for-iannotationprovider"></a>Erforderliche Member für **iannotationprovider**

Die folgenden Eigenschaften sind erforderlich, um die [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle zu implementieren.



| Erforderliche Member                                                                | Memberart | Hinweise |
|---------------------------------------------------------------------------------|-------------|-------|
| [**Annotationtypeid**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Eigenschaft    | Keine. |
| [**Annotationtypame**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Eigenschaft    | Keine. |
| [**Autor**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Eigenschaft    | Keine. |
| [**DateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Eigenschaft    | Keine. |
| [**Ziel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Eigenschaft    | Keine. |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 