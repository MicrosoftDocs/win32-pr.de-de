---
title: Tabellensteuermuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ITableProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Tabellensteuermuster wird verwendet, um Steuerelemente zu unterstützen, die als Container für eine Auflistung untergeordneter Elemente fungieren.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Tabellensteuermusters
- Benutzeroberflächenautomatisierung,Tabellensteuermuster
- Benutzeroberflächenautomatisierung,ITableProvider
- ITableProvider
- Implementieren Benutzeroberflächenautomatisierung Tabellensteuermustern
- Tabellensteuermuster
- Steuerelementmuster, ITableProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Tabelle
- Steuerelementmuster, Tabelle
- interfaces,ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb484245ee7c2f982ca6c5624ad108a0c75a4721ba7f6cbdf7a8af8ee2d91881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324133"
---
# <a name="table-control-pattern"></a>Tabellensteuermuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von ITableProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Tabellensteuermuster** wird verwendet, um Steuerelemente zu unterstützen, die als Container für eine Auflistung untergeordneter Elemente fungieren.

Die unteren Elemente des Containerelements müssen [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementieren und in einem zweidimensionalen logischen Koordinatensystem organisiert sein, das nach Zeile und Spalte durchlaufen werden kann. Dieses Steuerelementmuster entspricht [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) mit dem Unterschied, dass jedes Steuerelement, das [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) implementiert, auch eine Spalten- und/oder Zeilenheaderbeziehung für jedes untergeordnete Element verfügbar machen muss. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITableProvider**](#required-members-for-itableprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim **Implementieren des Tabellensteuermusters** die folgenden Richtlinien und Konventionen:

-   Der Zugriff auf den Inhalt einzelner Zellen erfolgt über ein zweidimensionales logisches Koordinatensystem oder Array, das durch die erforderliche, gleichzeitige Implementierung von [**IGridProvider bereitgestellt wird.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)
-   Eine Spalten- oder Zeilenüberschrift kann in einem Tabellenobjekt enthalten sein oder ein separates Headerobjekt darstellen, das einem Tabellenobjekt zugeordnet ist.
-   Spalten- und Zeilenüberschriften können sowohl eine primäre als auch beliebige unterstützende Überschriften enthalten.
    > [!Note]  
    > Dieses Konzept wird in einem Tabellenblatt Microsoft Excel, in dem ein Benutzer eine **Vornamenspalte definiert** hat. Diese Spalte verfügt jetzt über  zwei Header, einschließlich des vom Benutzer definierten Vornamenheaders und der alphanumerischen Bezeichnung für diese Spalte, die von der Anwendung zugewiesen wird.

     

-   Informationen [zu verwandten Rasterfunktionen finden](uiauto-implementinggrid.md) Sie unter Rastersteuermuster.

    Die folgende Abbildung zeigt eine Tabelle mit komplexen Spaltenüberschriften.

    ![Tabelle mit komplexen Spaltenüberschriften](images/uia-valuepattern-colorpicker.jpg)

    Die folgende Abbildung zeigt eine Tabelle mit einer mehrdeutigen [**ITableProvider::RowOrColumnMajor-Eigenschaft.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor)

    ![Tabelle mit einer mehrdeutigen roworcolumnmajor-Eigenschaft](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Erforderliche Member für **ITableProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITableProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) erforderlich.



| Erforderliche Member                                                   | Memberart | Hinweise |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Eigenschaft    | Keine  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Methode      | Keine  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[TableItem-Steuerelementmuster](uiauto-implementingtableitem.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




