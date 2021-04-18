---
title: Transform-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ITransformProvider und ITransformProvider2, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Transformations Steuerelement Musters
- Benutzeroberflächenautomatisierungs, Transformations Steuerelement-Muster
- UI-Automatisierung, ITransformProvider
- ITransformProvider
- Implementieren von Transformations Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Transformations Steuerelement-Muster
- Steuerelement Muster, ITransformProvider
- Steuerelement Muster, Implementieren der Transformation für die Benutzeroberflächen Automatisierung
- Steuerelement Muster, Transformieren
- Schnittstellen, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516958"
---
# <a name="transform-control-pattern"></a>Transform-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) und [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), einschließlich Informationen zu Eigenschaften und Methoden. Das Transform-Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die in einem zweidimensionalen Raum verschoben, verkleinert, geändert oder gedreht werden können.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ITransformProvider**](#required-members-for-itransformprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Transform** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Die Unterstützung für dieses Steuerelementmuster ist nicht auf Objekte auf dem Desktop beschränkt. Dieses Steuerelementmuster muss auch von den untergeordneten Elementen eines Containerobjekts unterstützt werden, wenn die untergeordneten Elemente verschoben, vergrößert, verkleinert oder innerhalb der Grenzen des Containers frei gedreht werden können.
-   Ein Objekt kann nicht so verschoben, vergrößert, verkleinert oder gedreht werden, dass seine resultierende Bildschirmposition vollständig außerhalb der Koordinaten des Containers liegt und daher nicht über die Tastatur oder Maus zugänglich ist (wenn z. B. ein Fenster auf oberster Ebene außerhalb des Bildschirms oder ein untergeordnetes Objekt außerhalb der Viewportgrenzen des Containers verschoben wird). In diesen Fällen wird das Objekt so nahe wie möglich bei den angeforderten Bildschirmkoordinaten platziert, wobei die oberen oder linken Koordinaten außer Kraft gesetzt werden, damit sich die Koordinaten innerhalb der Containergrenzen befinden.
-   Für Systeme mit mehreren Monitoren wird ein Objekt so nahe wie möglich bei den angeforderten Koordinaten auf dem primären Monitor platziert, wenn das Objekt vollständig außerhalb der Bildschirmkoordinaten des kombinierten Desktops verschoben, vergrößert, verkleinert oder gedreht wird.
-   Alle Parameter und Eigenschaftswerte sind absolute Angaben und unabhängig vom Gebietsschema.

## <a name="required-members-for-itransformprovider"></a>Erforderliche Member für **ITransformProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                         | Memberart | Hinweise |
|----------------------------------------------------------|-------------|-------|
| [**CanMove**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Eigenschaft    | Keine  |
| [**CanResize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Eigenschaft    | Keine  |
| [**Canrotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Eigenschaft    | Keine  |
| [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Methode      | Keine  |
| [**Größe ändern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Methode      | Keine  |
| [**Drehen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Methode      | Keine  |



 

Die folgenden zusätzlichen Eigenschaften und Methoden sind für die Implementierung der [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                              | Memberart | Hinweise |
|---------------------------------------------------------------|-------------|-------|
| [**Kanzoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Eigenschaft    | Keine  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Methode      | Keine  |
| [**Zoombyunit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Methode      | Keine  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Eigenschaft    | Keine  |
| [**Zoommaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Eigenschaft    | Keine  |
| [**Zoomminimal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Eigenschaft    | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 