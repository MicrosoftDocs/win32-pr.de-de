---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter
description: Dieses Thema bietet einen Überblick darüber, wie Steuerelement Entwickler Benutzeroberflächenautomatisierungs-Anbieter implementieren.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Benutzeroberflächen Automatisierung, Übersicht über Anbieter
- Benutzeroberflächenautomatisierungs, Anbieter Typen
- Benutzeroberflächenautomatisierungs, Anbieter Konzepte
- Anbieter, Informationen zu
- Anbieter, Typen
- Anbieter, Konzepte
- Anbieter, Elemente
- Anbieter, Navigation
- Anbieter, Ansichten
- Anbieter, Frameworks
- Anbieter, Fragmente
- Anbieter, Hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947599"
---
# <a name="ui-automation-providers-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter

Ein Microsoft-Benutzeroberflächenautomatisierungs-Anbieter ist ein Software Objekt, das ein Element der Benutzeroberfläche einer Anwendung verfügbar macht, damit Client Anwendungen für die Barrierefreiheit Informationen über das Element abrufen und seine Funktionalität aufrufen können. Im allgemeinen verfügt jedes Steuerelement oder ein anderes unterschiedliches Element in einer Benutzeroberfläche über einen Anbieter.

Microsoft umfasst einen Anbieter für alle Standard Steuerelemente, die mit Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF) bereitgestellt werden. Dies bedeutet, dass die Standard Steuerelemente automatisch für Benutzeroberflächenautomatisierungs-Clients verfügbar gemacht werden. Sie müssen keine Barrierefreiheits Schnittstellen für die Standard Steuerelemente implementieren.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente enthält, müssen Sie Benutzeroberflächenautomatisierungs-Anbieter für diese Steuerelemente implementieren, um Sie für Client Anwendungen für Barrierefreiheit zugänglich zu machen. Außerdem müssen Sie Anbieter für alle Steuerelemente von Drittanbietern implementieren, die keinen Anbieter enthalten. Sie implementieren einen Anbieter durch Implementierung von Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen und Steuerelement Muster-Schnittstellen.

Dieses Thema bietet einen Überblick darüber, wie Steuerelement Entwickler Benutzeroberflächenautomatisierungs-Anbieter implementieren. Dies umfasst die folgenden Abschnitte.

