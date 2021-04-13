---
title: Übersicht über UI-Automatisierungs Clients
description: In diesem Thema werden die Hauptaufgaben beschrieben, die bei der Implementierung einer Microsoft UI Automation-Client Anwendung beteiligt sind.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- UI-Automatisierung, Übersicht über Clients
- Clients, Informationen zu
- Clients, Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390404"
---
# <a name="ui-automation-clients-overview"></a>Übersicht über UI-Automatisierungs Clients

In diesem Thema werden die Hauptaufgaben beschrieben, die bei der Implementierung einer Microsoft UI Automation-Client Anwendung beteiligt sind.

Ein Benutzeroberflächenautomatisierungs-Client ist eine beliebige Anwendung, die mithilfe der Benutzeroberflächenautomatisierungs-API auf Informationen über Benutzeroberflächen Elemente zugreift oder Anwendungen mittels Programm gesteuerter Bearbeitung Ihrer Benutzeroberflächen Elemente steuert. Benutzeroberflächenautomatisierungs-Clients schließen Hilfstechnologieanwendungen ein, z. b. Sprachausgaben, die Informationen über Benutzeroberflächen Elemente abrufen und die Informationen auf eine Weise darstellen, die für Personen mit Behinderungen geeignet ist. Dazu zählen auch Anwendungen wie sprach Erkennungs Programme und Tools zum Testen von Software, die die Benutzeroberflächen Automatisierung anstelle der Maus und Tastatur zum "Steuern" anderer Anwendungen verwenden.

Aus Sicht der Benutzeroberflächen Automatisierung müssen die Hauptaufgaben, die eine Benutzeroberflächenautomatisierungs-Client Anwendung ausführen muss, Folgendes umfassen:

1.  **Rufen Sie eine Instanz des cuiautomation-Objekts ab.**

    Informationen zu Benutzeroberflächen Elementen und zum Zugriff auf die Funktionalität des Benutzeroberflächen Elements werden von Benutzeroberflächenautomatisierungs-Anbietern für Clients verfügbar gemacht. Client Anwendungen funktionieren jedoch nicht direkt mit Anbietern. Stattdessen liegt ein Kerndienst zwischen dem Client und dem Anbieter. Wenn ein Client die Benutzeroberflächenautomatisierungs-API aufruft, ruft er tatsächlich den Benutzeroberflächenautomatisierungs-Kerndienst auf, der wiederum Aufrufe an die vom Anbieter implementierten Schnittstellen durchführt.

    Um Zugriff auf den Automation-Kerndienst zu erhalten, muss ein Client eine Instanz des [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) -Objekts erstellen und einen [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstellen Zeiger für das-Objekt abrufen. Der **iuiautomation** -Zeiger ist der Client Schlüssel für den Zugriff auf alle Benutzeroberflächenautomatisierungs-Funktionen, die für den Client verfügbar sind. Weitere Informationen finden Sie unter [Erstellen des cuiautomation-Objekts](uiauto-creatingcuiautomation.md).

2.  **Abrufen von iuiautomationelement-Schnittstellen für UI-Elemente aus der Benutzeroberflächenautomatisierungs-Struktur.**

    Die Benutzeroberflächen Automatisierung macht einzelne Benutzeroberflächen Elemente als Objekte verfügbar, die die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle implementieren. Informationen zu einem Element stehen den Clients über Eigenschaften zur Verfügung, die von der **iuiautomationelement** -Schnittstelle des Elements verfügbar gemacht werden, sowie über den Zugriff auf die Steuerelement Muster des Elements. Eigenschaften und Methoden, die von den Steuerelement Muster-Schnittstellen verfügbar gemacht werden, ermöglichen den Zugriff auf Steuerungs spezifische Informationen und Funktionen.

    Die Elemente der Benutzeroberflächenautomatisierungs-Elemente werden für Clients in einer hierarchischen Struktur bereitgestellt, die als UI Automation Tree bezeichnet wird. Clients verwenden Methoden, die von der [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle verfügbar gemacht werden, um [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstellen für Benutzeroberflächen Elemente in der Struktur abzurufen, und um andere Schnittstellen abzurufen, mit denen die Struktur nach Elementen gesucht wird, die einem bestimmten Satz von Kriterien entsprechen Weitere Informationen finden Sie unter Abrufen von Benutzeroberflächenautomatisierungs- [Elementen](uiauto-obtainingelements.md).

    Beim Abrufen von Benutzeroberflächen Elementen können Clients die Systemleistung mithilfe der zwischen Speicherungs Funktionen der Benutzeroberflächen Automatisierung verbessern. Durch das Caching kann ein Client eine Reihe von Eigenschaften und Steuerelement Mustern angeben, die zusammen mit dem Element abgerufen werden sollen. Bei einem einzelnen prozessübergreifende-Befehl ruft die Benutzeroberflächen Automatisierung das-Element und die angegebenen Eigenschaften und Steuerelement Muster ab und speichert Sie dann im Cache. Ohne Caching ist ein separater interprozessaufrufbedarf erforderlich, um die einzelnen Eigenschaften oder Steuerelement Muster abzurufen. Weitere Informationen finden Sie unter zwischen [Speichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern](uiauto-cachingforclients.md).

3.  **Abrufen der Eigenschaften von Benutzeroberflächen Elementen und Aufrufen der Funktionalität des Benutzeroberflächen Elements**

    Clients verwenden die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle, um die Eigenschaften und Steuerelement Muster eines Elements abzurufen. Die-Schnittstelle enthält zwei Versionen der einzelnen Eigenschaften Abruf Methoden – eine Version Ruft die-Eigenschaft aus dem Cache ab, der andere Ruft die-Eigenschaft vom Anbieter ab. Weitere Informationen finden Sie unter [Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen](uiauto-propertiesforclients.md).

4.  **Reagieren auf Benutzeroberflächenautomatisierungs-Ereignisse.**

    Benutzeroberflächenautomatisierungs-Anbieter benachrichtigen Clients über Änderungen oder wichtige Vorkommen in der Benutzeroberfläche, indem Sie Ereignisse ausgeben. Clients müssen bestimmen, welche Ereignisse Sie benötigen, und dann Ereignis Behandlungs Schnittstellen implementieren und registrieren, um diese Ereignisse zu empfangen und zu verarbeiten. Weitere Informationen finden Sie unter [Abonnieren von Benutzeroberflächenautomatisierungs-Ereignissen](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> </dl>

 

 