---
title: Vergleich von Microsoft Active Accessibility und Benutzeroberflächen Automatisierung
description: In diesem Thema werden die Hauptunterschiede zwischen Microsoft Active Accessibility und der Benutzeroberflächen Automatisierung zusammengefasst.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340725"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Vergleich von Microsoft Active Accessibility und Benutzeroberflächen Automatisierung

Die Windows Automation-API besteht aus zwei Technologien – Microsoft Active Accessibility und Microsoft UI Automation. Bei Microsoft Active Accessibility handelt es sich um die Legacy-Barrierefreiheits Technologie, die als Plattform-Add-in für Windows 95 eingeführt wurde, während die Benutzeroberflächen Automatisierung eine neuere, leistungsfähigere Technologie ist, die die in Microsoft Active Accessibility enthaltenen Einschränkungen überschreitet.

In diesem Thema werden die Hauptunterschiede zwischen Microsoft Active Accessibility und der Benutzeroberflächen Automatisierung zusammengefasst. Er enthält folgende Abschnitte:

-   [Grundlegende Entwurfs Prinzipien](#basic-design-principles)
-   [Eigenschaften und Steuerelement Muster](#properties-and-control-patterns)
-   [MSAA-Rollen und Benutzeroberflächenautomatisierungs-Steuerungs Muster](#msaa-roles-and-ui-automation-control-patterns)
-   [Objektmodell Navigation](#object-model-navigation)
-   [Objektmodell Erweiterbarkeit](#object-model-extensibility)
-   [Übergang von MSAA](#transitioning-from-msaa)
-   [Auswählen von Microsoft Active Accessibility, UI-Automatisierung oder iaccessibleex](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Neue Anwendungen und Steuerelemente](#new-applications-and-controls)
    -   [Vorhandene Microsoft Active Accessibility-Implementierungen](#existing-microsoft-active-accessibility-implementations)
-   [Zugehörige Themen](#related-topics)

## <a name="basic-design-principles"></a>Grundlegende Entwurfs Prinzipien

Obwohl es sich bei Microsoft Active Accessibility und Benutzeroberflächen Automatisierung um zwei verschiedene Technologien handelt, sind die grundlegenden Entwurfs Prinzipien ähnlich. Der Zweck beider Technologien besteht darin, umfangreiche Informationen zu den in Windows-Anwendungen verwendeten Benutzeroberflächen Elementen verfügbar zu machen. Entwickler von Barrierefreiheits Tools können diese Informationen verwenden, um Software zu erstellen, mit der Anwendungen, die auf Windows ausgeführt werden, für Personen mit Sehbehinderung, Hörbehinderungen oder Bewegungsbehinderungen besser zugänglich sind.

Sowohl Microsoft Active Accessibility als auch UI Automation machen das UI-Objektmodell als hierarchische Struktur verfügbar, die auf dem Desktop verankert ist. Microsoft Active Accessibility stellt einzelne Benutzeroberflächen Elemente als *barrierefreie Objekte* dar, und die Benutzeroberflächen Automatisierung stellt Sie als *Automatisierungselemente* dar. Beide verweisen auf das Barrierefreiheits Tool oder das Software Automatisierungs Programm als *Client*. Microsoft Active Accessibility bezieht sich jedoch auf die Anwendung oder das Steuerelement, das die Benutzeroberfläche für Barrierefreiheit als *Server* bereitstellt, während die Benutzeroberflächen Automatisierung dies als *Anbieter* bezeichnet.

## <a name="properties-and-control-patterns"></a>Eigenschaften und Steuerelement Muster

Microsoft Active Accessibility bietet eine einzige Component Object Model (com)-Schnittstelle mit einer festgelegten, kleinen Gruppe von Eigenschaften. Die Benutzeroberflächen Automatisierung bietet einen umfassenderen Satz von Eigenschaften sowie eine Reihe erweiterter Schnittstellen, die als *Steuerelement Muster* bezeichnet werden, um barrierefreie Objekte in einer Weise zu bearbeiten, die Microsoft Active Accessibility

Weitere Informationen finden Sie unter [UI Automation Properties Overview](uiauto-propertiesoverview.md) und [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>MSAA-Rollen und Benutzeroberflächenautomatisierungs-Steuerungs Muster

Microsoft hat das Microsoft Active Accessibility-Objektmodell zur gleichen Zeit wie Windows 95 entwickelt. Das Modell basiert auf "Rollen", die vor einem Jahrzehnt definiert wurden, und Sie können keine neuen Benutzeroberflächen Verhalten unterstützen oder zwei oder mehr Rollen zusammenführen. Es gibt z. b. kein Textobjekt Modell, um Hilfstechnologien bei der Bewältigung komplexer Webinhalte zu unterstützen. Die Benutzeroberflächen Automatisierung überschreitet diese Einschränkungen durch die Einführung von Steuerungs Mustern, die es Objekten ermöglichen, mehr als eine Rolle zu unterstützen, und [das Steuerelement](uiauto-implementingtextandtextrange.md) Muster für die Benutzeroberflächen Automatisierung bietet ein vollständiges Textobjekt Modell.

## <a name="object-model-navigation"></a>Objektmodell Navigation

Eine weitere Einschränkung von Microsoft Active Accessibility besteht darin, das Objektmodell zu navigieren. Microsoft Active Accessibility stellt die Benutzeroberfläche als Hierarchie von zugänglichen Objekten dar. Clients Navigieren mithilfe von Schnittstellen und Methoden, die über das barrierefreie Objekt verfügbar sind, von einem zugänglichen Objekt zu einem anderen. Server können die untergeordneten Elemente eines barrierefreien Objekts mit Eigenschaften der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle oder mit der standardmäßigen [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -com-Schnittstelle verfügbar machen. Clients müssen jedoch in der Lage sein, beide Ansätze für jeden Server zu behandeln. Diese Mehrdeutigkeit bedeutet zusätzliche Arbeit für clientimplementierer und beschädigte barrierefreie Objekt Modelle für Server Implementierer.

Die Benutzeroberflächen Automatisierung stellt die Benutzeroberfläche als hierarchische Struktur von Automatisierungs Elementen dar und bietet eine einzelne Schnittstelle zum Navigieren in der Struktur. Clients können die Ansicht der Elemente in der Struktur anpassen, indem Sie Bereichs-und Filter Vorgänge festlegen.

## <a name="object-model-extensibility"></a>Objektmodell Erweiterbarkeit

Eigenschaften und Funktionen von Microsoft Active Accessibility können nicht ohne Unterbrechung oder Änderung der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -com-Schnittstellen Spezifikation erweitert werden. Das Ergebnis ist, dass das neue Steuerelement Verhalten nicht durch das Objektmodell verfügbar gemacht werden kann. Es ist in der Regel statisch.

Bei der Automatisierung der Benutzeroberfläche können Anwendungsentwickler benutzerdefinierte Eigenschaften, Steuerelement Muster und Ereignisse einführen, um die neuen Elemente zu beschreiben. Weitere Informationen finden Sie unter [benutzerdefinierte Eigenschaften, Ereignisse und Steuerelement Muster](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Übergang von MSAA

Das Windows Automation-API-Framework bietet Unterstützung für den Übergang von Microsoft Active Accessibility-Servern zu Benutzeroberflächenautomatisierungs-Anbietern. Die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle ermöglicht die Unterstützung spezifischer Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster, die älteren Microsoft Active Accessibility-Servern hinzugefügt werden, ohne dass die gesamte Implementierung neu geschrieben werden muss Mit der **iaccessibleex** -Schnittstelle können auch Prozess interne Microsoft Active Accessibility-Clients direkt auf Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen zugreifen, anstatt über Benutzeroberflächenautomatisierungs-Client Schnittstellen. Weitere Informationen finden Sie [unter iaccessibleex Interface](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Auswählen von Microsoft Active Accessibility, UI-Automatisierung oder iaccessibleex

In diesem Abschnitt erfahren Sie, welche Windows Automation-API-Lösung verwendet wird, um ein Hilfstechnologieprodukt zu implementieren oder Ihre Anwendung für Hilfstechnologieprodukte zugänglich zu machen.

### <a name="new-applications-and-controls"></a>Neue Anwendungen und Steuerelemente

Wenn Sie eine neue Anwendung oder ein neues Steuerelement entwickeln, empfiehlt Microsoft die Verwendung der Benutzeroberflächen Automatisierung. Obwohl Microsoft Active Accessibility kurzfristig einfacher implementiert werden kann, sind die Einschränkungen dieser Technologie, wie z. b. Das Aging-Objektmodell, und die Möglichkeit, das neue Verhalten der Benutzeroberfläche oder die mergerollen nicht zu unterstützen, langfristig schwieriger und kostengünstiger. Diese Einschränkungen sind besonders offensichtlich, wenn neue Steuerelemente eingeführt werden.

Das Benutzeroberflächenautomatisierungs-Objektmodell ist einfacher zu verwenden und flexibler als das von Microsoft Active Accessibility. Die Benutzeroberflächenautomatisierungs-Elemente reflektieren die Entwicklung von Benutzeroberflächen, und Entwickler können benutzerdefinierte Steuerelement Muster, Eigenschaften und Ereignisse für die Benutzeroberflächen Automatisierung definieren.

Microsoft Active Accessibility wird tendenziell langsam für Clients ausgeführt, die nicht mehr verarbeitet werden. Um die Leistung zu verbessern, wählen Entwickler von Tools für Barrierefreiheits Tools häufig aus, um Ihre Programme in den Ziel Anwendungsprozess einzuschließen und auszuführen: ein äußerst schwieriger und riskanter Ansatz. Die Automatisierung der Benutzeroberfläche ist für prozessübergreifende Clients viel einfacher zu implementieren und bietet eine wesentlich bessere Leistung und Zuverlässigkeit.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Vorhandene Microsoft Active Accessibility-Implementierungen

Wenn Sie eine vorhandene Anwendung oder ein Steuerelement aktualisieren, die auf Microsoft Active Accessibility basiert, sollten Sie die Unterstützung für die Benutzeroberflächen Automatisierung durch Implementieren der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle hinzufügen. Stellen Sie zunächst sicher, dass Ihre Anwendung oder das Steuerelement die folgenden Anforderungen erfüllt:

-   Die Baseline der Hierarchie von zugänglichen Objekten von Microsoft Active Accessibility Server muss gut organisiert und fehlerfrei sein. [**Iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) kann Probleme mit vorhandenen zugänglichen Objekt Hierarchien nicht beheben.
-   Ihre [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung muss sowohl den Microsoft Active Accessibility Specification als auch der Benutzeroberflächenautomatisierungs-Spezifikation entsprechen. Microsoft stellt eine Reihe von Tools zum Überprüfen der Konformität mit beiden Spezifikationen bereit. Weitere Informationen finden Sie unter [TestTools](testing-tools.md).

Wenn eine dieser Anforderungen nicht erfüllt ist, sollten Sie die Benutzeroberflächen Automatisierung nativ implementieren. Wenn dies erforderlich ist, können Sie Legacy-Microsoft Active Accessibility Server-Implementierungen für die Abwärtskompatibilität beibehalten. Aus Sicht des Benutzeroberflächenautomatisierungs-Clients besteht kein Unterschied zwischen Benutzeroberflächenautomatisierungs-Anbietern und Microsoft Active Accessibility-Servern, die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) korrekt implementieren.

Weitere Informationen finden Sie [unter iaccessibleex Interface](iaccessibleex.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows Automation-API](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung](entry-uiauto-win32.md)
</dt> <dt>

[Die iaccessibleex-Schnittstelle](iaccessibleex.md)
</dt> </dl>

 

 