-   [Anbietertypen](#types-of-providers)
-   [Konzepte für Benutzeroberflächenautomatisierungs-Anbieter](#ui-automation-provider-concepts)
    -   [Elemente](#elements)
    -   [Frameworks](#frameworks)
    -   [Fragmente](#fragments)
    -   [Hosts](#hosts)
-   [Zugehörige Themen](#related-topics)

## <a name="types-of-providers"></a>Anbietertypen

Benutzeroberflächenautomatisierungs-Anbieter werden in zwei Kategorien unterteilt: serverseitige Anbieter und Client seitige (oder *Proxy*-) Anbieter.

Ein serverseitiger Anbieter ist ein Objekt, z. b. ein benutzerdefiniertes Steuerelement, das seine eigene systemeigene Implementierung der relevanten Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen enthält. Ein serverseitiger Anbieter kommuniziert mit Client Anwendungen über die Prozess Grenze hinweg, indem er seine Implementierung der Anbieter Schnittstellen dem Benutzeroberflächenautomatisierungs-Kern bereitstellt, der Anforderungen von Clients verarbeitet. Weitere Informationen zu serverseitigen Anbietern finden Sie unter [Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-serversideprovider.md).

Bei einem Client seitigen Anbieter oder Proxy handelt es sich um ein Objekt, das Benutzeroberflächenautomatisierungs-Anbieter Schnittstellen implementiert, wenn ein Steuerelement keine eigene vollständige Anbieter Implementierung enthält. Ohne einen Proxy ist ein solches Steuerelement für die Automatisierung der Benutzeroberfläche größtenteils nicht transparent, sodass nur grundlegende Informationen, die über das Fenster Handle (**HWND**) verfügbar sind, bereitgestellt werden können, z. b. die Steuerungs Position In der Regel kommunizieren Proxy Anbieter über die Prozess Grenze hinweg mit der Anwendung, indem Sie Windows-Nachrichten senden und empfangen. Weitere Informationen finden Sie unter [Implementieren eines Client-Side-Benutzeroberflächenautomatisierungs-Anbieters (Proxy)](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Konzepte für Benutzeroberflächenautomatisierungs-Anbieter

Dieser Abschnitt bietet kurze Erläuterungen zu einer Auswahl von Schlüsselkonzepten, die Sie kennen müssen, um Benutzeroberflächenautomatisierungs-Anbieter implementieren zu können.

### <a name="elements"></a>Elemente

Benutzeroberflächenautomatisierungs-Elemente sind Teile der Benutzeroberfläche – normalerweise Windows oder Steuerelemente –, die für Benutzeroberflächenautomatisierungs-Clients sichtbar sind Zu den entsprechenden Beispielen zählen Anwendungsfenster, Bereiche, Schaltflächen, QuickInfos, Listenfelder und Listenelemente.

Benutzeroberflächenautomatisierungs-Elemente werden für Clients als-Struktur verfügbar gemacht. Die Benutzeroberflächen Automatisierung erstellt die Struktur durch Navigieren von einem Element zu einem anderen. Die Navigation wird vom Anbieter für jedes Element aktiviert. Jedes Element kann auf sein eigenes übergeordnetes Element, seine gleich geordneten Elemente und die ersten und letzten untergeordneten Elemente verweisen.

Ein Client kann die Benutzeroberflächenautomatisierungs-Struktur in drei Prinzipal Ansichten sehen, wie in der folgenden Tabelle beschrieben:



| Sicht         | BESCHREIBUNG                                                    |
|--------------|----------------------------------------------------------------|
| Rohdatenansicht     | Schließt alle-Elemente ein.                                         |
| Steuerelementansicht | Schließt Elemente ein, die Steuerelemente sind.                           |
| Inhaltsansicht | Schließt Steuerelemente ein, die dem Benutzerinformationen übermitteln. |



 

Für die Definition eines Elements als Inhaltselement oder Steuerelement ist die Anbieterimplementierung zuständig. Steuerelemente können auch Inhaltselemente sein, aber alle Inhaltselemente sind auch Steuerelemente.

Weitere Informationen zur Client Ansicht der-Struktur finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

### <a name="frameworks"></a>Frameworks

Ein Framework ist eine Komponente, die untergeordneten Steuerelemente, Treffertests und das Rendering in einem Bereich des Bildschirms verwaltet. Beispielsweise kann ein Win32-Fenster, das häufig als **HWND** bezeichnet wird, als Framework fungieren, das mehrere Benutzeroberflächenautomatisierungs-Elemente enthält, z. b. eine Menüleiste, eine Statusleiste und Schaltflächen.

Win32-Container Steuerelemente, wie z. b. Listenfelder und Strukturansicht-Steuerelemente, werden als Frameworks betrachtet, da Sie Ihren eigenen Code zum Rendern von untergeordneten Elementen und zum Ausführen von Treffer Tests enthalten. Im Gegensatz dazu ist ein WPF-Listenfeld kein Framework, da Rendering und Treffer Tests vom enthaltenden Fenster behandelt werden.

Die Benutzeroberfläche in einer Anwendung kann aus verschiedenen Frameworks bestehen. Beispielsweise kann ein **HWND** in einer Anwendung dynamisches HTML (DHTML) enthalten, das wiederum eine Komponente (z. b. ein Kombinations Feld in einem **HWND**) enthalten kann.

### <a name="fragments"></a>Fragments

Eine komplette Teilstruktur von Elementen eines bestimmten Frameworks wird als Fragment bezeichnet. Das Element im Stammknoten der Unterstruktur wird als Fragmentstamm bezeichnet. Ein Fragmentstamm besitzt kein übergeordnetes Element, wird aber innerhalb eines anderen Frameworks gehostet, in der Regel in einem Win32-Fenster (**HWND**).

### <a name="hosts"></a>Hosts

Der Stamm Knoten jedes Fragments muss in einem-Element gehostet werden, in der Regel in einem Win32-Fenster (**HWND**). Die Ausnahme stellt der Desktop dar, der in keinem anderen Element gehostet wird. Der Host eines benutzerdefinierten Steuer Elements ist das **HWND** des Steuer Elements selbst, nicht das Anwendungsfenster oder ein anderes Fenster, das möglicherweise Gruppen von Steuerelementen der obersten Ebene enthält.

Der Host eines Fragments spielt eine wichtige Rolle beim Bereitstellen von Benutzeroberflächenautomatisierungs-Diensten. Er ermöglicht die Navigation zum Fragmentstamm und stellt einige Standardeigenschaften bereit, damit diese nicht vom benutzerdefinierten Anbieter implementiert werden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren eines Client-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters](uiauto-serversideprovider.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




