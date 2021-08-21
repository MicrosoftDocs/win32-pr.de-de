---
title: Glossar (Windows Barrierefreiheitsfeatures)
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab29ee66c3aa943b4be8708cec237d9a22d0d60b4fdac21c2176206f241afc16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827314"
---
# <a name="glossary-windows-accessibility-features"></a>Glossar (Windows Barrierefreiheitsfeatures)

## <a name="a"></a>Ein

<dl> <dt>

**Zugriffsschlüssel**
</dt> <dd>

Ein unterstrichenes Zeichen im Text der Bezeichnung eines Steuerelements.

</dd> <dt>

**Barrierefreiheitshilfe**
</dt> <dd>

Wird auch als Hilfstechnologie bezeichnet. spezialisierte Programme, die mit dem Betriebssystem eines Computers arbeiten, um bestimmte Beeinträchtigungen wie eine begrenzte Bewegung oder Blindheit zu unterstützen. Zu den Produkten gehören größere Tastaturen, Tastaturen mit Anvieren mit den Augen, Spracheingabe-Hilfsprogramme, Bildschirmtastaturen und Produkte, die Text in Sprache oder ein dynamisches Braille-Display konvertieren können. Weitere Informationen finden Sie unter [Hilfstechnologieprodukte](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**Barrierefreies Objekt**
</dt> <dd>

Jedes Benutzeroberflächenelement, das die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert und über Eigenschaften verfügt, die den Namen des Objekts, die Bildschirmpositionen und andere Informationen beschreiben, die von Barrierefreiheitshilfen benötigt werden. Weitere Informationen finden Sie unter [Barrierefreie Objekte.](accessible-objects.md)

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**untergeordnetes Element**
</dt> <dd>

Siehe [*einfaches Element*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Alle Programme, die Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility, um auf die Benutzeroberflächenelemente einer Anwendung zu zugreifen, sie zu identifizieren oder zu bearbeiten; -Clients umfassen Barrierefreiheitshilfen, automatisierte Testtools und einige computerbasierte Trainingsanwendungen. Weitere Informationen finden Sie unter [Funktionsweise Active Accessibility](how-active-accessibility-works.md).

</dd> <dt>

**clientseitiger Anbieter**
</dt> <dd>

Eine Softwarekomponente, die von einem Benutzeroberflächenautomatisierung-Client implementiert wird, um Informationen über die Benutzeroberfläche einer Anwendung abzurufen, die keine oder keine vollständige Unterstützung für Benutzeroberflächenautomatisierung. In der Regel kommunizieren clientseitige Anbieter (Proxys) über die Prozessgrenze hinweg mit der Anwendung, indem sie nachrichtenbasierte Windows empfangen.

</dd> <dt>

**container**
</dt> <dd>

Wird auch als übergeordnetes Element bezeichnet. ein barrierefreies Objekt, das einem oder mehrere einfache Elemente entspricht; Beispielsweise ist ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein Listenfeld das übergeordnete Element der Listenelemente.

</dd> <dt>

**Steuerelementmuster**
</dt> <dd>

In Benutzeroberflächenautomatisierung eine Entwurfsimplementierung, die eine diskrete Funktionalität für ein Steuerelement beschreibt. Diese Funktionalität kann die visuelle Darstellung eines Steuerelements und die Aktionen umfassen, die es ausführen kann.

</dd> <dt>

**Steuerelementmusterobjekt**
</dt> <dd>

Eine Laufzeitinstanz eines COM-Objekts, das eine oder mehrere Steuerelementmusterschnittstellen verfügbar macht.

</dd> <dt>

**Steuerelementmusteranbieter**
</dt> <dd>

Eine Softwarekomponente, die eine oder mehrere Steuerelementmusterschnittstellen implementiert.

</dd> <dt>

**Benutzerdefiniertes Steuerelement**
</dt> <dd>

Ein Steuerelement, das von einem Benutzer oder Drittanbieter oder einem systemdefinierten Steuerelement, das von einem Benutzer oder Drittanbieter geändert wurde, entwickelt wurde.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Degenerierten Textbereich (leerer Bereich)**
</dt> <dd>

Ein -Objekt, das eine leere Textspanne (null Zeichen) darstellt. Ein degenerierten Textbereich verfügt über angrenzende Endpunkte und gibt einen Punkt zwischen zwei Zeichen an.

</dd> <dt>

**Disjoint text range**
</dt> <dd>

Ein Objekt, das mehrere Textspanne darstellt, die nicht physisch nebeneinander liegen.

</dd> <dt>

**Andockcontainer**
</dt> <dd>

Ein Steuerelement, das die horizontale und vertikale Anordnung von untergeordneten Elementen relativ zu den Grenzen des Andockcontainers und anderer Elemente innerhalb des Containers ermöglicht.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Ereignislistener**
</dt> <dd>

Eine Clientanwendung, die sich für den Empfang von Benachrichtigungen von Benutzeroberflächenautomatisierung oder Microsoft Active Accessibility, wenn bestimmte Ui-Änderungen auftreten.

</dd> <dt>

**Ereignisbenachrichtigung**
</dt> <dd>

Ein Aufruf eines Benutzeroberflächenautomatisierung-Anbieters an einen Client, bei dem der Anbieter den Client über ein Ereignis benachrichtigt, das sich auf den Zustand oder die Darstellung eines Benutzeroberflächenelements auswirken kann.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**\[Filterung\]**
</dt> <dd>

Um die Typen der Benutzeroberflächenautomatisierung, die in eine Ansicht der Struktur der Benutzeroberflächenautomatisierung werden sollen. Siehe auch: Rohdatenansicht, Steuerelementansicht und Inhaltsansicht.

</dd> <dt>

**Fragmentstamm**
</dt> <dd>

Das Benutzeroberflächenautomatisierung element am Stammknoten einer Teilstruktur der Benutzeroberflächenautomatisierung Struktur. Ein Fragmentstamm verfügt nicht über ein übergeordnetes Element, wird aber in einem anderen Framework gehostet, in der Regel ein Win32-Fensterhand handle (**HWND**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Ein Benutzeroberflächenelement, z. B. ein Fenster oder Steuerelement, das andere Benutzeroberflächenelemente enthält. Ein Host führt Benutzeroberflächenautomatisierung Dienste im Namen der gehosteten Elemente aus.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**Iaccessible**
</dt> <dd>

Die COM-Schnittstelle, die alle Methoden und Eigenschaften für Microsoft Active Accessibility.

</dd> <dt>

**IAccessible-Proxy**
</dt> <dd>

Eine Art von [**IAccessible-Unterstützung,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) die Standardmäßige Barrierefreiheitsinformationen für Standardelemente der Benutzeroberfläche bietet: USER-Steuerelemente, BENUTZERmenüs und allgemeine Steuerelemente aus COMCTL und COMCTL32. Weitere Informationen finden Sie unter [IAccessible Proxies](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**Logische Navigation**
</dt> <dd>

Einer von zwei IAccessible-Navigationsmodi, in denen ein Client die Microsoft Active Accessibility objekthierarchie (next, previous, parent, first child, last child) untersucht. [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

Packen und Senden von Schnittstellenparametern über Prozessgrenzen hinweg.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**Native Implementierung**
</dt> <dd>

Der Typ der Unterstützung, die von Benutzeroberflächenelementen bereitgestellt wird, die die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Off-Screen-Modell**
</dt> <dd>

Dieses Modell ist eine Datenbank mit Objekten auf dem Bildschirm und enthält ihre Eigenschaften und ihre räumlichen Beziehungen.

</dd> <dt>

**OLEACC**
</dt> <dd>

Die Dynamic Link-Bibliothek, die die Microsoft Active Accessibility zur Verfügung stellt und Anforderungen von Microsoft Active Accessibility verwaltet.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

Wird auch als Container bezeichnet. ein barrierefreies Objekt, das einem oder mehrere einfache Elemente entspricht; Beispielsweise ist ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein Listenfeld das übergeordnete Element der Listenelemente.

</dd> <dt>

**Platzhalterautomatisierungselement**
</dt> <dd>

Ein Benutzeroberflächenautomatisierung, das ein virtualisiertes Element in der strukturierten Benutzeroberflächenautomatisierung darstellt. In der Regel hat ein Platzhalter keine Daten für alle eigenschaften Benutzeroberflächenautomatisierung geladen und muss nur das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) implementieren.

</dd> <dt>

**Eigenschaftsänderungsereignis**
</dt> <dd>

Ein Ereignis, das ausgelöst wird, wenn sich der Wert einer Eigenschaft geändert hat. Clients registrieren sich, um bestimmte Durch Eigenschaften geänderte Ereignisse zu empfangen, und Benutzeroberflächenautomatisierung die registrierten Clients benachrichtigt, wenn diese Ereignisse auftreten.

</dd> <dt>

**Anbieterschnittstelle**
</dt> <dd>

Eine Auflistung von öffentlichen Methoden, die von einem Benutzeroberflächenautomatisierung implementiert werden.

</dd> <dt>

**Proxy**
</dt> <dd>

Weitere Informationen finden [*Sie unter IAccessible proxy (IAccessible-Proxy).*](uiauto-glossary.md)

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**Rohdatenansicht**
</dt> <dd>

Die vollständige Struktur der [**IUIAutomationElement-Objekte**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) in Benutzeroberflächenautomatisierung Struktur, für die der Desktop der Stamm ist. Die Unformatierungsansicht folgt eng der nativen programmgesteuerten Struktur einer Anwendung und ist daher die genaueste Ansicht der Benutzeroberflächenstruktur. Sie stellt gleichzeitig die Basis zum Erstellen anderer Ansichten der Struktur dar.

</dd> <dt>

**realisiertes Element**
</dt> <dd>

Ein Benutzeroberflächenelement, für das vollständige Informationen in den Arbeitsspeicher geladen wurden, sodass Benutzeroberflächenautomatisierung automatisierungselement für das Element erstellen können.

</dd> <dt>

**Laufzeitbezeichner**
</dt> <dd>

Ein Array von ganzen Zahlen, das die ausgeführte Instanz eines Benutzeroberflächenautomatisierung identifiziert. Der Bezeichner ist innerhalb der Benutzeroberfläche des Desktops eindeutig, auf dem er generiert wurde.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**Sicheres Array**
</dt> <dd>

Ein selbstbeschreibenden Datentyp zum Deklarieren von Arrays, die beim Erstellen von COM-Komponenten verwendet werden. Zusammen mit den Daten enthält ein sicheres Array Informationen über die Anzahl und die Grenzen seiner Dimensionen.

</dd> <dt>

**Scoping**
</dt> <dd>

Definieren des Umfangs der Ansicht, beginnend mit einem Basiselement.

</dd> <dt>

**server**
</dt> <dd>

Alle Steuerungs-, Modul- oder Anwendungen, die Microsoft Active Accessibility, um Informationen über die Benutzeroberfläche verfügbar zu machen

</dd> <dt>

**Serverseitiger Anbieter**
</dt> <dd>

Eine Softwarekomponente, die Informationen zu einem Benutzeroberflächenelement verfügbar macht, das auf einem Benutzeroberflächenframework basiert, das Benutzeroberflächenautomatisierung unterstützt. Serverseitige Anbieter (native Anbieter) kommunizieren über die Prozessgrenze hinweg mit Clientanwendungen, indem sie COM-Schnittstellen für das Benutzeroberflächenautomatisierung-Kernsystem verfügbar machen, das Anforderungen von Clients unterstützt.

</dd> <dt>

**simple-Element**
</dt> <dd>

Wird auch als untergeordnetes Element bekannt. jedes Benutzeroberflächenelement, das ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mit anderen Elementen teilt und dieses **IAccessible-Objekt** verwendet, um seine Eigenschaften verfügbar zu machen. Weitere Informationen finden Sie unter [Simple Elements](simple-elements.md).

</dd> <dt>

**Räumliche Navigation**
</dt> <dd>

Einer von zwei IAccessible-Navigationsmodi, in denen ein Client basierend auf seinen Bildschirmpositionen (nach oben, unten, links, rechts) von einem Benutzeroberflächenelement zu einem anderen wechselt. [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Textdienstframework**
</dt> <dd>

Ein skalierbares Systemframework, das Dienste in natürlicher Sprache und erweiterte Texteingaben auf dem Desktop und in Anwendungen ermöglicht.

</dd> <dt>

**Texteinheit**
</dt> <dd>

Eine vordefinierte Texteinheit (Zeichen, Wort, Zeile oder Absatz), die zum Navigieren durch logische Segmente eines Textbereichs verwendet wird.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Benutzeroberflächenautomatisierung Client**
</dt> <dd>

Eine Hilfstechnologieanwendung, z. B. eine Sprachausgabe, die Benutzeroberflächenautomatisierung, um programmgesteuerten Zugriff auf die Benutzeroberflächenelemente in einer Anwendungsbenutzeroberfläche zu erhalten. Der Client stellt dem Endbenutzer Informationen zu Benutzeroberflächenelementen zur Verfügung. Automatisierte Testskripts werden auch als Benutzeroberflächenautomatisierung betrachtet.

</dd> <dt>

**Benutzeroberflächenautomatisierung Core**
</dt> <dd>

Eine Laufzeitkomponente, die die -Benutzeroberflächenautomatisierungs-Framework.

</dd> <dt>

**Benutzeroberflächenautomatisierung-Element**
</dt> <dd>

Ein Benutzeroberflächenelement, das durch ein COM-Objekt dargestellt wird, das eine Benutzeroberflächenautomatisierung-Anbieterschnittstelle implementiert und die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für Benutzeroberflächenautomatisierung verfügbar macht.

</dd> <dt>

**Benutzeroberflächenautomatisierungs-Framework**
</dt> <dd>

Eine integrale Windows, die den programmgesteuerten Zugriff auf die meisten Benutzeroberflächenelemente auf dem Desktop unterstützt. Es ermöglicht Hilfstechnologieprodukten wie Spracheingaben, Endbenutzern Informationen über die Benutzeroberfläche zur Verfügung zu stellen und die Benutzeroberfläche mit anderen Als-Standardeingaben zu bearbeiten. Benutzeroberflächenautomatisierung ermöglicht auch die Interaktion automatisierter Testskripts mit der Benutzeroberfläche.

</dd> <dt>

**Benutzeroberflächenautomatisierung Knoten**
</dt> <dd>

Veraltet. Siehe Benutzeroberflächenautomatisierung-Element.

</dd> <dt>

**Benutzeroberflächenautomatisierung-Anbieter**
</dt> <dd>

Eine Implementierung von Benutzeroberflächenautomatisierung Schnittstellen, die programmgesteuerte Informationen zu einem Benutzeroberflächenelement verfügbar machen. Der Anbieter stellt diese Informationen als Reaktion Benutzeroberflächenautomatisierungs-Framework Clientanforderungen an Benutzeroberflächenautomatisierung an den Server.

</dd> <dt>

**Benutzeroberflächenautomatisierung Struktur**
</dt> <dd>

Eine hierarchische Darstellung aller Benutzeroberflächenautomatisierung auf dem Windows Desktop. Die -Struktur besteht aus einem Stammelement, das den aktuellen Desktop darstellt, und dessen untergeordnete Elemente die Windows. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Teile der Benutzeroberfläche darstellen, z. B. Menüs, Schaltflächen, Symbolleisten und Listenfelder. Diese Elemente können Elemente wie Listenelemente enthalten.

</dd> <dt>

**Benutzeroberflächenframework**
</dt> <dd>

Eine Komponente, die untergeordnete Steuerelemente, Treffertests und rendering in einem Bereich des Bildschirms verwaltet.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**Ansichtsbezeichner**
</dt> <dd>

Ein -Wert, der eine Ansicht identifiziert, die für ein Benutzeroberflächenautomatisierung element verfügbar ist, das ein Steuerelementmuster implementiert. Dieser Elementtyp bietet und kann zwischen mehreren Darstellungen desselben Informations- oder untergeordneten Steuerelements wechseln.

</dd> <dt>

**Virtualisiertes Element**
</dt> <dd>

Ein Benutzeroberflächenelement, das nur dann in den Arbeitsspeicher geladen wird, wenn es benötigt wird, in der Regel, wenn das Element auf dem Bildschirm sichtbar wird. Ein virtualisiertes Element wird durch ein Platzhalterautomatisierungselement in der Benutzeroberflächenautomatisierung dargestellt.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Fensterereignisse (WinEvents)**
</dt> <dd>

Der Ereignistyp, der verwendet wird, um Clients zu benachrichtigen, dass sich ein barrierefreies Objekt in irgendeiner Weise geändert hat.

</dd> <dt>

**fensterbasiertes Element**
</dt> <dd>

Ein Benutzeroberflächenautomatisierung-Element, das ein Benutzeroberflächenelement darstellt, das über ein eigenes Win32-Fensterhand handle **(HWND) verfügt.**

</dd> </dl>

 

 




