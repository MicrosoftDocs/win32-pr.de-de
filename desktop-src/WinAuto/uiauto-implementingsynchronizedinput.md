---
title: SynchronizedInput-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von isynchronizedinputprovider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- UI-Automatisierung, Implementieren des SynchronizedInput-Steuerelement Musters
- Benutzeroberflächenautomatisierungs-, SynchronizedInput-Steuerelement Muster
- UI-Automatisierung, isynchronizedinputprovider
- ISynchronizedInputProvider
- Implementieren von SynchronizedInput-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- SynchronizedInput-Steuerelement Muster
- Steuerelement Muster, isynchronizedinputprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-SynchronizedInput
- Steuerelement Muster, SynchronizedInput
- Schnittstellen, isynchronizedinputprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337177"
---
# <a name="synchronizedinput-control-pattern"></a>SynchronizedInput-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**isynchronizedinputprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), einschließlich Informationen zu Eigenschaften und Methoden. Mit dem **SynchronizedInput** -Steuerelement Muster können Microsoft UI Automation-Client Anwendungen die Maus-oder Tastatureingaben an ein bestimmtes UI-Element weiterleiten.

Dieses Steuerelement Muster wird in der Regel in automatisierten Test Skripts verwendet, um Maus-oder Tastatureingaben an ein bestimmtes Benutzeroberflächen Element zu senden und dann zu überprüfen, ob das Element die Eingabe empfangen hat.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **isynchronizedinputprovider**](#required-members-for-isynchronizedinputprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **SynchronizedInput** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Wenn die [**isynchronizedinputprovider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) -Methode aufgerufen wird, sollte der Benutzeroberflächenautomatisierungs-Anbieter mit der Überprüfung der Eingabe des angegebenen Typs beginnen und dann eine der folgenden Aktionen ausführen:
    -   Wenn übereinstimmende Eingaben für das Element gefunden werden, sollte der Anbieter das [**UIA-Ereignis " \_ inputreachedtargeteventid**](uiauto-event-ids.md) " erhöhen.
    -   Wenn übereinstimmende Eingaben gefunden werden, aber ein anderes Element erreicht wurden, sollte der Anbieter das UIA-Ereignis " [**\_ inputreachedotherelementeventid**](uiauto-event-ids.md) " erhöhen.
    -   Wenn nicht übereinstimmende Eingaben gefunden werden, sollte der Anbieter die Eingabe verwerfen und das UIA-Ereignis " [**\_ inputverwerdebug-**](uiauto-event-ids.md) ID" erhöhen.
-   Der Benutzeroberflächenautomatisierungs-Anbieter muss die Eingabe verwerfen, wenn Sie für ein anderes Element als das aktuelle Element gilt.
-   Wenn das Element die Eingabe empfängt oder wenn die [**isynchronizedinputprovider:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) -Methode aufgerufen wird, beendet der Anbieter die Überprüfung der Eingabe und fährt wie gewohnt fort.
-   Wenn [**isynchronizedinputprovider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) aufgerufen wird, wenn der Anbieter bereits Eingaben abhört, sollte der Anbieter [**UIA \_ E \_ InvalidOperation**](uiauto-error-codes.md)zurückgeben.

## <a name="required-members-for-isynchronizedinputprovider"></a>Erforderliche Member für **isynchronizedinputprovider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**isynchronizedinputprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                         | Memberart | Hinweise |
|------------------------------------------------------------------------------------------|-------------|-------|
| [**Startüberwachung**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | Methode      | Keine  |
| [**Abbrechen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | Methode      | Keine  |
| [**UIA \_ inputreachedtargeteventid**](uiauto-event-ids.md) | Ereignis       | Keine  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




