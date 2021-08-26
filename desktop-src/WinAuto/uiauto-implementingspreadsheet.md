---
title: Tabellenkalkulations-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ISpreadsheetProvider, einschließlich Informationen zu Methoden.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Tabellenkalkulations-Steuerelementmusters
- Benutzeroberflächenautomatisierung, Tabellenkalkulations-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ISpreadsheetProvider
- ISpreadsheetProvider
- Implementieren Benutzeroberflächenautomatisierung Tabellenkalkulations-Steuerelementmusters
- Tabellenkalkulations-Steuerelementmuster
- Steuerelementmuster,ISpreadsheetProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Arbeitsblatts
- Steuerelementmuster, Tabellenkalkulation
- interfaces,ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7991937f1530e28ed85227fbe19be13b628f9722d5609367e2f483c86a2bb70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098280"
---
# <a name="spreadsheet-control-pattern"></a>Tabellenkalkulations-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**ISpreadsheetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)einschließlich Informationen zu Methoden. Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet. Das  Tabellenkalkulations-Steuerelementmuster wird verwendet, um den Inhalt eines Arbeitsblatts oder eines anderen rasterbasierten Dokuments verfügbar zu machen.

Das  Tabellenkalkulations-Steuerelementmuster ist eng mit dem [Grid-Steuerelementmuster](uiauto-implementinggrid.md) verknüpft. -Steuerelemente,  die das Tabellenkalkulations-Steuerelementmuster implementieren, sollten auch das Grid-Steuerelementmuster implementieren. Steuerelemente können ggf. auch das [Tabellensteuerelementmuster](uiauto-implementingtable.md) implementieren. Beispiele für Steuerelemente, die diese Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie  beim Implementieren des Tabellenkalkulations-Steuerelementmusters die folgenden Richtlinien und Konventionen:

-   Wenn ein Arbeitsblatt die [**ISpreadsheetProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) implementiert, müssen die Zellen die [**ISpreadsheetItemProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) implementieren.
-   Die [**ISpreadsheetProvider::GetItemByName-Methode**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) soll die gleiche Art von Navigation bereitstellen, die eine Anwendung möglicherweise mit einem **Jump-to-Label-Feature** bereitstellt. In vielen Tabellenkalkulationsprogrammen können bestimmte Zellen einen Anzeigenamen oder eine Bezeichnung erhalten. **GetItemByName** ermöglicht dem Client, basierend auf seinem Anzeigenamen eine Zelle zu suchen. Diese Methode sollte keine Zellen abrufen, die den Namenstext enthalten, da die Ergebnisse sehr mehrdeutig sein können. Wenn das Arbeitsblattprogramm mehreren Zellen in einem Arbeitsblatt den gleichen Anzeigenamen oder die gleiche Bezeichnung zulässt, ist das Verhalten von Microsoft Benutzeroberflächenautomatisierung nicht definiert.

## <a name="required-members-for-ispreadsheetprovider"></a>Erforderliche Member für **ISpreadsheetProvider**

Die folgende Methode ist für die Implementierung der [**ISpreadsheetProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) erforderlich.



| Erforderliche Member                                                       | Memberart | Hinweise |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 