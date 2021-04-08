---
title: Arbeiten mit Galerien
description: Das Windows-Menü Band Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows-Menüband, Galerien
- Menüband, Galerien
- Windows-Menüband, dropdowngallery-Steuerelement
- Menüband, dropdowngallery-Steuerelement
- Windows-Menüband, splitbuttongallery-Steuerelement
- Multifunktionsleiste, splitbuttongallery-Steuerelement
- Dropdowngallery-Steuerelement
- Splitbuttongallery-Steuerelement
- Menüband für Windows-Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729232"
---
# <a name="working-with-galleries"></a>Arbeiten mit Galerien

Das Windows-Menü Band Framework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl von Sammlungs basierten Steuerelementen. Durch das anpassen und Neukonfigurieren der Multifunktionsleisten-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework die Reaktion auf Benutzerinteraktionen sowohl in der Host Anwendung als auch auf dem Menüband selbst und bieten die Flexibilität, verschiedene Laufzeitumgebungen zu verarbeiten.

-   [Introduction (Einführung)](#introduction)
-   [Buden](#working-with-galleries)
    -   [Element Kataloge](#item-galleries)
    -   [Befehls Galerien](#command-galleries)
    -   [Katalog Steuerelemente](#working-with-galleries)
-   [Vorgehensweise beim Implementieren eines Katalogs](#how-to-implement-a-gallery)
    -   [Die grundlegenden Komponenten](#the-basic-components)
    -   [Deklarieren der Steuerelemente im Markup](#declare-the-controls-in-markup)
    -   [Erstellen eines Befehls Handlers](#create-a-command-handler)
    -   [Binden des Befehls Handlers](#bind-the-command-handler)
    -   [Initialisieren einer Sammlung](#initialize-a-collection)
    -   [Behandeln von Sammlungs Ereignissen](#handle-collection-events)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Diese Fähigkeit des Multifunktionsleisten-Frameworks, sich dynamisch an Lauf Zeit Bedingungen, Anwendungsanforderungen und Endbenutzer Eingaben anzupassen, hebt die umfassenden Benutzeroberflächen Funktionen des Frameworks hervor und bietet Entwicklern die Flexibilität, eine breite Palette von Kundenanforderungen zu erfüllen.

Der Schwerpunkt dieses Handbuchs besteht darin, die dynamischen Katalog Steuerelemente zu beschreiben, die vom Framework unterstützt werden, ihre Unterschiede zu erläutern, zu erörtern, wann und wo Sie am besten verwendet werden können, und zu veranschaulichen, wie Sie in eine Menü Bandanwendung integriert werden können

## <a name="galleries"></a>Kataloge

Galerien sind funktionale und grafisch umfangreiche Listenfeld-Steuerelemente. Die Element Auflistung eines Katalogs kann nach Kategorien organisiert werden, die in flexiblen Spalten-und Zeilen basierten Layouts angezeigt werden, die mit Bildern und Text dargestellt werden. abhängig vom Typ des Katalogs wird die Live Vorschau unterstützt.

Kataloge sind aus folgenden Gründen funktionell von anderen dynamischen Menüband-Steuerelementen unterschieden:

-   Kataloge implementieren die [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle, die die verschiedenen Methoden zum Bearbeiten von Galerie Element Auflistungen definiert.
-   Kataloge können zur Laufzeit auf der Grundlage von Aktivitäten aktualisiert werden, die direkt im Menüband auftreten, z. b. Wenn ein Benutzer der Symbolleiste für den schnell Zugriff (QAT) einen Befehl hinzufügt.
-   Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt aus der Laufzeitumgebung auftreten, z. b. Wenn ein Druckertreiber nur Hochformat Layouts unterstützt.
-   Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt in der Host Anwendung auftreten, z. b. Wenn ein Benutzer ein Element in einem Dokument auswählt.

Das Menüband-Framework macht zwei Arten von Galerien verfügbar: Element Kataloge und Befehls Galerien.

### <a name="item-galleries"></a>Element Kataloge

Element Kataloge enthalten eine indexbasierte Auflistung verwandter Elemente, wobei jedes Element durch ein Bild, eine Zeichenfolge oder beides dargestellt wird. Das-Steuerelement ist an einen einzelnen Befehls Handler gebunden, der auf dem Indexwert basiert, der von der Benutzeroberflächen- [ \_ pkey \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) -Eigenschaft identifiziert wird.

Element Kataloge unterstützen die Live Vorschau. Dies bedeutet, dass ein Befehls Ergebnis basierend auf mouseover oder Fokus angezeigt wird, ohne dass ein Commit für den Befehl ausgeführt oder tatsächlich aufgerufen wird.

> [!IMPORTANT]
> Das Framework bietet keine Unterstützung für das Hosting von Element Galerien im Anwendungsmenü.

 

### <a name="command-galleries"></a>Befehls Galerien

Befehls Galerien enthalten eine Auflistung von eindeutigen, nicht indizierten Elementen. Jedes Element wird durch ein einzelnes Steuerelement dargestellt, das über eine Befehls-ID an einen Befehls Handler gebunden ist. Ebenso wie eigenständige Steuerelemente leitet jedes Element in einer Befehls Galerie Eingabeereignisse an einen zugeordneten Befehls Handler weiter – die Befehls Galerie selbst lauscht nicht auf Ereignisse.

Befehls Galerien unterstützen keine Live Vorschau.

### <a name="gallery-controls"></a>Katalog Steuerelemente

Es gibt vier Katalog Steuerelemente im Menüband-Framework: [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md)und [**ComboBox**](windowsribbon-element-combobox.md). Alle außer **ComboBox** können entweder als Element Katalog oder als Befehls Katalog implementiert werden.

### <a name="dropdowngallery"></a>Dropdown Gallery

Ein [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) ist eine Schaltfläche, die eine Dropdown Liste anzeigt, die eine Auflistung von sich gegenseitig ausschließenden Elementen oder Befehlen enthält.

Der folgende Screenshot veranschaulicht das Menüband [-Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.

![Screenshot eines Dropdown Galerie-Steuer Elements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>Splitbuttongallery

Ein [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) ist ein zusammengesetztes Steuerelement, das ein einzelnes Standardelement oder einen einzelnen Befehl aus seiner Auflistung auf einer primären Schaltfläche verfügbar macht und andere Elemente oder Befehle in einer sich gegenseitig ausschließenden Dropdown Liste anzeigt, die angezeigt wird, wenn auf eine sekundäre Schaltfläche geklickt wird.

Der folgende Screenshot veranschaulicht das Steuerelement für den [Menüband-unterteilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog in Microsoft Paint für Windows 7.

![Screenshot eines Steuer Elements für eine unterteilte Schaltflächen Galerie in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>Inribbongallery

Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Katalog ist ein Katalog, in dem eine Sammlung verwandter Elemente oder Befehle im Menüband angezeigt wird. Wenn im Katalog zu viele Elemente vorhanden sind, wird ein Erweiterungs Pfeil bereitgestellt, um den Rest der Auflistung in einem erweiterten Bereich anzuzeigen.

Der folgende Screenshot veranschaulicht das Multifunktionsleisten [-Steuerelement im Menüband-](windowsribbon-controls-inribbongallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.

![Screenshot eines in-Ribbon Gallery-Steuer Elements im Microsoft Paint-Menüband.](images/controls/inribbongallery.png)

### <a name="combobox"></a>Kombinationsfeld

Ein Kombinations [**Feld**](windowsribbon-element-combobox.md) ist ein einspaltige Listenfeld, das eine Auflistung von Elementen mit einem statischen Steuerelement oder einem Bearbeitungs Steuerelement und einem Dropdown Pfeil enthält. Der Listenfeld Bereich des Steuer Elements wird angezeigt, wenn der Benutzer auf den Dropdown Pfeil klickt.

Der folgende Screenshot veranschaulicht ein Menüband-Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement von Windows Live Movie Maker.

![Screenshot eines ComboBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/combobox.png)

Da es sich bei der [**ComboBox**](windowsribbon-element-combobox.md) ausschließlich um einen Element Katalog handelt, werden Befehls Elemente nicht unterstützt. Es ist auch das einzige Katalog Steuerelement, das keinen Befehlsbereich unterstützt. (Ein Befehlsbereich ist eine Auflistung von Befehlen, die im Markup deklariert und am unteren Rand einer Element Galerie oder Befehls Galerie aufgelistet werden.)

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren eines Befehls Raums mit drei Schaltflächen in einem [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)erforderlich ist.


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



Der folgende Screenshot veranschaulicht den drei-Schaltflächen-Befehlsbereich des vorangehenden Code Beispiels.

![Screenshot eines Befehls Raums mit drei Schaltflächen in einer dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Vorgehensweise beim Implementieren eines Katalogs

In diesem Abschnitt werden die Implementierungsdetails von Menü Band Katalogen erläutert und erläutert, wie Sie in eine Menü Bandanwendung integriert werden.

### <a name="the-basic-components"></a>Die grundlegenden Komponenten

In diesem Abschnitt werden die Eigenschaften und Methoden beschrieben, die das Backbone dynamischer Inhalte im Menüband Framework bilden und das Hinzufügen, löschen, aktualisieren und anderweitig bearbeiten des Inhalts und des visuellen Layouts von Menü Band Katalogen zur Laufzeit unterstützen.

### <a name="iuicollection"></a>Iuicollection

Kataloge benötigen einen grundlegenden Satz von Methoden, um auf die einzelnen Elemente in ihren Sammlungen zuzugreifen und Sie zu bearbeiten.

Die [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) -Schnittstelle definiert diese Methoden, und das Framework ergänzt ihre Funktionalität durch zusätzliche Methoden, die in der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle definiert sind. **Iuicollection** wird vom Framework für jede Katalog Deklaration im Menü Band Markup implementiert.

Wenn zusätzliche Funktionen erforderlich sind, die nicht von der [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Schnittstelle bereitgestellt werden, kann ein benutzerdefiniertes Auflistungs Objekt, das von der Host Anwendung implementiert und von [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) abgeleitet wurde, für die frameworkauflistung ersetzt werden.

### <a name="iuicollectionchangedevent"></a>Iuicollectionchangede Vent

Damit eine Anwendung auf Änderungen in einer Galerie Auflistung antwortet, muss Sie die [**iuicollectionchangedebug**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) -Schnittstelle implementieren. Anwendungen können Benachrichtigungen von einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [**iuicollectionchangedevent:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) -Ereignislistener abonnieren.

Wenn die Anwendung die vom Framework bereitgestellte Galerie Auflistung durch eine benutzerdefinierte Auflistung ersetzt, sollte die Anwendung die [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle implementieren. Wenn [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann die Anwendung das Framework von Änderungen in der benutzerdefinierten Sammlung, die dynamische Aktualisierungen des Katalog-Steuer Elements erfordern, nicht benachrichtigen.

In Fällen, in denen [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann das Katalog-Steuerelement nur durch die Invalidierung durch [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) und [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)oder durch Aufrufen von [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)aktualisiert werden.

### <a name="iuisimplepropertyset"></a>Iuisimplepropertyset

Anwendungen müssen iuisimplepropertyset für jedes Element oder jeden Befehl in einer Galerie Auflistung implementieren. Die Eigenschaften, die mit [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) angefordert werden können, sind jedoch unterschiedlich.

Elemente werden über den Benutzeroberflächen- [ \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel definiert und an einen Katalog gebunden, und es werden Eigenschaften mit einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt verfügbar gemacht.

Die gültigen Eigenschaften für Elemente in Element Galerien ([**UI \_ CommandType \_ Collection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.

> [!Note]  
> Einige Element Eigenschaften, z. b. die [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), können im Markup definiert werden. Weitere Details finden Sie in der Referenz Dokumentation zu [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) .

 



Control

Eigenschaften

[**ComboBox**](windowsribbon-element-combobox.md)

[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)

[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**Inribbongallery**](windowsribbon-element-inribbongallery.md)

[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)

[Benutzeroberfläche \_ Pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ itemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[Benutzeroberfläche \_ Pkey \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) ist eine Eigenschaft der Element Galerie.



 

Die gültigen Element Eigenschaften für Befehls Galerien ([**UI \_ CommandType \_ CommandCollection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.



| Control                                                                | Eigenschaften                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)       | [Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**Inribbongallery**](windowsribbon-element-inribbongallery.md)       | [Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) | [Benutzeroberfläche \_ Pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Kategorien werden verwendet, um Elemente und Befehle in Galerien zu organisieren. Kategorien werden mithilfe des Eigenschafts Schlüssels der UI- [ \_ pkey- \_ Kategorien](windowsribbon-reference-properties-uipkey-categories.md) definiert und an einen Katalog gebunden, und es werden Eigenschaften mit einem kategoriespezifischen [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt verfügbar gemacht.

Kategorien haben keinen CommandType und unterstützen keine Benutzerinteraktion. Beispielsweise können Kategorien nicht zum SelectedItem in einem Element Katalog werden, und Sie sind nicht an einen Befehl in einer Befehls Galerie gebunden. Wie andere Katalog Element Eigenschaften können auch Kategorieeigenschaften wie " [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md) " und " [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) " durch Aufrufen von " [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)" abgerufen werden.

> [!IMPORTANT]
> [**Iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) sollte den [**benutzeroberflächensammlungs- \_ \_ InvalidIndex**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) zurückgeben, wenn die [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) für ein Element angefordert wird, dem keine Kategorie zugeordnet ist.

 

### <a name="declare-the-controls-in-markup"></a>Deklarieren der Steuerelemente im Markup

Galerien müssen wie alle Menü Band Steuerelemente im Markup deklariert werden. Ein Katalog wird im Markup als Element Katalog oder Befehls Katalog identifiziert, und verschiedene Präsentations Details werden deklariert. Im Gegensatz zu anderen Steuerelementen ist es für Kataloge erforderlich, dass nur der Basis Steuerelement-oder Sammlungs Container im Markup deklariert wird. Die tatsächlichen Sammlungen werden zur Laufzeit aufgefüllt. Wenn ein Katalog im Markup deklariert wird, wird mit dem *Type* -Attribut angegeben, ob es sich bei dem Katalog um eine Element Galerie einer Befehls Galerie handelt.

Es gibt eine Reihe optionaler Layoutattribute, die für jedes der hier beschriebenen Steuerelemente verfügbar sind. Diese Attribute stellen Entwicklereinstellungen für das Framework zur Verfügung, die sich direkt darauf auswirken, wie ein Steuerelement in einem Menüband aufgefüllt und angezeigt wird. Die in Markup anwendbaren Einstellungen beziehen sich auf die Anzeige-und Layoutvorlagen und Verhaltensweisen, die unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)erläutert werden.

Wenn ein bestimmtes Steuerelement keine Layouteinstellungen direkt im Markup zulässt oder die Layouteinstellungen nicht angegeben sind, definiert das Framework Steuerelement spezifische Anzeige Konventionen basierend auf der Menge des verfügbaren Bildschirm Raums.

In den folgenden Beispielen wird veranschaulicht, wie Sie einen Satz von Galerien in eine Multifunktionsleiste integrieren.

### <a name="command-declarations"></a>Befehls Deklarationen

Befehle sollten mit einem *CommandName* -Attribut deklariert werden, das zum Zuordnen eines Steuer Elements oder einer Gruppe von Steuerelementen mit dem Befehl verwendet wird.

Ein *CommandID* -Attribut, das zum Binden eines Befehls an einen Befehls Handler verwendet wird, wenn das Markup kompiliert wird, kann auch hier angegeben werden. Wenn keine ID angegeben ist, wird eine von dem Framework generiert.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Steuerelement Deklarationen

Dieser Abschnitt enthält Beispiele, die das grundlegende Steuerelement Markup veranschaulichen, das für die verschiedenen Katalog Typen erforderlich ist. Sie zeigen, wie die Katalog Steuerelemente deklariert und mit einem Befehl über das *CommandName* -Attribut verknüpft werden.

Das folgende Beispiel zeigt eine Steuerelement Deklaration für [**dropdowngallery**](windowsribbon-element-dropdowngallery.md) , in der das *Type* -Attribut verwendet wird, um anzugeben, dass es sich um eine Befehls Galerie handelt.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



Das folgende Beispiel zeigt eine Steuerelement Deklaration für den [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



Das folgende Beispiel zeigt eine Steuerelement Deklaration für den [**inribbongallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Da der [**inribbongallery**](windowsribbon-element-inribbongallery.md) so konzipiert ist, dass er eine Teilmenge der Element Auflistung im Menüband anzeigt, ohne ein Dropdown Menü zu aktivieren, bietet er eine Reihe optionaler Attribute, die seine Größe und das Element Layout bei der Menü Band Initialisierung steuern. Diese Attribute sind für den **inribbongallery** eindeutig und nicht in den anderen dynamischen Steuerelementen verfügbar.

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



Das folgende Beispiel zeigt eine Steuerelement Deklaration für das [**ComboBox**](windowsribbon-element-combobox.md)-Steuerelement.


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Erstellen eines Befehls Handlers

Für jeden Befehl erfordert das Menüband-Framework einen entsprechenden Befehls Handler in der Host Anwendung. Befehls Handler werden von der Menüband-Host Anwendung implementiert und werden von der [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle abgeleitet.

> [!Note]  
> Mehrere Befehle können an einen einzelnen Befehls Handler gebunden werden.

 

Ein Befehls Handler dient zwei Zwecken:

-   [**Iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) antwortet auf Aktualisierungs Anforderungen für Eigenschaften. Die Werte der Befehls Eigenschaften, z. b. [ \_ \_ aktivierte UI pkey](windowsribbon-reference-properties-uipkey-enabled.md) -oder [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-label.md)-Bezeichnungen, werden durch Aufrufe von [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) oder [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)festgelegt.
-   [**Iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) antwortet auf Execute-Ereignisse. Diese Methode unterstützt die folgenden drei Ausführungs Zustände, die durch den [**UI \_ executionverb**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) -Parameter angegeben werden.
    -   Der Ausführungs Status führt alle Befehle aus, an die der Handler gebunden ist, oder führt Sie aus.
    -   Der Vorschau Zustand zeigt eine Vorschau der Befehle an, an die der Handler gebunden ist. Dadurch werden die Befehle ausgeführt, ohne dass ein Commit für das Ergebnis ausgeführt wird.
    -   Der cancelpreview-Status bricht alle in der Vorschau angezeigten Befehle ab. Dies ist erforderlich, um die Traversierung über ein Menü oder eine Liste und eine sequenzielle Vorschau zu unterstützen und die Ergebnisse nach Bedarf rückgängig zu machen

Im folgenden Beispiel wird ein Katalog Befehls Handler veranschaulicht.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Binden des Befehls Handlers

Nachdem Sie einen Befehls Handler definiert haben, muss der Befehl an den Handler gebunden werden.

Im folgenden Beispiel wird veranschaulicht, wie ein Galerie Befehl an einen bestimmten Befehls Handler gebunden wird. In diesem Fall werden die [**ComboBox**](windowsribbon-element-combobox.md) -Steuerelemente und die Gallery-Steuerelemente an die entsprechenden Befehls Handler gebunden.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Initialisieren einer Sammlung

Im folgenden Beispiel wird eine benutzerdefinierte Implementierung von [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) für Element-und Befehls Galerien veranschaulicht.

Die citemproperties-Klasse in diesem Beispiel wird von [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)abgeleitet. Zusätzlich zur erforderlichen [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)-Methode implementiert die citemproperties-Klasse einen Satz von Hilfsfunktionen für die Initialisierung und Index Verfolgung.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Behandeln von Sammlungs Ereignissen

Im folgenden Beispiel wird eine iuicollectionchangedebug-Implementierung veranschaulicht.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammlungs Eigenschaften](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Erstellen einer Menü Bandanwendung](windowsribbon-stepbystep.md)
</dt> <dt>

[Grundlegendes zu Befehlen und Steuerelementen](windowsribbon-commandscontrols.md)
</dt> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menüband-Entwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Galerie Beispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

 