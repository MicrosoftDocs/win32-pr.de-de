---
title: Anmerkungssteuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IAnnotationProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Annotation-Steuerelementmuster wird verwendet, um die Eigenschaften einer Anmerkung in einem Dokument verfügbar zu machen.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Anmerkungssteuerelementmusters
- Benutzeroberflächenautomatisierung,Anmerkungssteuerelementmuster
- Benutzeroberflächenautomatisierung,IAnnotationProvider
- IAnnotationProvider
- Implementieren Benutzeroberflächenautomatisierung Anmerkungssteuerelementmusters
- Anmerkungssteuerelementmuster
- Steuerelementmuster,IAnnotationProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Anmerkung
- Steuerelementmuster,Anmerkung
- interfaces,IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cdc5c37c61878513b5d01812ab73c086f87d182d4b2c955efaf8706d52e4bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505255"
---
# <a name="annotation-control-pattern"></a>Anmerkungssteuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IAnnotationProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Annotation-Steuerelementmuster** wird verwendet, um die Eigenschaften einer Anmerkung in einem Dokument verfügbar zu machen.

Ein Beispiel ist ein Kommentarsprechblasen, der sich am Rand eines Dokuments befindet und mit einem Dokumenttext oder einer Tabellenkalkulationszelle verbunden ist.

Die folgende Abbildung zeigt ein Beispiel für eine Anmerkung. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

![Screenshot eines Kommentarbaluns in einem Dokument](images/annotation.png)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Annotation-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Es gibt viele verschiedene Arten von Anmerkungen. Die Headerdatei UIAutomationClient.h definiert einen Satz benannter konstanter Werte, die die Von Microsoft Benutzeroberflächenautomatisierung unterstützten Anmerkungstypen identifizieren. Weitere Informationen finden Sie unter [**Anmerkungstypbezeichner.**](uiauto-annotation-type-identifiers.md)
-   Wenn Sie [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md)verwenden, müssen Sie die [**IAnnotationProvider::AnnotationTypeName-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) implementieren, damit Clients den Namen des Anmerkungstyps ermitteln können. Sie müssen **AnnotationTypeName** nicht für einen Standardanmerkungstyp implementieren, da Benutzeroberflächenautomatisierung einen Standardnamen bereitstellt. Sie können ihn jedoch implementieren, wenn Sie den Standardnamen überschreiben müssen.
-   Die [**IAnnotationProvider::Author-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) ist optional.
-   Die [**IAnnotationProvider::D ateTime-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) ist optional.
-   Die [**IAnnotationProvider::Target-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) ist erforderlich, da sie eine Anmerkung mit einem Benutzeroberflächenelement verknüpft, sodass ein Client von der Anmerkung zurück zum Benutzeroberflächenelement navigiert, auf das die Anmerkung verweist.
-   Da Anmerkungen viele verschiedene Formen annehmen können, definiert die [**IAnnotationProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) keine Eigenschaft zum Speichern des Werts oder Texts einer Anmerkung. Eine einfache Anmerkung sollte die [**IValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) verfügbar machen, und die [**IValueProvider::Value-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) sollte einen schreibgeschützten Wert zurückgeben, der den Anmerkungstext angibt. Eine umfangreichere Anmerkung sollte die [**ITextProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) verfügbar machen, um Clients umfangreicheren Text bereitzustellen.
-   Das Navigieren von einem Benutzeroberflächenelement zu einer Anmerkung für das Element hängt wie folgt von der Art des Elements ab, das mit Anmerkungen versehen wird:
    -   Implementieren Sie für Tabellenzellen die [**ISpreadsheetItemProvider::GetAnnotationObjects-Methode,**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) um auf die Anmerkung zu verweisen.
    -   Implementieren Sie für Textinhalt das Textattribut [**AnnotationObjects**](uiauto-textattribute-ids.md) auf der [**ITextRangeProvider-Schnittstelle,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) um auf die Anmerkung zu verweisen.
-   Einige Arten von Anmerkungen erfordern keine vollständige Implementierung der [**IAnnotationProvider-Schnittstelle.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Beispielsweise kann ein einfacher Rechtschreibfehlerindikator dargestellt werden, indem die [**ITextRangeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ein [**AnnotationTypes-Textattribut**](uiauto-textattribute-ids.md) von [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)und einen NULL-Wert für das Textattribut [**AnnotationObjects**](uiauto-textattribute-ids.md) zurückgibt.
-   Es kann hilfreich sein, die [**IAnnotationProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) für ein benutzeroberflächenelement zu implementieren, das nicht sichtbar ist. Beispielsweise können Sie ein nicht sichtbares Benutzeroberflächenautomatisierung-Element erstellen, das **IAnnotationProvider** implementiert, um erweiterte Informationen zu einem Grammatikfehler bereitzustellen.
-   Anmerkungen in einem textbasierten Steuerelement können komplex sein, wenn das Steuerelement überlappende Kommentare enthält. Verwenden Sie die folgenden Richtlinien, um komplexe Anmerkungen zu behandeln:
    -   Ein Textbereich ohne Anmerkungen sollte ein leeres Array für das Textattribut [**AnnotationTypes**](uiauto-textattribute-ids.md) und ein leeres Array für das Textattribut [**AnnotationObjects**](uiauto-textattribute-ids.md) zurückgeben.
    -   Ein Textbereich mit einer Anmerkung sollte ein Array mit einem ganzzahligen Wert für das Textattribut [**AnnotationTypes**](uiauto-textattribute-ids.md) und ein Array einer [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für das Textattribut [**AnnotationObjects**](uiauto-textattribute-ids.md) zurückgeben.
    -   Ein Textbereich mit mehreren Anmerkungen sollte ein Array mit mehreren ganzzahligen Werten für das Textattribut [**AnnotationTypes**](uiauto-textattribute-ids.md) und ein Array mit einer übereinstimmenden Anzahl von [**IRawElementProviderSimple-Schnittstellen**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) für das Textattribut [**AnnotationObjects**](uiauto-textattribute-ids.md) zurückgeben.
    -   Ein Textbereich mit unterschiedlichen Anmerkungen, z. B. ein Bereich mit textbeschriftetem und nicht kommentiertem Text, sollte die [**ReservedMixedAttributeValue-Eigenschaft**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) sowohl für [**AnnotationTypes**](uiauto-textattribute-ids.md) als auch [**für AnnotationObjects**](uiauto-textattribute-ids.md)zurückgeben. Ein Client, der diese Antwort empfängt, kann den Textbereich unterteilen, um zu ermitteln, wo die Anmerkungen beginnen und enden.

## <a name="required-members-for-iannotationprovider"></a>Erforderliche Member für **IAnnotationProvider**

Die folgenden Eigenschaften sind für die Implementierung der [**IAnnotationProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) erforderlich.



| Erforderliche Member                                                                | Memberart | Hinweise |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Eigenschaft    | Keine. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Eigenschaft    | Keine. |
| [**Autor**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Eigenschaft    | Keine. |
| [**Datetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Eigenschaft    | Keine. |
| [**Ziel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Eigenschaft    | Keine. |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 