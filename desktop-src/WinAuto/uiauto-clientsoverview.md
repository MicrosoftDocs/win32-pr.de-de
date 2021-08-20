---
title: Übersicht über Benutzeroberflächenautomatisierung Clients
description: In diesem Thema werden die wichtigsten Aufgaben beschrieben, die bei der Implementierung einer Microsoft Benutzeroberflächenautomatisierung-Clientanwendung zu erledigen sind.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- Benutzeroberflächenautomatisierung, Clients – Übersicht
- Clients, Informationen
- Clients, Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37ff185e72c25f5c3b8eeba8cdd4ae9250391a867538ad3e4b6de4f8d1dce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928682"
---
# <a name="ui-automation-clients-overview"></a>Übersicht über Benutzeroberflächenautomatisierung Clients

In diesem Thema werden die wichtigsten Aufgaben beschrieben, die bei der Implementierung einer Microsoft Benutzeroberflächenautomatisierung-Clientanwendung zu erledigen sind.

Ein Benutzeroberflächenautomatisierung Client ist jede Anwendung, die die Benutzeroberflächenautomatisierung-API verwendet, um auf Informationen zu Benutzeroberflächenelementen zuzugreifen oder Anwendungen durch programmgesteuerte Bearbeitung ihrer Benutzeroberflächenelemente zu steuern. Benutzeroberflächenautomatisierung Clients enthalten Hilfstechnologieanwendungen wie Sprachausgaben, die Informationen zu Benutzeroberflächenelementen abrufen und die Informationen so darstellen, dass sie für Personen mit Behinderungen geeignet sind. Sie umfassen auch Anwendungen wie Spracherkennungsprogramme und Softwaretesttools, die Benutzeroberflächenautomatisierung anstelle der Maus und Tastatur verwenden, um andere Anwendungen zu "steuern".

Aus Benutzeroberflächenautomatisierung Sicht müssen die wichtigsten Aufgaben, die eine Benutzeroberflächenautomatisierung Clientanwendung ausführen muss, Folgendes umfassen:

1.  **Rufen Sie eine Instanz des CUIAutomation-Objekts ab.**

    Informationen über Benutzeroberflächenelemente und den Zugriff auf benutzeroberflächenelementfunktionen werden clients von Benutzeroberflächenautomatisierung-Anbietern zur Verfügung gestellt. Clientanwendungen funktionieren jedoch nicht direkt mit Anbietern. Stattdessen liegt ein Kerndienst zwischen dem Client und dem Anbieter. Wenn ein Client die Benutzeroberflächenautomatisierung-API aufruft, ruft er tatsächlich den Benutzeroberflächenautomatisierung Kerndienst auf, der wiederum Aufrufe an die vom Anbieter implementierten Schnittstellen vornimmt.

    Um Zugriff auf den Kerndienst Benutzeroberflächenautomatisierung zu erhalten, muss ein Client eine Instanz des [**CUIAutomation-Objekts**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) erstellen und einen [**IUIAutomation-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) für das Objekt abrufen. Der **IUIAutomation-Zeiger** ist der Schlüssel des Clients für den Zugriff auf alle Benutzeroberflächenautomatisierung Funktionen, die dem Client zur Verfügung stehen. Weitere Informationen finden Sie unter [Erstellen des CUIAutomation-Objekts.](uiauto-creatingcuiautomation.md)

2.  **Rufen Sie IUIAutomationElement-Schnittstellen für Benutzeroberflächenelemente aus der Benutzeroberflächenautomatisierung Struktur ab.**

    Benutzeroberflächenautomatisierung macht einzelne Benutzeroberflächenelemente als Objekte verfügbar, die die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) implementieren. Informationen zu einem Element stehen Clients über Eigenschaften zur Verfügung, die von der **IUIAutomationElement-Schnittstelle** des Elements verfügbar gemacht werden, sowie Zugriff auf die Steuerelementmuster des Elements. Eigenschaften und Methoden, die von den Steuerelementmusterschnittstellen verfügbar gemacht werden, bieten Zugriff auf steuerelementspezifische Informationen und Funktionen.

    Die Benutzeroberflächenautomatisierung Elementobjekte werden Clients in einer hierarchischen Struktur bereitgestellt, die als Benutzeroberflächenautomatisierung Struktur bezeichnet wird. Clients verwenden Methoden, die von der [**IUIAutomation-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) verfügbar gemacht werden, um [**IUIAutomationElement-Schnittstellen**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für Benutzeroberflächenelemente in der Struktur abzurufen, und um andere Schnittstellen abzurufen, die verwendet werden, um die Struktur nach Elementen zu durchsuchen, die einem bestimmten Kriteriensatz entsprechen. Weitere Informationen finden Sie unter [Abrufen von Benutzeroberflächenautomatisierung Elementen.](uiauto-obtainingelements.md)

    Beim Abrufen von Benutzeroberflächenelementen können Clients die Systemleistung mithilfe der Cachefunktionen von Benutzeroberflächenautomatisierung verbessern. Das Zwischenspeichern ermöglicht es einem Client, einen Satz von Eigenschaften und Steuerelementmustern anzugeben, die zusammen mit dem -Element abgerufen werden sollen. In einem einzelnen prozessübergreifenden Aufruf ruft Benutzeroberflächenautomatisierung das Element und die angegebenen Eigenschaften und Steuerelementmuster ab und speichert sie dann im Cache. Ohne Zwischenspeicherung ist ein separater prozessübergreifender Aufruf erforderlich, um jede Eigenschaft oder jedes Steuerelementmuster abzurufen. Weitere Informationen finden Sie unter [Zwischenspeichern Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmuster.](uiauto-cachingforclients.md)

3.  **Rufen Sie Eigenschaften von UI-Elementen ab, und rufen Sie die Funktionalität des UI-Elements auf.**

    Clients verwenden die [**IUIAutomationElement-Schnittstelle,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) um die Eigenschaften und Steuerelementmuster eines Elements abzurufen. Die Schnittstelle enthält zwei Versionen jeder Eigenschaftsabrufmethode– eine Version ruft die Eigenschaft aus dem Cache ab, die andere ruft die Eigenschaft vom Anbieter ab. Weitere Informationen finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elements](uiauto-propertiesforclients.md).

4.  **Reagieren sie auf Benutzeroberflächenautomatisierung Ereignisse.**

    Benutzeroberflächenautomatisierung-Anbieter benachrichtigen Clients über Änderungen oder wichtige Vorkommen in der Benutzeroberfläche, indem sie Ereignisse auslösen. Clients müssen bestimmen, welche Ereignisse sie benötigen, und dann Schnittstellen zur Ereignisbehandlung implementieren und registrieren, um diese Ereignisse zu empfangen und zu verarbeiten. Weitere Informationen finden Sie unter [Abonnieren von Benutzeroberflächenautomatisierung Ereignissen.](uiauto-eventsforclients.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 