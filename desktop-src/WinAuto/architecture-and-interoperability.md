---
title: Architektur und Interoperabilität
description: In diesem Thema werden kurz die Architektur von Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen ermöglichen, die auf den beiden verschiedenen Technologien basieren.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b146fa2d628ff64d2dcf714a1f860bee28c2f0f816e057f6b411e8344462fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053018"
---
# <a name="architecture-and-interoperability"></a>Architektur und Interoperabilität

In diesem Thema werden kurz die Architektur von Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung sowie die Komponenten beschrieben, die die Interoperabilität zwischen Anwendungen ermöglichen, die auf den beiden verschiedenen Technologien basieren.

Weitere Informationen zur Interoperabilität Microsoft Active Accessibility Benutzeroberflächenautomatisierung finden Sie unter [Allgemeine Infrastruktur.](common-infrastructure.md)

Dieses Thema enthält folgende Abschnitte:

-   [Microsoft Active Accessibility Architektur](#microsoft-active-accessibility-architecture)
-   [Benutzeroberflächenautomatisierung Architektur](#ui-automation-architecture)
-   [Microsoft Active Accessibility und Benutzeroberflächenautomatisierung Interoperabilität](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [Die IAccessibleEx-Schnittstelle](#the-iaccessibleex-interface)
-   [Zugehörige Themen](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Microsoft Active Accessibility Architektur

Microsoft Active Accessibility stellt grundlegende Informationen zu Steuerelementen wie Steuerelementname, Position auf dem Bildschirm und Steuerelementtyp sowie Zustandsinformationen wie Sichtbarkeit und Aktiviert/Deaktiviert-Status zur Verfügung. Die Benutzeroberfläche wird als Hierarchie von barrierefreien Objekten dargestellt. Änderungen und Aktionen werden als WinEvents dargestellt.

Microsoft Active Accessibility besteht aus den folgenden Komponenten:

-   Barrierefreies Objekt– Ein logisches Benutzeroberflächenelement (z. B. eine Schaltfläche), das durch eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model-Schnittstelle (COM) und einen untergeordneten Integerbezeichner (ChildID) dargestellt wird.
-   WinEvents: Ein Ereignissystem, mit dem Server Clients benachrichtigen können, wenn sich ein barrierefreies Objekt ändert. Weitere Informationen finden Sie unter [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll: Die Laufzeitbibliothek mit dynamischem Link, die die Microsoft Active Accessibility-API und das Framework für Barrierefreiheit bietet. OLEACC implementiert Proxyobjekte, die Standardinformationen zur Barrierefreiheit für Standardelemente der Benutzeroberfläche bereitstellen, einschließlich USER-Steuerelementen, BENUTZERmenüs und allgemeinen Steuerelementen.

Beispielsweise Microsoft Active Accessibility die Systemkomponente des Barrierefreiheitsframework (OLEACC) die Kommunikation zwischen Hilfstechnologien (Barrierefreiheitstools) und Anwendungen, wie in der folgenden Abbildung dargestellt.

![Abbildung, die zeigt, wie Barrierefreiheitstools mit Anwendungen interagieren](images/msaaarch.gif)

Die Anwendungen (Microsoft Active Accessibility Server) stellen Informationen zur Barrierefreiheit der Benutzeroberfläche für Tools (Microsoft Active Accessibility Clients) zur Verfügung, die im Auftrag von Benutzern mit der Benutzeroberfläche interagieren. Die Codegrenze ist sowohl eine programmgesteuerte als auch eine Prozessgrenze.

## <a name="ui-automation-architecture"></a>Benutzeroberflächenautomatisierung Architektur

Mit Benutzeroberflächenautomatisierung wird die Benutzeroberflächenautomatisierung-Kernkomponente (UIAutomationCore.dll) sowohl in die Prozesse der Barrierefreiheitstools als auch der Anwendungen geladen. Die Kernkomponente verwaltet die prozessübergreifende Kommunikation, bietet Dienste auf höherer Ebene wie das Suchen nach Elementen nach Eigenschaftswerten und ermöglicht das Massenabrufen oder Zwischenspeichern von Eigenschaften, was eine bessere Leistung als die Microsoft Active Accessibility bietet.

Benutzeroberflächenautomatisierung enthält Proxyobjekte, die Benutzeroberflächeninformationen zu Standardelementen der Benutzeroberfläche bereitstellen, z. B. USER-Steuerelemente, BENUTZERmenüs und allgemeine Steuerelemente. Es enthält auch Proxys, die es Benutzeroberflächenautomatisierung Clients ermöglichen, Benutzeroberflächeninformationen von Microsoft Active Accessibility erhalten.

Die folgende Abbildung zeigt die Beziehungen zwischen den verschiedenen Benutzeroberflächenautomatisierung, die in Barrierefreiheitstools (Clients) und in Anwendungen (Anbietern) verwendet werden.

![Abbildung, die zeigt, wie Komponenten von Barrierefreiheitstools mit denen in Anwendungen interagieren](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Microsoft Active Accessibility und Benutzeroberflächenautomatisierung Interoperabilität

Die Benutzeroberflächenautomatisierung zu Microsoft Active Accessibility Bridge ermöglicht Microsoft Active Accessibility-Clients den Zugriff auf Benutzeroberflächenautomatisierung-Anbieter, indem das Benutzeroberflächenautomatisierung-Objektmodell in ein Microsoft Active Accessibility-Objektmodell konvertiert wird. Die folgende Abbildung zeigt die Rolle der Benutzeroberflächenautomatisierung-zu-Microsoft Active Accessibility Bridge.

![Abbildung zur Funktionsweise der Benutzeroberflächenautomatisierung mit Barrierefreiheitstools und -anwendungen](images/uiatomsaabridge.gif)

Entsprechend übersetzt der Microsoft Active Accessibility-zu-Benutzeroberflächenautomatisierung-Proxy Microsoft Active Accessibility-basierten Serverobjektmodelle für Benutzeroberflächenautomatisierung Clients. Die folgende Abbildung zeigt die Rolle des Microsoft Active Accessibility-zu-Benutzeroberflächenautomatisierung Proxys.

![Abbildung zur Funktionsweise des Benutzeroberflächenautomatisierungs-Proxys mit Barrierefreiheitstools und -anwendungen](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>Die IAccessibleEx-Schnittstelle

Die [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ermöglicht vorhandenen Anwendungen oder Benutzeroberflächenbibliotheken, ihr Microsoft Active Accessibility-Objektmodell zu erweitern, um Benutzeroberflächenautomatisierung zu unterstützen, ohne die Implementierung von Grund auf neu zu schreiben. Mit **IAccessibleEx** können Sie nur die zusätzlichen Benutzeroberflächenautomatisierung und Steuerelementmuster implementieren, die zum vollständigen Beschreiben der Benutzeroberfläche und ihrer Funktionalität erforderlich sind.

Da der Microsoft Active Accessibility-zu-Benutzeroberflächenautomatisierung-Proxy die Objektmodelle von [**IAccessibleEx-fähigen**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)Microsoft Active Accessibility-Servern als Benutzeroberflächenautomatisierung-Objektmodelle übersetzt, müssen Benutzeroberflächenautomatisierung-Clients keine zusätzlichen Arbeiten mehr tun. Die **IAccessibleEx-Schnittstelle** kann auch prozessintern Microsoft Active Accessibility clients ermöglichen, direkt mit Benutzeroberflächenautomatisierung interagieren.

Weitere Informationen finden Sie unter [Die IAccessibleEx-Schnittstelle.](iaccessibleex.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Übersicht über die Automation-API](windows-automation-api-overview.md)
</dt> <dt>

[Die IAccessibleEx-Schnittstelle](iaccessibleex.md)
</dt> <dt>

[Sicherheitsüberlegungen für Hilfstechnologien](uiauto-securityoverview.md)
</dt> </dl>

 

 




