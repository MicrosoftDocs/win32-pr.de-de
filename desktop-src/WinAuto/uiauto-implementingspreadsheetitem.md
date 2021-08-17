---
title: SpreadsheetItem-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ISpreadsheetItemProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des SpreadsheetItem-Steuerelementmusters
- Benutzeroberflächenautomatisierung,SpreadsheetItem-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- Implementieren Benutzeroberflächenautomatisierung SpreadsheetItem-Steuerelementmusters
- SpreadsheetItem-Steuerelementmuster
- Steuerelementmuster,ISpreadsheetItemProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung SpreadsheetItem
- Steuerelementmuster, SpreadsheetItem
- interfaces,ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d5feaa32b5fe79635c6acc01e1e0b18b9ba77c382ba3f07c64f7cb3e921b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324370"
---
# <a name="spreadsheetitem-control-pattern"></a>SpreadsheetItem-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von ISpreadsheetItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **SpreadsheetItem-Steuerelementmuster** wird verwendet, um die Eigenschaften einer Zelle in einem Arbeitsblatt oder einem anderen rasterbasierten Dokument verfügbar zu machen.

Das **SpreadsheetItem-Steuerelementmuster** ist eng mit dem [GridItem-Steuerelementmuster](uiauto-implementinggriditem.md) verknüpft. -Steuerelemente, die das **SpreadsheetItem-Steuerelementmuster** implementieren, sollten auch das GridItem-Steuerelementmuster implementieren. Steuerelemente können gegebenenfalls auch [das TableItem-Steuerelementmuster](uiauto-implementingtableitem.md) implementieren. Beispiele für Steuerelemente, die diese Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim **Implementieren des SpreadsheetItem-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Wenn Sie die [**Methoden ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) und [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) implementieren, lesen Sie die [**IAnnotationProvider-Dokumentation.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Beide Methoden geben Arrays zurück, damit Anbieter mehrere Anmerkungen für eine einzelne Zelle unterstützen können.
-   Einige Arten von Anmerkungen erfordern keine vollständige Implementierung der [**IAnnotationProvider-Schnittstelle.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Beispielsweise kann ein einfacher Rechtschreibfehlerindikator dargestellt werden, indem [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) einen Textattributbezeichner von [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)zurückgibt und [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) einen NULL-Wert zurückgibt.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Erforderliche Member für **ISpreadsheetItemProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ISpreadsheetItemProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) erforderlich.



| Erforderliche Member                                                                         | Memberart | Hinweise                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Eigenschaft    | Die Implementierung einer separaten [**Formula-Eigenschaft**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) ist erforderlich, da die [Value-Eigenschaft](value-property.md) einer Zelle in der Regel den berechneten Wert der Zelle zurückgibt. Die **Formula-Eigenschaft** sollte **NULL sein,** wenn keine Formel festgelegt ist. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Methode      | Gibt ein Array von Elementanbietern zurück, die auf die anmerkungen verweisen, die mit dieser Zelle verknüpft sind. Zeiger innerhalb des Arrays können NULL sein, wenn eine Anmerkung keinen verknüpften Anbieter hat.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Methode      | Gibt ein Array von Anmerkungstypbezeichnern zurück, die die Anmerkungen in dieser Zelle beschreiben. Das Array muss die gleiche Größe wie das von [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)zurückgegebene Array haben.                                         |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tabellenkalkulations-Steuerelementmuster](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 