---
title: Aufrufen des Steuerelementmusters
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IInvokeProvider, einschließlich Informationen zu Methoden.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Invoke-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Invoke-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IInvokeProvider
- IInvokeProvider
- Implementieren Benutzeroberflächenautomatisierung Invoke-Steuerelementmustern
- Aufrufen von Steuerelementmustern
- Steuerelementmuster,IInvokeProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Invoke
- Steuerelementmuster,Aufrufen
- interfaces,IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbd675a9c30daf0e7b097a706dae9ff0d7767f92f7b785b3098d72ddf6f7cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997940"
---
# <a name="invoke-control-pattern"></a>Aufrufen des Steuerelementmusters

Beschreibt Richtlinien und Konventionen für die Implementierung [**von IInvokeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)einschließlich Informationen zu Methoden. Das  Invoke-Steuerelementmuster wird verwendet, um Steuerelemente zu unterstützen, die bei der Aktivierung keinen Zustand behalten, sondern stattdessen eine einzelne, eindeutige Aktion initiieren oder ausführen.

Steuerelemente, die den Zustand verwalten, z. B. Kontrollkästchen und Optionsfelder, müssen stattdessen [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) bzw. [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des Invoke-Steuerelementmusters die folgenden Richtlinien und Konventionen: 

-   Steuerelemente implementieren [**IInvokeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) wenn das gleiche Verhalten nicht über einen anderen Steuerelementmusteranbieter verfügbar gemacht wird. Wenn beispielsweise die [**IUIAutomationInvokePattern::Invoke-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) für ein Steuerelement dieselbe Aktion wie die [**IUIAutomationExpandCollapsePattern::Expand-**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) oder [**Collapse-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) ausführt, sollte das Steuerelement **IInvokeProvider** nicht implementieren.
-   Ein Steuerelement wird normalerweise durch Klicken, Doppelklicken, Drücken der EINGABETASTE oder durch eine vordefinierte oder alternative Tastenkombination aufgerufen.
-   Das **Invoked-Ereignis** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) wird für ein Steuerelement ausgelöst, das aktiviert wurde (als Antwort auf ein Steuerelement, das seine zugeordnete Aktion führt). Sofern möglich, sollte das Ereignis ausgelöst werden, nachdem das Steuerelement die Aktion abgeschlossen hat und ohne Blockierung zurückgekehrt ist. Das **Invoked-Ereignis** (**UIA \_ \_ InvokedEventId**) sollte ausgelöst werden, bevor die **Invoke-Anforderung** in den folgenden Szenarien bedient wird:
    -   Es ist nicht möglich oder zweckmäßig, bis zum Abschluss der Aktion zu warten.
    -   Die Aktion erfordert eine Benutzeraktion.
    -   Die Aktion ist zeitaufwändig und führt dazu, dass der aufrufende Client für einen längeren Zeitraum blockiert wird.
-   Wenn das Aufrufen des Steuerelements erhebliche Nebeneffekte hat, sollten diese Nebeneffekte über die **HelpText-Eigenschaft verfügbar gemacht** werden. Obwohl beispielsweise [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) nicht der Auswahl zugeordnet ist, kann **Invoke** dazu führen, dass ein anderes Steuerelement ausgewählt wird.
-   Mauszeigereffekte (oder Mausovereffekte) stellen im Allgemeinen kein **Invoked-Ereignis** dar. Steuerelemente, die eine Aktion ausführen (anstatt einen visuellen Effekt zu verursachen), die auf dem Hoverzustand basieren, sollten jedoch das **Invoke-Steuerelementmuster** unterstützen.
    > [!Note]  
    > Diese Implementierung wird als Problem für Barrierefreiheit betrachtet, wenn das Steuerelement nur als Ergebnis eines mausbezogenen Nebeneffekts aufgerufen werden kann.

     

-   Das Aufrufen eines Steuerelements unterscheidet sich vom Auswählen eines Elements. Abhängig vom Steuerelement kann das Aufrufen jedoch möglicherweise den Nebeneffekt haben, dass das Element ausgewählt wird. Wenn Sie z. B. ein Microsoft Word Dokumentlistenelement im Ordner Eigene Dokumente aufrufen, wird das Element ausgewählt und das Dokument geöffnet.
-   Ein Element kann aus der Microsoft Benutzeroberflächenautomatisierung sofort nach dem Aufruf nicht mehr angezeigt werden. Dies kann zur Folge haben, dass das Anfordern von Informationen von dem Element, die durch den Ereignisrückruf bereitgestellt werden, fehlschlägt. Als Problemlösung wird empfohlen, zwischengespeicherte Informationen vorab abzurufen.
-   Steuerelemente können mehrere Steuerelementmuster implementieren. Beispielsweise implementiert das **Steuerelement Füllfarbe** auf Microsoft Excel Symbolleiste sowohl das Invoke- als auch das [ExpandCollapse-Steuerelementmuster.](uiauto-implementingexpandcollapse.md) Das ExpandCollapse-Steuerelementmuster macht das  Menü verfügbar, und das Invoke-Steuerelementmuster füllt die aktive Auswahl mit der ausgewählten Farbe aus.

## <a name="required-members-for-iinvokeprovider"></a>Erforderliche Member für **IInvokeProvider**

Die folgende Methode ist für die Implementierung der [**IInvokeProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) erforderlich.



| Erforderliche Member                                | Memberart | Hinweise                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Methode      | **Invoke** ist ein asynchroner Aufruf und muss sofort ohne Blockierung zurückgeben.<br/> Dieses Verhalten ist insbesondere für Steuerelemente wichtig, die direkt oder indirekt ein modales Dialogfeld starten, wenn sie aufgerufen werden. Jeder Benutzeroberflächenautomatisierungs-Client, der das Ereignis ausgelöst hat, bleibt blockiert, bis das modale Dialogfeld geschlossen wird. <br/> |



 

Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





