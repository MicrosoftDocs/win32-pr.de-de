---
title: Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter
description: Dieses Thema bietet eine Übersicht darüber, wie Steuerelemententwickler Benutzeroberflächenautomatisierung Anbieter implementieren.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- übersicht über Benutzeroberflächenautomatisierung, Anbieter
- Benutzeroberflächenautomatisierung, Anbietertypen
- Benutzeroberflächenautomatisierung,Anbieterkonzepte
- providers,about
- providers,types
- Anbieter, Konzepte
- providers,elements
- Providers, Navigation
- providers,views
- Anbieter, Frameworks
- providers,fragments
- providers,hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03480fd77ec75a7747d0cc425d38b6160a3b001df275e9f0e50cbf397b1e15a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826846"
---
# <a name="ui-automation-providers-overview"></a>Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter

Ein Microsoft Benutzeroberflächenautomatisierung-Anbieter ist ein Softwareobjekt, das ein Element der Benutzeroberfläche einer Anwendung verfügbar macht, sodass Clientanwendungen für die Barrierefreiheit Informationen über das Element abrufen und dessen Funktionalität aufrufen können. Im Allgemeinen verfügt jedes Steuerelement oder ein anderes eindeutiges Element in einer Benutzeroberfläche über einen Anbieter.

Microsoft umfasst einen Anbieter für jedes standard-Steuerelement, das mit Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF) bereitgestellt wird. Dies bedeutet, dass die Standardsteuerelemente automatisch für Benutzeroberflächenautomatisierung Clients verfügbar gemacht werden. Sie müssen keine Barrierefreiheitsschnittstellen für die Standardsteuerelemente implementieren.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente enthält, müssen Sie Benutzeroberflächenautomatisierung-Anbieter für diese Steuerelemente implementieren, damit sie für Clientanwendungen für Barrierefreiheit zugänglich sind. Außerdem müssen Sie Anbieter für Steuerelemente von Drittanbietern implementieren, die keinen Anbieter enthalten. Sie implementieren einen Anbieter, indem Sie Benutzeroberflächenautomatisierung Anbieterschnittstellen und Steuerelementmusterschnittstellen implementieren.

Dieses Thema bietet eine Übersicht darüber, wie Steuerelemententwickler Benutzeroberflächenautomatisierung Anbieter implementieren. Sie enthält die folgenden Abschnitte.

