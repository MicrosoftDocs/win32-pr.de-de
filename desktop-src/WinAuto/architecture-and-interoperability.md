---
title: Architektur und Interoperabilität
description: In diesem Thema wird die Architektur von Microsoft Active Accessibility und der Microsoft-Benutzeroberflächen Automatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen auf der Grundlage der beiden unterschiedlichen Technologien ermöglichen.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104101186"
---
# <a name="architecture-and-interoperability"></a>Architektur und Interoperabilität

In diesem Thema wird die Architektur von Microsoft Active Accessibility und der Microsoft-Benutzeroberflächen Automatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen auf der Grundlage der beiden unterschiedlichen Technologien ermöglichen.

Weitere Informationen zur Interoperabilität von Microsoft Active Accessibility und zur Benutzeroberflächen Automatisierung finden Sie unter [Common Infrastructure (allgemeine Infrastruktur](common-infrastructure.md)).

Dieses Thema enthält folgende Abschnitte:

-   [Microsoft Active Accessibility-Architektur](#microsoft-active-accessibility-architecture)
-   [Architektur der Benutzeroberflächen Automatisierung](#ui-automation-architecture)
-   [Interoperabilität von Microsoft Active Accessibility und UI-Automatisierung](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Die iaccessibleex-Schnittstelle](#the-iaccessibleex-interface)
-   [Zugehörige Themen](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Microsoft Active Accessibility-Architektur

Microsoft Active Accessibility stellt grundlegende Informationen zu Steuerelementen, wie z. b. den Steuerelement Namen, den Speicherort auf dem Bildschirm und die Art der Steuerung, sowie Zustandsinformationen wie Sichtbarkeit und aktivierten/deaktivierten Die Benutzeroberfläche wird als Hierarchie barrierefreier Objekte dargestellt. Änderungen und Aktionen werden als WinEvents dargestellt.

Microsoft Active Accessibility besteht aus den folgenden Komponenten:

-   Barrierefreies Objekt – ein logisches UI-Element (z. b. eine Schaltfläche), das durch eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Component Object Model (com)-Schnittstelle und einen untergeordneten ganzzahligen Bezeichner (childID) dargestellt
-   WinEvents – ein Ereignis System, mit dem Server Clients benachrichtigen können, wenn ein Barrierefreies Objekt geändert wird. Weitere Informationen finden Sie unter [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll – die Laufzeit, Dynamic Link Library, die die Microsoft Active Accessibility-API und das Barrierefreiheits System Framework bereitstellt. Oleacc implementiert Proxy Objekte, die standardmäßige Barrierefreiheits Informationen für Standardbenutzer Oberflächen Elemente bereitstellen, einschließlich Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente.

Bei Microsoft Active Accessibility unterstützt die Systemkomponente des Barrierefreiheits-Frameworks (oleacc) die Kommunikation zwischen Hilfstechnologien (Barrierefreiheits Tools) und Anwendungen, wie in der folgenden Abbildung veranschaulicht.

![Abbildung, die zeigt, wie Barrierefreiheits Tools mit Anwendungen interagieren](images/msaaarch.gif)

Die Anwendungen (Microsoft Active Accessibility-Server) stellen Informationen zur Benutzeroberflächen-Barrierefreiheit für Tools (Microsoft Active Accessibility-Clients) bereit, die im Namen von Benutzern mit der Benutzeroberfläche interagieren. Die Code Grenze ist sowohl eine programmgesteuerte als auch eine Prozess Grenze.

## <a name="ui-automation-architecture"></a>Architektur der Benutzeroberflächen Automatisierung

Bei der Automatisierung der Benutzeroberfläche wird die Benutzeroberflächenautomatisierungs-Kernkomponente (UIAutomationCore.dll) sowohl in die Tools für die Barrierefreiheit als auch in die Anwendungsprozesse geladen. Die Kernkomponente verwaltet die prozessübergreifende Kommunikation, bietet Dienste höherer Ebene, wie z. b. das Suchen nach Elementen nach Eigenschafts Werten, und ermöglicht das Massen abrufen oder Zwischenspeichern von Eigenschaften, was eine bessere Leistung als die Implementierung von Microsoft Active Accessibility bietet.

Die Benutzeroberflächen Automatisierung umfasst Proxy Objekte, die Benutzeroberflächen Informationen über Standardbenutzer Oberflächen Elemente wie Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente bereitstellen. Außerdem sind Proxys enthalten, mit denen Benutzeroberflächenautomatisierungs-Clients Benutzeroberflächen Informationen von Microsoft Active Accessibility-Servern erhalten.

Die folgende Abbildung zeigt die Beziehungen zwischen den verschiedenen Benutzeroberflächenautomatisierungs-Komponenten, die in Barrierefreiheits Tools (Clients) und in Anwendungen (Anbietern) verwendet werden.

![Abbildung, die zeigt, wie Komponenten von Barrierefreiheits Tools mit Anwendungen in Anwendungen interagieren](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Interoperabilität von Microsoft Active Accessibility und UI-Automatisierung

Mithilfe der Benutzeroberflächen Automatisierung an Microsoft Active Accessibility Bridge können Microsoft Active Accessibility-Clients auf Benutzeroberflächenautomatisierungs-Anbieter zugreifen, indem Sie das Objektmodell für die Benutzeroberflächen Automatisierung in ein Microsoft Active Accessibility-Objektmodell In der folgenden Abbildung wird die Rolle der Benutzeroberflächen Automatisierung-zu-Microsoft-Active Accessibility Bridge gezeigt.

![Darstellung der Funktionsweise der Benutzeroberflächen Automatisierung mit Barrierefreiheits Tools und-Anwendungen](images/uiatomsaabridge.gif)

Entsprechend übersetzt der Microsoft Active Accessibility-to-UI-Automatisierungs Proxy Microsoft Active Accessibility-basierte Server Objekt Modelle für Benutzeroberflächenautomatisierungs-Clients. In der folgenden Abbildung wird die Rolle des Microsoft Active Accessibility-to-UI-Automatisierungs Proxys gezeigt.

![Abbildung der Funktionsweise des Benutzeroberflächenautomatisierungs-Proxys mit Tools und Anwendungen](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>Die iaccessibleex-Schnittstelle

Mit der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle können vorhandene Anwendungen oder Benutzeroberflächen Bibliotheken Ihr Microsoft Active Accessibility-Objektmodell erweitern, um die Benutzeroberflächen Automatisierung zu unterstützen, ohne die Implementierung von Grund auf neu schreiben Mit **iaccessibleex** können Sie nur die zusätzlichen Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster implementieren, die erforderlich sind, um die Benutzeroberfläche und ihre Funktionalität vollständig zu beschreiben.

Da der Microsoft Active Accessibility-to-UI-Automatisierungs Proxy die Objekt Modelle von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-fähigen Microsoft Active Accessibility Servern als Benutzeroberflächenautomatisierungs-Objekt Modelle übersetzt, müssen Benutzeroberflächenautomatisierungs-Clients keine zusätzlichen Aufgaben erledigen. Mit der **iaccessibleex** -Schnittstelle können auch Prozess interne Microsoft Active Accessibility-Clients für die direkte Interaktion mit Benutzeroberflächenautomatisierungs-Anbietern aktiviert werden.

Weitere Informationen finden Sie [unter iaccessibleex Interface](iaccessibleex.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows Automation-API](windows-automation-api-overview.md)
</dt> <dt>

[Die iaccessibleex-Schnittstelle](iaccessibleex.md)
</dt> <dt>

[Sicherheitsüberlegungen für Hilfstechnologien](uiauto-securityoverview.md)
</dt> </dl>

 

 




