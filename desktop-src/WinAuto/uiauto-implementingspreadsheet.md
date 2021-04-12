---
title: Tabellen Steuerungs Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ispreadsheetprovider, einschließlich Informationen zu-Methoden.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Tabellen Steuerungs Musters
- Benutzeroberflächenautomatisierungs-, Tabellen Steuerungs Muster
- UI-Automatisierung, ispreadsheetprovider
- ISpreadsheetProvider
- Implementieren des Steuerelement Musters der Benutzeroberflächen Automatisierung
- Tabellen Steuerungs Muster
- Steuerelement Muster, ispreadsheetprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabelle
- Steuerelement Muster, Tabelle
- Schnittstellen, ispreadsheetprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315776"
---
# <a name="spreadsheet-control-pattern"></a>Tabellen Steuerungs Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), einschließlich Informationen zu-Methoden. Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet. Das **Tabellen** Steuerungs Muster wird verwendet, um den Inhalt einer Kalkulations Tabelle oder eines anderen Raster basierten Dokuments verfügbar zu machen.

Das **Tabellen** Steuerelement-Muster ist eng mit dem [Raster](uiauto-implementinggrid.md) Steuerelement Muster verknüpft. Steuerelemente, die das **Tabellen** Steuerelement-Muster implementieren, sollten auch das Raster-Steuerelement Muster implementieren. Steuerelemente können ggf. auch das [Table](uiauto-implementingtable.md) -Steuerelement Muster implementieren. Beispiele für Steuerelemente, die diese Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Tabellen** Steuerelement-Musters die folgenden Richtlinien und Konventionen:

-   Wenn eine Kalkulations Tabelle die Schnittstelle [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) implementiert, muss die Zelle die [**ispreadsheetitemprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) -Schnittstelle implementieren.
-   Die [**ispreadsheetprovider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) -Methode soll die gleiche Art von Navigation bereitstellen, die eine Anwendung möglicherweise mit einer Funktion **zum Springen zur Bezeichnung** bereitstellt. Bei vielen Tabellen Kalkulations Programmen können bestimmte Zellen einen anzeigen Amen oder eine Bezeichnung erhalten. **GetItemByName** ermöglicht es dem Client, eine Zelle auf der Grundlage des anzeigen Amens zu suchen. Diese Methode sollte keine Zellen abrufen, die den Namenstext enthalten, da die Ergebnisse sehr mehrdeutig sein können. Wenn das Tabellen Kalkulations Programm zulässt, dass mehrere Zellen in derselben Tabelle denselben anzeigen Amen oder eine gleiche Bezeichnung aufweisen, ist das Verhalten der Microsoft-Benutzeroberflächen Automatisierung nicht definiert.

## <a name="required-members-for-ispreadsheetprovider"></a>Erforderliche Member für **ispreadsheetprovider**

Die folgende Methode ist für die Implementierung der [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                       | Memberart | Hinweise |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 