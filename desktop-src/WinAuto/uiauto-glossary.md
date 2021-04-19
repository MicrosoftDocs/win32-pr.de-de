---
title: Glossar (Windows-Barrierefreiheits Features)
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337277"
---
# <a name="glossary-windows-accessibility-features"></a>Glossar (Windows-Barrierefreiheits Features)

## <a name="a"></a>A

<dl> <dt>

**Zugriffstaste**
</dt> <dd>

Ein unterstrichenes Zeichen im Text der Bezeichnung eines Steuer Elements.

</dd> <dt>

**Hilfe zur Barrierefreiheit**
</dt> <dd>

Wird auch als Hilfstechnologie bezeichnet. spezialisierte Programme, die mit dem Betriebssystem eines Computers arbeiten, um bestimmte Beeinträchtigungen zu erfüllen, z. b. eine begrenzte Bandbreite an Bewegung oder Blindheit. Zu den Produkten zählen größere Tastaturen, Tastatur gesteuerte Tastatur, Spracheingabe-Hilfsprogramme, Bildschirm Tastaturen und Produkte, mit denen Text in Sprache oder in eine dynamische Braille-Anzeige konvertiert werden kann. Weitere Informationen finden Sie unter [Hilfstechnologieprodukte](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**Barrierefreies Objekt**
</dt> <dd>

Alle Benutzeroberflächen Elemente, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren und über Eigenschaften verfügen, die den Namen des Objekts, die Bildschirm Positionen und andere von hilfshilfen benötigte Informationen beschreiben. Weitere Informationen finden Sie unter [barrierefreie Objekte](accessible-objects.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**untergeordnetes Element**
</dt> <dd>

Siehe [*einfaches Element*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Jedes Programm, das die Benutzeroberflächen Automatisierung oder Microsoft-Active Accessibility verwendet, um auf die Benutzeroberflächen Elemente einer Anwendung zuzugreifen, Sie zu identifizieren oder zu bearbeiten. zu den Clients gehören Barrierefreiheits Hilfen, automatisierte Testtools und einige computerbasierte Schulungs Anwendungen. Weitere Informationen finden Sie unter [Funktionsweise von Active Accessibility](how-active-accessibility-works.md).

</dd> <dt>

**Client seitiger Anbieter**
</dt> <dd>

Eine von einem Benutzeroberflächenautomatisierungs-Client implementierte Softwarekomponente zum Abrufen von Informationen über die Benutzeroberfläche einer Anwendung, die die Benutzeroberflächen Automatisierung nicht unterstützt oder nicht vollständig unterstützt. In der Regel kommunizieren Client seitige Anbieter (Proxys) über die Prozess Grenze hinweg mit der Anwendung, indem Sie Windows-Nachrichten senden und empfangen.

</dd> <dt>

**container**
</dt> <dd>

Wird auch als übergeordnetes Element bezeichnet. ein Barrierefreies Objekt, das einem oder mehreren einfachen Elementen entspricht. Beispielsweise ist ein [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für ein Listenfeld das übergeordnete Element der Listenelemente.

</dd> <dt>

**Steuerelement Muster**
</dt> <dd>

In der Benutzeroberflächen Automatisierung eine Entwurfs Implementierung, die eine diskrete Funktionalität für ein Steuerelement beschreibt. Diese Funktion kann die visuelle Darstellung eines Steuer Elements und die Aktionen enthalten, die es ausführen kann.

</dd> <dt>

**Steuerelement Pattern-Objekt**
</dt> <dd>

Eine Lauf Zeit Instanz eines COM-Objekts, das eine oder mehrere Steuerelement Muster-Schnittstellen verfügbar macht.

</dd> <dt>

**Steuerelement Muster Anbieter**
</dt> <dd>

Eine Softwarekomponente, die eine oder mehrere Steuerelement Muster-Schnittstellen implementiert.

</dd> <dt>

**Custom-Steuerelement**
</dt> <dd>

Ein Steuerelement, das von einem Benutzer oder einem Softwarehersteller von Drittanbietern erstellt wurde, oder ein System definiertes Steuerelement, das von einem Benutzer oder einem Softwarehersteller von Drittanbietern geändert wurde.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**degenerierter Textbereich (leerer Bereich)**
</dt> <dd>

Ein-Objekt, das einen leeren (NULL Zeichen) Textabschnitt darstellt. Ein degenerierter Textbereich weist angrenzende Endpunkte auf und gibt einen Punkt zwischen zwei Zeichen an.

</dd> <dt>

**nicht zusammenhängender Textbereich**
</dt> <dd>

Ein-Objekt, das mehrere Textabschnitte darstellt, die sich nicht physisch nebeneinander nebeneinander befinden.

</dd> <dt>

**Docking Container**
</dt> <dd>

Ein Steuerelement, das die Anordnung von untergeordneten Elementen (sowohl horizontal als auch vertikal) relativ zu den Begrenzungen des Docking Containers und anderen Elementen im Container ermöglicht.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Ereignislistener**
</dt> <dd>

Eine Client Anwendung, die registriert ist, um Benachrichtigungen von der Benutzeroberflächen Automatisierung oder Active Accessibility Microsoft zu erhalten, wenn bestimmte Änderungen an der Benutzeroberfläche auftreten.

</dd> <dt>

**Ereignis Benachrichtigung**
</dt> <dd>

Ein-Befehl von einem Benutzeroberflächenautomatisierungs-Anbieter an einen Client, bei dem der Anbieter den Client über ein Ereignis benachrichtigt, das sich auf den Zustand oder die Darstellung eines UI-Elements auswirken könnte.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Filtern \[\]**
</dt> <dd>

Zum Definieren der Typen von Benutzeroberflächenautomatisierungs-Elementen, die in eine Ansicht der Benutzeroberflächenautomatisierungs-Struktur eingeschlossen werden sollen. Siehe auch: unformatierte Ansicht, Steuerelement Ansicht und Inhaltsansicht.

</dd> <dt>

**Fragmentstamm**
</dt> <dd>

Das Benutzeroberflächenautomatisierungs-Element am Stamm Knoten einer Teilstruktur der Benutzeroberflächenautomatisierungs-Struktur. Ein Fragmentstamm besitzt kein übergeordnetes Element, wird aber innerhalb eines anderen Frameworks gehostet, in der Regel ein Win32-Fenster Handle (**HWND**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Ein Benutzeroberflächen Element, z. b. ein Fenster oder ein Steuerelement, das andere Elemente der Benutzeroberfläche enthält. Ein Host führt Benutzeroberflächenautomatisierungs-Dienste für die gehosteten-Elemente aus.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

Die COM-Schnittstelle, die alle Methoden und Eigenschaften für Microsoft Active Accessibility enthält.

</dd> <dt>

**Ibarrierefreie-Proxy**
</dt> <dd>

Ein Typ von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung, der standardmäßige Barrierefreiheits Informationen für Standardbenutzer Oberflächen Elemente bereitstellt: Benutzer Steuerelemente, Benutzermenüs und allgemeine Steuerelemente von COMCTL und Comctl32. Weitere Informationen finden Sie unter [IAccessible](iaccessible-proxies.md)-Proxys.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**logische Navigation**
</dt> <dd>

Einer von zwei [**zugänglichen**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Navigationsmodi, in denen ein Client die Microsoft Active Accessibility-Objekthierarchie untersucht (Next, Previous, Parent, First Child, Last Child).

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

Verpacken und Senden von Schnittstellenparametern über Prozess Grenzen hinweg.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**Native Implementierung**
</dt> <dd>

Der Typ der von Benutzeroberflächen Elementen bereitgestellten Unterstützung, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Offscreen-Modell**
</dt> <dd>

Bei diesem Modell handelt es sich um eine Datenbank von Objekten auf dem Bildschirm, die ihre Eigenschaften und deren räumliche Beziehungen enthält.

</dd> <dt>

**Oleacc**
</dt> <dd>

Die Dynamic Link Library, die die Microsoft Active Accessibility-Laufzeit bereitstellt und Anforderungen von Microsoft Active Accessibility Clients verwaltet.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

Wird auch als Container bezeichnet. ein Barrierefreies Objekt, das einem oder mehreren einfachen Elementen entspricht. Beispielsweise ist ein [**ibarrierefreie**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für ein Listenfeld das übergeordnete Element der Listenelemente.

</dd> <dt>

**Platzhalter-Automatisierungs Element**
</dt> <dd>

Ein Benutzeroberflächenautomatisierungs-Element, das ein virtualisiertes Element in der Benutzeroberflächenautomatisierungs-Struktur darstellt. In der Regel hat ein Platzhalter keine Daten für alle Benutzeroberflächenautomatisierungs-Eigenschaften geladen, und es ist erforderlich, nur das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster zu implementieren.

</dd> <dt>

**Ereignis für geänderte Eigenschaft**
</dt> <dd>

Ein Ereignis, das ausgelöst wird, wenn sich der Wert einer Eigenschaft geändert hat. Clients registrieren sich, um bestimmte von der Eigenschaft geänderte Ereignisse zu empfangen, und die Benutzeroberflächen Automatisierung benachrichtigt die registrierten Clients, wenn diese Ereignisse auftreten.

</dd> <dt>

**Anbieter Schnittstelle**
</dt> <dd>

Eine Auflistung von öffentlichen Methoden, die von einem Benutzeroberflächenautomatisierungs-Anbieter implementiert werden.

</dd> <dt>

**Proxy**
</dt> <dd>

Siehe [*IAccessible-Proxy*](uiauto-glossary.md).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**Rohdaten Ansicht**
</dt> <dd>

Die vollständige Struktur von [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekten in der Benutzeroberflächenautomatisierungs-Struktur, für die der Desktop das Stammverzeichnis ist. Die Rohdaten Ansicht folgt genau der systemeigenen programmgesteuerten Struktur einer Anwendung und ist daher die präzisere Ansicht der UI-Struktur. Sie stellt gleichzeitig die Basis zum Erstellen anderer Ansichten der Struktur dar.

</dd> <dt>

**realisierte Elemente**
</dt> <dd>

Ein Benutzeroberflächen Element, für das vollständige Informationen in den Arbeitsspeicher geladen wurden, sodass die Benutzeroberflächen Automatisierung ein Automation-Element für das Element erstellen kann.

</dd> <dt>

**Lauf Zeit Bezeichner**
</dt> <dd>

Ein Array von ganzen Zahlen, das die laufende Instanz eines Benutzeroberflächenautomatisierungs-Elements angibt. Der Bezeichner ist innerhalb der Benutzeroberfläche des Desktops eindeutig, auf dem er generiert wurde.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**sicheres Array**
</dt> <dd>

Ein selbst beschreibender Datentyp zum Deklarieren von Arrays, die beim Erstellen von COM-Komponenten verwendet werden. Zusammen mit den Daten enthält ein sicheres Array Informationen über die Anzahl und die Begrenzungen seiner Dimensionen.

</dd> <dt>

**Bereichs**
</dt> <dd>

Definieren des Umfangs der Ansicht, beginnend mit einem Basiselement.

</dd> <dt>

**server**
</dt> <dd>

Alle Steuerelemente, Module oder Anwendungen, die Microsoft Active Accessibility verwenden, um Informationen über Ihre Benutzeroberfläche verfügbar zu machen

</dd> <dt>

**Serverseitiger Anbieter**
</dt> <dd>

Eine Softwarekomponente, die Informationen zu einem Benutzeroberflächen Element verfügbar macht, das auf einem Benutzeroberflächen-Framework basiert, das systemeigene Benutzeroberflächen Automatisierung nicht unterstützt. Server seitige Anbieter (Native Anbieter) kommunizieren über die Prozess Grenze hinweg mit Client Anwendungen, indem Sie dem Benutzeroberflächenautomatisierungs-Kernsystem com-Schnittstellen bereitstellen, das Anforderungen von Clients verarbeitet.

</dd> <dt>

**einfaches Element**
</dt> <dd>

Wird auch als untergeordnetes Element bezeichnet. ein beliebiges Benutzeroberflächen Element, das ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt mit anderen Elementen gemeinsam nutzt und auf diesem **IAccessible** -Objekt basiert, um seine Eigenschaften verfügbar zu machen. Weitere Informationen finden Sie unter [einfache Elemente](simple-elements.md).

</dd> <dt>

**räumliche Navigation**
</dt> <dd>

Einer von zwei [**zugänglichen**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Navigationsmodi, in denen ein Client auf der Grundlage seiner Bildschirm Positionen von einem Benutzeroberflächen Element zu einem anderen wechselt (nach oben, unten, Links, rechts).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Textdienstframework**
</dt> <dd>

Ein skalierbares System Framework, das Dienste für natürliche Sprache und erweiterte Texteingaben auf dem Desktop und in Anwendungen ermöglicht.

</dd> <dt>

**Text Einheit**
</dt> <dd>

Eine vordefinierte Text Einheit (Zeichen, Wort, Zeile oder Absatz), die zum Navigieren durch logische Segmente eines Text Bereichs verwendet wird.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**UI-Automatisierungs Client**
</dt> <dd>

Eine hilfstechnologieanwendung, z. b. eine Bildschirm Sprachausgabe, die Benutzeroberflächen Automatisierung verwendet, um programmgesteuerten Zugriff auf die Benutzeroberflächen Elemente in einer Anwendungs Benutzeroberfläche zu erhalten. Der Client stellt Informationen über Benutzeroberflächen Elemente für den Endbenutzer dar. Automatisierte Test Skripts gelten auch als Benutzeroberflächenautomatisierungs-Clients.

</dd> <dt>

**Benutzeroberflächen Automatisierung-Kern**
</dt> <dd>

Eine Laufzeitkomponente, die das Benutzeroberflächenautomatisierungs-Framework implementiert.

</dd> <dt>

**UI-Automatisierungs Element**
</dt> <dd>

Ein Benutzeroberflächen Element, das durch ein COM-Objekt dargestellt wird, das eine Benutzeroberflächenautomatisierungs-Anbieter Schnittstelle implementiert und die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für Benutzeroberflächenautomatisierungs-Clients verfügbar macht

</dd> <dt>

**Benutzeroberflächen-Automatisierungs Framework**
</dt> <dd>

Eine integrale Windows-Komponente, die programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop unterstützt Sie ermöglicht Hilfstechnologieprodukten wie z. b. Bildschirmlesern, Endbenutzern Informationen zur Benutzeroberfläche bereitzustellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben zu bearbeiten. Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.

</dd> <dt>

**UI-Automatisierungs Knoten**
</dt> <dd>

Veraltet. Siehe Benutzeroberflächenautomatisierungs-Element.

</dd> <dt>

**Benutzeroberflächen-Automatisierungsanbieter**
</dt> <dd>

Eine Implementierung von UI-Automatisierungs Schnittstellen, die programmgesteuerte Informationen über ein UI-Element verfügbar macht. Der Anbieter stellt diese Informationen dem Benutzeroberflächenautomatisierungs-Framework als Reaktion auf Benutzeroberflächenautomatisierungs-Client Anforderungen zur Verfügung.

</dd> <dt>

**UI-Automatisierungs Struktur**
</dt> <dd>

Eine hierarchische Darstellung aller Benutzeroberflächenautomatisierungs-Elemente auf dem Windows-Desktop. Die Struktur besteht aus einem Stamm Element, das den aktuellen Desktop darstellt und dessen untergeordnete Elemente Anwendungsfenster darstellen. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Teile der Benutzeroberfläche darstellen, z. b. Menüs, Schaltflächen, Symbolleisten und Listenfelder. Diese Elemente können Elemente enthalten, wie z. b. Listenelemente.

</dd> <dt>

**UI-Framework**
</dt> <dd>

Eine Komponente, die untergeordnete Steuerelemente, Treffer Tests und das Rendering in einem Bereich des Bildschirms verwaltet.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**Bezeichner anzeigen**
</dt> <dd>

Ein Wert, der eine Ansicht angibt, die für ein Benutzeroberflächenautomatisierungs-Element verfügbar ist, das ein Steuerelement Muster implementiert. Dieser Elementtyp stellt und ist in der Lage, zwischen mehreren Darstellungen desselben Informations Satzes oder untergeordneter Steuerelemente zu wechseln.

</dd> <dt>

**virtualisiertes Element**
</dt> <dd>

Ein Benutzeroberflächen Element, das nur bei Bedarf in den Arbeitsspeicher geladen wird, in der Regel, wenn das Element auf dem Bildschirm sichtbar wird. Ein virtualisiertes Element wird durch ein Platzhalter-Automatisierungs Element in der Benutzeroberflächenautomatisierungs-Struktur dargestellt.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Fenster Ereignisse (WinEvents)**
</dt> <dd>

Der Ereignistyp, der verwendet wird, um Clients zu benachrichtigen, dass ein Barrierefreies Objekt in irgendeiner Weise geändert wurde.

</dd> <dt>

**Fenster basiertes Element**
</dt> <dd>

Ein Benutzeroberflächenautomatisierungs-Element, das ein Benutzeroberflächen Element mit einem eigenen Win32-Fenster Handle (**HWND**) darstellt.

</dd> </dl>

 

 