-   [Anbietertypen](#types-of-providers)
-   [Konzepte für Benutzeroberflächenautomatisierungs-Anbieter](#ui-automation-provider-concepts)
    -   [CreateUiDefinition-Elemente](#elements)
    -   [Frameworks](#frameworks)
    -   [Fragmente](#fragments)
    -   [Hosts](#hosts)
-   [Zugehörige Themen](#related-topics)

## <a name="types-of-providers"></a>Anbietertypen

Benutzeroberflächenautomatisierung Anbieter lassen sich in zwei Kategorien unterteilen: serverseitige Anbieter und clientseitige Anbieter (oder *Proxyanbieter).*

Ein serverseitiger Anbieter ist ein Objekt, z. B. ein benutzerdefiniertes Steuerelement, das seine eigene native Implementierung der relevanten Benutzeroberflächenautomatisierung Anbieterschnittstellen enthält. Ein serverseitiger Anbieter kommuniziert mit Clientanwendungen über die Prozessgrenze hinweg, indem seine Implementierung der Anbieterschnittstellen für den Benutzeroberflächenautomatisierung Core verfügbar ist, der Anforderungen von Clients verarbeitet. Weitere Informationen zu serverseitigen Anbietern finden Sie unter [Implementieren eines Server-Side Benutzeroberflächenautomatisierung-Anbieters.](uiauto-serversideprovider.md)

Ein clientseitiger Anbieter oder Proxy ist ein Objekt, das Benutzeroberflächenautomatisierung Anbieterschnittstellen im Auftrag eines Steuerelements implementiert, das keine eigene vollständige Anbieterimplementierungen enthält. Ohne Proxy ist ein solches Steuerelement für Benutzeroberflächenautomatisierung größtenteils nicht transparent, was nur grundlegende Informationen bereitstellen kann, die über das Fensterhandle **(HWND)** verfügbar sind, z. B. die Steuerungsposition. Proxyanbieter kommunizieren in der Regel über die Prozessgrenze hinweg mit der Anwendung, indem sie Windows Nachrichten senden und empfangen. Weitere Informationen finden Sie unter [Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierung-Anbieters.](uiauto-clientsideprovider.md)

## <a name="ui-automation-provider-concepts"></a>Konzepte für Benutzeroberflächenautomatisierungs-Anbieter

Dieser Abschnitt bietet kurze Erläuterungen zu einer Auswahl von Schlüsselkonzepten, die Sie kennen müssen, um Benutzeroberflächenautomatisierungs-Anbieter implementieren zu können.

### <a name="elements"></a>Elemente

Benutzeroberflächenautomatisierung Elemente sind Teile der Benutzeroberfläche , in der Regel Fenster oder Steuerelemente, die für Benutzeroberflächenautomatisierung Clients sichtbar sind. Zu den entsprechenden Beispielen zählen Anwendungsfenster, Bereiche, Schaltflächen, QuickInfos, Listenfelder und Listenelemente.

Benutzeroberflächenautomatisierung Elemente werden clients als Struktur verfügbar gemacht. Benutzeroberflächenautomatisierung erstellt die Struktur, indem von einem Element zu einem anderen navigiert wird. Die Navigation wird vom Anbieter für jedes Element aktiviert. Jedes Element kann auf sein eigenes übergeordnetes Element, seine gleichgeordneten Elemente und sein erstes und letztes untergeordnetes Element verweisen.

Ein Client kann die Benutzeroberflächenautomatisierung Struktur in drei Prinzipalansichten anzeigen, wie in der folgenden Tabelle beschrieben:



| Sicht         | Beschreibung                                                    |
|--------------|----------------------------------------------------------------|
| Rohdatenansicht     | Schließt alle Elemente ein.                                         |
| Steuerelementansicht | Schließt Elemente ein, die Steuerelemente sind.                           |
| Inhaltsansicht | Enthält Steuerelementelemente, die dem Benutzer Informationen vermitteln. |



 

Für die Definition eines Elements als Inhaltselement oder Steuerelement ist die Anbieterimplementierung zuständig. Steuerelemente können auch Inhaltselemente sein, aber alle Inhaltselemente sind auch Steuerelemente.

Weitere Informationen zur Clientansicht der Struktur finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).

### <a name="frameworks"></a>Frameworks

Ein Framework ist eine Komponente, die untergeordneten Steuerelemente, Treffertests und das Rendering in einem Bereich des Bildschirms verwaltet. Beispielsweise kann ein Win32-Fenster, das häufig als **HWND** bezeichnet wird, als Framework dienen, das mehrere Benutzeroberflächenautomatisierung Elemente enthält, z. B. eine Menüleiste, eine Statusleiste und Schaltflächen.

Win32-Containersteuerelemente wie Listenfelder und Strukturansichtssteuerelemente werden als Frameworks betrachtet, da sie ihren eigenen Code zum Rendern untergeordneter Elemente und zum Ausführen von Treffertests enthalten. Im Gegensatz dazu ist ein WPF-Listenfeld kein Framework, da das Rendering und Treffertests vom enthaltenden Fenster verarbeitet werden.

Die Benutzeroberfläche in einer Anwendung kann aus verschiedenen Frameworks bestehen. Beispielsweise kann ein **HWND** in einer Anwendung dynamisches HTML (DHTML) enthalten, das wiederum eine Komponente wie ein Kombinationsfeld in einem **HWND** enthalten kann.

### <a name="fragments"></a>Fragments

Eine vollständige Teilstruktur von Elementen aus einem bestimmten Framework wird als Fragment bezeichnet. Das Element im Stammknoten der Unterstruktur wird als Fragmentstamm bezeichnet. Ein Fragmentstamm hat kein übergeordnetes Element, sondern wird in einem anderen Framework gehostet, in der Regel in einem Win32-Fenster (**HWND**).

### <a name="hosts"></a>Hosts

Der Stammknoten jedes Fragments muss in einem Element gehostet werden, in der Regel in einem Win32-Fenster (**HWND**). Die Ausnahme stellt der Desktop dar, der in keinem anderen Element gehostet wird. Der Host eines benutzerdefinierten Steuerelements ist der **HWND** des Steuerelements selbst, nicht das Anwendungsfenster oder ein anderes Fenster, das Gruppen von Steuerelementen der obersten Ebene enthalten kann.

Der Host eines Fragments spielt eine wichtige Rolle bei der Bereitstellung Benutzeroberflächenautomatisierung Dienste. Er ermöglicht die Navigation zum Fragmentstamm und stellt einige Standardeigenschaften bereit, damit diese nicht vom benutzerdefinierten Anbieter implementiert werden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren eines Client-Side Benutzeroberflächenautomatisierung-Anbieters](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementieren eines Server-Side Benutzeroberflächenautomatisierung-Anbieters](uiauto-serversideprovider.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




