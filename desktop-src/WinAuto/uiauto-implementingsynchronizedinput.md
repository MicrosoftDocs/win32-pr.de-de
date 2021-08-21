---
title: SynchronizedInput-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ISynchronizedInputProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des SynchronizedInput-Steuerelementmusters
- Benutzeroberflächenautomatisierung,SynchronizedInput-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ISynchronizedInputProvider
- ISynchronizedInputProvider
- Implementieren Benutzeroberflächenautomatisierung SynchronizedInput-Steuerelementmuster
- SynchronizedInput-Steuerelementmuster
- Steuerelementmuster,ISynchronizedInputProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung SynchronizedInput
- Steuerelementmuster,SynchronizedInput
- interfaces,ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91aa4ad93a30be26ebcbc463ade3a27d896d61727508965a86d1ed229b7d79be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114851"
---
# <a name="synchronizedinput-control-pattern"></a>SynchronizedInput-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**ISynchronizedInputProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **SynchronizedInput-Steuerelementmuster** ermöglicht Es Microsoft Benutzeroberflächenautomatisierung Clientanwendungen, die Maus- oder Tastatureingabe an ein bestimmtes Benutzeroberflächenelement weiterzuleiten.

Dieses Steuerelementmuster wird in der Regel in automatisierten Testskripts verwendet, um Maus- oder Tastatureingaben an ein bestimmtes Benutzeroberflächenelement zu senden und dann zu überprüfen, ob das Element die Eingabe empfangen hat.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ISynchronizedInputProvider**](#required-members-for-isynchronizedinputprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **SynchronizedInput-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Wenn die [**ISynchronizedInputProvider::StartListening-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) aufgerufen wird, sollte der Benutzeroberflächenautomatisierung Anbieter mit der Überprüfung auf Eingaben des angegebenen Typs beginnen und dann eine der folgenden Aktionen ausführen:
    -   Wenn eine übereinstimmende Eingabe für das Element gefunden wird, sollte der Anbieter das [**UIA \_ InputReachedTargetEventId-Ereignis**](uiauto-event-ids.md) auslösen.
    -   Wenn eine übereinstimmende Eingabe gefunden wird, aber ein anderes Element erreicht wurde, sollte der Anbieter das [**UIA \_ InputReachedOtherElementEventId-Ereignis**](uiauto-event-ids.md) auslösen.
    -   Wenn eine nicht übereinstimmende Eingabe gefunden wird, sollte der Anbieter die Eingabe verwerfen und das [**UIA \_ InputDiscardedEventId-Ereignis**](uiauto-event-ids.md) auslösen.
-   Der Benutzeroberflächenautomatisierung-Anbieter muss die Eingabe verwerfen, wenn es sich um ein anderes Element als das aktuelle Element handelt.
-   Wenn das Element die Eingabe empfängt oder die [**ISynchronizedInputProvider::Cancel-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) aufgerufen wird, beendet der Anbieter die Überprüfung der Eingabe und fährt wie gewohnt fort.
-   Wenn [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) aufgerufen wird, wenn der Anbieter bereits auf Eingaben lauscht, sollte der Anbieter [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md)zurückgeben.

## <a name="required-members-for-isynchronizedinputprovider"></a>Erforderliche Member für **ISynchronizedInputProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISynchronizedInputProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) erforderlich.



| Erforderliche Member                                                                         | Memberart | Hinweise |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Methode      | Keine  |
| [**Abbrechen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Methode      | Keine  |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) | Ereignis       | Keine  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




