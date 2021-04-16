---
title: Table-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITableProvider, einschließlich Informationen zu Eigenschaften und Methoden. Das Table-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Tabellen Steuerungs Musters
- UI-Automatisierung, Table-Steuerelement Muster
- UI-Automatisierung, ITableProvider
- ITableProvider
- Implementieren von Tabellen Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Tabellen Steuerelement-Muster
- Steuerelement Muster, ITableProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabelle
- Steuerelement Muster, Tabelle
- Schnittstellen, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562573"
---
# <a name="table-control-pattern"></a>Table-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **Table** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von untergeordneten Elementen fungieren.

Die untergeordneten Elemente des Container-Elements müssen [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) implementieren und in einem zweidimensionalen logischen Koordinatensystem angeordnet sein, das nach Zeilen und Spalten durchlaufen werden kann. Dieses Steuerelement Muster entspricht [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , wobei jedes Steuerelement, das [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) implementiert, auch für jedes untergeordnete Element eine Spalten-und/oder Zeilen Header Beziehung verfügbar machen muss. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITableProvider**](#required-members-for-itableprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Table** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Der Zugriff auf den Inhalt einzelner Zellen erfolgt über ein zweidimensionales logisches Koordinatensystem oder ein Array, das von der erforderlichen, gleichzeitigen Implementierung von [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)bereitgestellt wird.
-   Eine Spalten- oder Zeilenüberschrift kann in einem Tabellenobjekt enthalten sein oder ein separates Headerobjekt darstellen, das einem Tabellenobjekt zugeordnet ist.
-   Spalten- und Zeilenüberschriften können sowohl eine primäre als auch beliebige unterstützende Überschriften enthalten.
    > [!Note]  
    > Dieses Konzept wird in einem Microsoft Excel-Arbeitsblatt ersichtlich, in dem ein Benutzer eine **Vorname** -Spalte definiert hat. Diese Spalte verfügt jetzt über zwei Header, einschließlich des vom benutzerdefinierten **Vornamen** Headers und der alphanumerischen Bezeichnung für diese Spalte, die von der Anwendung zugewiesen wird.

     

-   Weitere Informationen finden Sie unter [Raster Steuerelement Muster](uiauto-implementinggrid.md) für Verwandte Raster Funktionen.

    Die folgende Abbildung zeigt eine Tabelle mit komplexen Spalten Headern.

    ![Tabelle mit komplexen Spaltenüberschriften](images/uia-valuepattern-colorpicker.jpg)

    Die folgende Abbildung zeigt eine Tabelle mit einer mehrdeutigen [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) -Eigenschaft.

    ![Tabelle mit mehrdeutiger RowOrColumnMajor-Eigenschaft](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Erforderliche Member für **ITableProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                   | Memberart | Hinweise |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Eigenschaft    | Keine  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Methode      | Keine  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[TableItem-Steuerelement Muster](uiauto-implementingtableitem.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




