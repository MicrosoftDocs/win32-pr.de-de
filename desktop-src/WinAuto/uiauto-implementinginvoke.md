---
title: Steuerelement Muster aufrufen
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IInvokeProvider, einschließlich Informationen zu-Methoden.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Aufruf Steuerungs Musters
- UI-Automatisierung, Steuerelement Muster aufrufen
- UI-Automatisierung, IInvokeProvider
- IInvokeProvider
- Implementieren von Steuerelement Mustern für die Benutzeroberflächen Automatisierung
- Aufrufen von Steuerelement Mustern
- Steuerelement Muster, IInvokeProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächenautomatisierungs-aufrufen
- Steuerelement Muster, aufrufen
- Schnittstellen, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855923"
---
# <a name="invoke-control-pattern"></a>Steuerelement Muster aufrufen

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), einschließlich Informationen zu-Methoden. Das **Aufruf** Steuerelement-Muster wird zur Unterstützung von Steuerelementen verwendet, die den Zustand nicht beibehalten, wenn Sie aktiviert werden, sondern eine einzelne, eindeutige Aktion initiieren oder ausführen.

Steuerelemente, die den Zustand beibehalten (z. b. Kontrollkästchen und Options Felder), müssen stattdessen [**itggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) bzw. [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Aufruf** Steuerungs Musters die folgenden Richtlinien und Konventionen:

-   Steuerelemente implementieren [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) , wenn das gleiche Verhalten nicht durch einen anderen Steuerelement Muster-Anbieter verfügbar gemacht wird. Wenn z. b. die [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) -Methode in einem-Steuerelement dieselbe Aktion wie die [**iuiautomationexpandredusepattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) -oder [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) -Methode ausführt, sollte das Steuerelement **IInvokeProvider** nicht implementieren.
-   Ein Steuerelement wird normalerweise durch Klicken, Doppelklicken, Drücken der EINGABETASTE oder durch eine vordefinierte oder alternative Tastenkombination aufgerufen.
-   Das Ereignis **Aufruf** Ereignis ([**UIA \_ aufrufen \_ invokedeventid**](uiauto-event-ids.md)) wird für ein Steuerelement ausgelöst, das aktiviert wurde (als Antwort auf ein Steuerelement, das die zugehörige Aktion ausführt). Sofern möglich, sollte das Ereignis ausgelöst werden, nachdem das Steuerelement die Aktion abgeschlossen hat und ohne Blockierung zurückgekehrt ist. Das **aufgerufene** Ereignis (**UIA \_ -Aufruf \_ invoketoventid**) sollte vor der Wartung der **Aufruf** Anforderung in den folgenden Szenarien ausgelöst werden:
    -   Es ist nicht möglich oder zweckmäßig, bis zum Abschluss der Aktion zu warten.
    -   Die Aktion erfordert eine Benutzeraktion.
    -   Die Aktion ist zeitaufwändig und führt dazu, dass der aufrufende Client für einen längeren Zeitraum blockiert wird.
-   Wenn das Aufrufen des Steuer Elements bedeutende Nebeneffekte hat, sollten diese Nebeneffekte über die **HelpText** -Eigenschaft verfügbar gemacht werden. Wenn z. b. [**iuiautomationinvokepattern:: Aufrufen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) nicht mit der Auswahl verknüpft ist, kann der **Aufruf** bewirken, dass ein anderes Steuerelement ausgewählt wird.
-   Hover-(oder Mouseover) Effekte stellen im Allgemeinen kein **aufgerufenes** Ereignis dar. Allerdings sollten Steuerelemente, die eine Aktion ausführen (im Gegensatz zur Ursache eines visuellen Effekts), das Steuerelement Muster **aufrufen** unterstützen.
    > [!Note]  
    > Diese Implementierung wird als Problem für Barrierefreiheit betrachtet, wenn das Steuerelement nur als Ergebnis eines mausbezogenen Nebeneffekts aufgerufen werden kann.

     

-   Das Aufrufen eines Steuerelements unterscheidet sich vom Auswählen eines Elements. Abhängig vom Steuerelement kann das Aufrufen jedoch möglicherweise den Nebeneffekt haben, dass das Element ausgewählt wird. Wenn Sie z. b. ein Microsoft Word-Dokument Listenelement im Ordner "eigene Dokumente" aufrufen, wird das Element ausgewählt und das Dokument geöffnet.
-   Ein Element kann beim Aufrufen nicht sofort aus der Microsoft UI Automation-Struktur verschwinden. Dies kann zur Folge haben, dass das Anfordern von Informationen von dem Element, die durch den Ereignisrückruf bereitgestellt werden, fehlschlägt. Als Problemlösung wird empfohlen, zwischengespeicherte Informationen vorab abzurufen.
-   Steuerelemente können mehrere Steuerelementmuster implementieren. Beispielsweise implementiert das **Füllfarbe** -Steuerelement auf der Microsoft Excel-Symbolleiste sowohl das Aufruf-als auch das [ExpandCollapse](uiauto-implementingexpandcollapse.md) -Steuerelement Muster. Das ExpandCollapse-Steuerelement Muster macht das Menü verfügbar, und das Muster zum **aufrufen** des Steuer Elements füllt die aktive Auswahl mit der ausgewählten Farbe aus.

## <a name="required-members-for-iinvokeprovider"></a>Erforderliche Member für **IInvokeProvider**

Die folgende Methode ist für die Implementierung der [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                | Memberart | Hinweise                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Methode      | " **Aufrufen** " ist ein asynchroner Aufruf und muss sofort ohne Blockierung zurückgegeben werden.<br/> Dieses Verhalten ist insbesondere für Steuerelemente wichtig, die direkt oder indirekt ein modales Dialogfeld starten, wenn sie aufgerufen werden. Jeder Benutzeroberflächenautomatisierungs-Client, der das Ereignis ausgelöst hat, bleibt blockiert, bis das modale Dialogfeld geschlossen wird. <br/> |



 

Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ aufrufen \_ invokedebug-ID**](uiauto-event-ids.md)
</dt> </dl>

 

 





