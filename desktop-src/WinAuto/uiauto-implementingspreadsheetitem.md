---
title: Spreadsheetitem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ispreadsheetitemprovider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Benutzeroberflächenautomatisierung, Implementieren des spreadsheetitem-Steuerelement Musters
- UI-Automatisierung, spreadsheetitem-Steuerelement Muster
- UI-Automatisierung, ispreadsheetitemprovider
- ISpreadsheetItemProvider
- Implementieren des spreadsheetitem-Steuerelement Musters der Benutzeroberflächen Automatisierung
- Spreadsheetitem-Steuerelement Muster
- Steuerelement Muster, ispreadsheetitemprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabellen kalerischen Elemente
- Steuerelement Muster, spreadsheetitem
- Schnittstellen, ispreadsheetitemprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039478"
---
# <a name="spreadsheetitem-control-pattern"></a>Spreadsheetitem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ispreadsheetitemprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **spreadsheetitem** -Steuerelement Muster wird verwendet, um die Eigenschaften einer Zelle in einer Kalkulations Tabelle oder einem anderen Raster basierten Dokument verfügbar zu machen.

Das **spreadsheetitem** -Steuerelement Muster ist eng mit dem [GridItem](uiauto-implementinggriditem.md) -Steuerelement Muster verknüpft. Steuerelemente, die das **spreadsheetitem** -Steuerelement Muster implementieren, sollten auch das GridItem-Steuerelement Muster implementieren. Steuerelemente können ggf. auch das [TableItem](uiauto-implementingtableitem.md) -Steuerelement Muster implementieren. Beispiele für Steuerelemente, die diese Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ispreadsheetitemprovider**](#required-members-for-ispreadsheetitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **spreadsheetitem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Informationen zum Implementieren der [**ispreadsheetitemprovider:: getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) -Methode und der [**ispreadsheetitemprovider:: getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) -Methode finden Sie in der [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Dokumentation. Diese Methoden geben Arrays zurück, damit Anbieter mehrere Anmerkungen in einer einzelnen Zelle unterstützen können.
-   Einige Arten von Anmerkungen erfordern keine vollständige Implementierung der [**iannotationprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) -Schnittstelle. Ein einfacher Rechtschreibfehler Indikator könnte z. b. dargestellt werden, wenn [**getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) einen Text Attribut Bezeichner von [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)zurückgibt und [**getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) einen NULL-Wert zurückgibt.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Erforderliche Member für **ispreadsheetitemprovider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ispreadsheetitemprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                         | Memberart | Hinweise                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Eigenschaft    | Das Implementieren einer separaten [**Formel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) Eigenschaft ist erforderlich, da die [value](value-property.md) -Eigenschaft einer Zelle in der Regel den berechneten Wert der Zelle zurückgibt. Die **Formel** Eigenschaft sollte **null** sein, wenn keine Formel festgelegt ist. |
| [**Getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Methode      | Gibt ein Array von Element Anbietern zurück, die auf die Anmerkungen verweisen, die mit dieser Zelle verknüpft sind. Zeiger innerhalb des Arrays können NULL sein, wenn eine Anmerkung keinen verknüpften Anbieter hat.                                                                                                       |
| [**Getannotationtypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Methode      | Gibt ein Array von Anmerkung-typbezeichaten zurück, die die Anmerkungen in dieser Zelle beschreiben. Das Array muss dieselbe Größe aufweisen wie das Array, das von [**getannotationobjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)zurückgegeben wird.                                         |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tabellen Steuerungs Muster](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 