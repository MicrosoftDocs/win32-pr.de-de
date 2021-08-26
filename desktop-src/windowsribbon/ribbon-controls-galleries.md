---
title: Arbeiten mit Katalogen
description: Das Windows-Menübandframework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl sammlungsbasierter Steuerelemente hinweg.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Menüband,Kataloge
- Menüband,Kataloge
- Windows Menüband, DropDownGallery-Steuerelement
- Menüband, DropDownGallery-Steuerelement
- Windows Menüband, SplitButtonGallery-Steuerelement
- Menüband, SplitButtonGallery-Steuerelement
- DropDownGallery-Steuerelement
- SplitButtonGallery-Steuerelement
- Kataloge für Windows Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933445"
---
# <a name="working-with-galleries"></a>Arbeiten mit Katalogen

Das Windows-Menübandframework bietet Entwicklern ein stabiles und konsistentes Modell für die Verwaltung dynamischer Inhalte über eine Vielzahl sammlungsbasierter Steuerelemente hinweg. Durch Anpassen und Neukonfigurieren der Menüband-Benutzeroberfläche ermöglichen diese dynamischen Steuerelemente dem Framework, sowohl in der Hostanwendung als auch im Menüband selbst auf Benutzerinteraktion zu reagieren und die Flexibilität zur Handhabung verschiedener Laufzeitumgebungen zu bieten.

-   [Introduction (Einführung)](#introduction)
-   [Kataloge](#working-with-galleries)
    -   [Elementgalerien](#item-galleries)
    -   [Befehlsgalerien](#command-galleries)
    -   [Katalogsteuerelemente](#working-with-galleries)
-   [Implementieren eines Katalogs](#how-to-implement-a-gallery)
    -   [Die grundlegenden Komponenten](#the-basic-components)
    -   [Deklarieren der Steuerelemente im Markup](#declare-the-controls-in-markup)
    -   [Erstellen eines Befehlshandlers](#create-a-command-handler)
    -   [Binden des Befehlshandlers](#bind-the-command-handler)
    -   [Initialisieren einer Auflistung](#initialize-a-collection)
    -   [Behandeln von Sammlungsereignissen](#handle-collection-events)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Diese Fähigkeit des Menübandframework, sich dynamisch an Laufzeitbedingungen, Anwendungsanforderungen und Endbenutzereingaben anzupassen, hebt die umfassenden Benutzeroberflächenfunktionen des Frameworks hervor und bietet Entwicklern die Flexibilität, eine Vielzahl von Kundenanforderungen zu erfüllen.

Der Schwerpunkt dieses Leitfadens liegt darauf, die dynamischen Katalogsteuerelemente zu beschreiben, die vom Framework unterstützt werden, ihre Unterschiede zu erläutern, zu besprechen, wann und wo sie am besten verwendet werden können, und zu veranschaulichen, wie sie in eine Menübandanwendung integriert werden können.

## <a name="galleries"></a>Kataloge

Kataloge sind funktionstüchtige und grafisch umfangreiche Listenfeld-Steuerelemente. Die Elementsammlung eines Katalogs kann nach Kategorien organisiert, in flexiblen spalten- und zeilenbasierten Layouts angezeigt, mit Bildern und Text dargestellt werden und je nach Art des Katalogs die Livevorschau unterstützen.

Kataloge unterscheiden sich aus den folgenden Gründen funktionell von anderen dynamischen Menüband-Steuerelementen:

-   Kataloge implementieren die [**IUICollection-Schnittstelle,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) die die verschiedenen Methoden zum Bearbeiten von Katalogelementsammlungen definiert.
-   Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die direkt im Menüband auftreten, z. B. wenn ein Benutzer der Symbolleiste für den Schnellzugriff (QAT) einen Befehl hinzufügt.
-   Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt aus der Laufzeitumgebung auftreten, z. B. wenn ein Druckertreiber nur Layouts für Hochformatseiten unterstützt.
-   Kataloge können zur Laufzeit aktualisiert werden, basierend auf Aktivitäten, die indirekt in der Hostanwendung auftreten, z. B. wenn ein Benutzer ein Element in einem Dokument auswählt.

Das Menübandframework macht zwei Arten von Katalogen verfügbar: Elementgalerien und Befehlsgalerien.

### <a name="item-galleries"></a>Elementgalerien

Elementgalerien enthalten eine indexbasierte Auflistung verwandter Elemente, bei der jedes Element durch ein Bild, eine Zeichenfolge oder beides dargestellt wird. Das Steuerelement ist an einen einzelnen Befehlshandler gebunden, der auf dem Indexwert basiert, der von der [ \_ PKEY \_ SelectedItem-Eigenschaft](windowsribbon-reference-properties-uipkey-selecteditem.md) der Benutzeroberfläche identifiziert wird.

Elementgalerien unterstützen die Livevorschau. Dies bedeutet, dass ein Befehlsergebnis basierend auf Mauszeiger oder Fokus angezeigt wird, ohne den Befehl zu committen oder tatsächlich auf den Befehl zu übertragen.

> [!IMPORTANT]
> Das Framework unterstützt das Hosten von Elementgalerien im Anwendungsmenü nicht.

 

### <a name="command-galleries"></a>Befehlsgalerien

Befehlsgalerien enthalten eine Auflistung unterschiedlicher, nicht indizierter Elemente. Jedes Element wird durch ein einzelnes Steuerelement dargestellt, das über eine Befehls-ID an einen Befehlshandler gebunden ist. Wie eigenständige Steuerelemente leitet jedes Element in einem Befehlskatalog Eingabeereignisse an einen zugeordneten Befehlshandler weiter– der Befehlskatalog selbst laussiert nicht auf Ereignisse.

Befehlsgalerien unterstützen keine Livevorschau.

### <a name="gallery-controls"></a>Katalogsteuerelemente

Es gibt vier Katalogsteuerelemente im Menübandframework: [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButtonGallery,**](windowsribbon-element-splitbuttongallery.md) [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)und [**ComboBox.**](windowsribbon-element-combobox.md) Alle außer **ComboBox können** entweder als Elementkatalog oder als Befehlskatalog implementiert werden.

### <a name="dropdowngallery"></a>DropDownGallery

Eine [**DropDownGallery ist**](windowsribbon-element-dropdowngallery.md) eine Schaltfläche, die eine Dropdownliste anzeigt, die eine Sammlung von sich gegenseitig ausschließenden Elementen oder Befehlen enthält.

Der folgende Screenshot veranschaulicht das [Menüband-Dropdownkatalog-Steuerelement](windowsribbon-controls-dropdowngallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Dropdownkatalog-Steuerelements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) ist ein zusammengesetztes Steuerelement, das ein einzelnes Standardelement oder einen Befehl aus seiner Sammlung auf einer primären Schaltfläche verfügbar macht und andere Elemente oder Befehle in einer sich gegenseitig ausschließenden Dropdownliste anzeigt, die angezeigt wird, wenn auf eine sekundäre Schaltfläche geklickt wird.

Der folgende Screenshot veranschaulicht das Steuerelement Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Katalogsteuerfelds mit geteilter Schaltfläche in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

Eine [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) ist ein Katalog, der eine Sammlung verwandter Elemente oder Befehle im Menüband anzeigt. Wenn zu viele Elemente im Katalog vorhanden sind, wird ein Erweiterungspfeil bereitgestellt, um den Rest der Sammlung in einem erweiterten Bereich anzuzeigen.

Der folgende Screenshot veranschaulicht das [Menüband-In-Ribbon Gallery-Steuerelement](windowsribbon-controls-inribbongallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Katalogsteuerelementes im Menüband im Microsoft-Farbband.](images/controls/inribbongallery.png)

### <a name="combobox"></a>Kombinationsfeld

Ein [**ComboBox-Steuerelement**](windowsribbon-element-combobox.md) ist ein Einspalten-Listenfeld, das eine Sammlung von Elementen mit einem statischen Steuerelement oder einem Bearbeitungssteuerfeld und einem Dropdownpfeil enthält. Der Listenfeldteil des Steuerelements wird angezeigt, wenn der Benutzer auf den Dropdownpfeil klickt.

Der folgende Screenshot veranschaulicht ein [Menüband-Kombinationsfeld-Steuerelement](windowsribbon-controls-combobox.md) aus Windows Live Movie Maker.

![Screenshot eines Kombinationsfeld-Steuerelements im Microsoft-Farbband.](images/controls/combobox.png)

Da [**comboBox ausschließlich**](windowsribbon-element-combobox.md) ein Elementkatalog ist, werden keine Befehlselemente unterstützt. Es ist auch das einzige Katalogsteuer steuerelement, das keinen Befehlsraum unterstützt. (Ein Befehlsraum ist eine Sammlung von Befehlen, die im Markup deklariert und am unteren Rand eines Elementkatalogs oder Befehlskatalogs aufgeführt werden.)

Das folgende Codebeispiel zeigt das Markup, das zum Deklarieren eines Befehlsraums mit drei Schaltflächen in einer [**DropDownGallery erforderlich ist.**](windowsribbon-element-dropdowngallery.md)


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



Der folgende Screenshot veranschaulicht den Befehlsraum mit drei Schaltflächen des vorangehenden Codebeispiels.

![Screenshot eines Befehlsraums mit drei Schaltflächen in einer Dropdownliste.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Implementieren eines Katalogs

In diesem Abschnitt werden die Implementierungsdetails von Menüband-Katalogen erläutert und erläutert, wie sie in eine Menübandanwendung integriert werden.

### <a name="the-basic-components"></a>Die grundlegenden Komponenten

In diesem Abschnitt werden die Eigenschaften und Methoden beschrieben, die den Backbone dynamischer Inhalte im Menübandframework bilden und das Hinzufügen, Löschen, Aktualisieren und anderweitige Bearbeiten des Inhalts und visuellen Layouts von Menüband-Katalogen zur Laufzeit unterstützen.

### <a name="iuicollection"></a>IUICollection

Kataloge erfordern einen grundlegenden Satz von Methoden, um auf die einzelnen Elemente in ihren Sammlungen zu zugreifen und sie zu bearbeiten.

Die [IEnumUnknown-Schnittstelle](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) definiert diese Methoden, und das Framework ergänzt ihre Funktionalität durch zusätzliche Methoden, die in der [**IUICollection-Schnittstelle definiert**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) sind. **IUICollection** wird vom Framework für jede Katalogdeklaration im Menübandmarkup implementiert.

Wenn zusätzliche Funktionen erforderlich sind, die nicht von der [**IUICollection-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) bereitgestellt werden, kann ein benutzerdefiniertes Sammlungsobjekt, das von der Hostanwendung implementiert und von [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) abgeleitet wird, durch die Frameworksammlung ersetzt werden.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Damit eine Anwendung auf Änderungen in einer Katalogsammlung reagieren kann, muss sie die [**IUICollectionChangedEvent-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) implementieren. Anwendungen können Benachrichtigungen von einem [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) über den [**IUICollectionChangedEvent::OnChanged-Ereignislistener**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) abonnieren.

Wenn die Anwendung die vom Framework bereitgestellte Katalogsammlung durch eine benutzerdefinierte Sammlung ersetzt, sollte die Anwendung die [IConnectionPointContainer-Schnittstelle](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) implementieren. Wenn [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann die Anwendung das Framework nicht über Änderungen in der benutzerdefinierten Sammlung benachrichtigen, die dynamische Aktualisierungen des Katalogsteuerpunkts erfordern.

In Fällen, in denen [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) nicht implementiert ist, kann das Katalogsteuerfeld nur durch Ungültigkeit über [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) und [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)oder durch Aufrufen von [**IUIFramework::SetUICommandProperty aktualisiert werden.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Anwendungen müssen IUISimplePropertySet für jedes Element oder jeden Befehl in einer Katalogsammlung implementieren. Die Eigenschaften, die mit [**IUISimplePropertySet::GetValue angefordert**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) werden können, variieren jedoch.

Elemente werden über den [ \_ PKEY \_ ItemsSource-Eigenschaftsschlüssel](windowsribbon-reference-properties-uipkey-itemssource.md) der Benutzeroberfläche definiert und an einen Katalog gebunden und machen Eigenschaften mit einem [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) verfügbar.

Die gültigen Eigenschaften für Elemente in Elementgalerien ([**UI \_ COMMANDTYPE \_ COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.

> [!Note]  
> Einige Elementeigenschaften, z. [B. \_ \_ PKEY-Beschriftung der Benutzeroberfläche,](windowsribbon-reference-properties-uipkey-label.md)können im Markup definiert werden. Weitere Informationen finden Sie in der [Referenzdokumentation zu](windowsribbon-reference-properties.md) Eigenschaftsschlüsseln.

 



Control

Eigenschaften

[**ComboBox**](windowsribbon-element-combobox.md)

[Benutzeroberfläche \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Benutzeroberfläche \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Benutzeroberfläche \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Benutzeroberfläche \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[Benutzeroberfläche \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) ist eine Eigenschaft des Elementkatalogs.



 

Die gültigen Elementeigenschaften für Befehlssammlungen ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) werden in der folgenden Tabelle beschrieben.



| Control                                                                | Eigenschaften                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Benutzeroberfläche \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Benutzeroberfläche \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Benutzeroberfläche \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Kategorien werden verwendet, um Elemente und Befehle in Katalogen zu organisieren. Kategorien werden über den [Eigenschaftenschlüssel \_ PKEY \_ Categories](windowsribbon-reference-properties-uipkey-categories.md) der Benutzeroberfläche definiert und an einen Katalog gebunden und machen Eigenschaften mit einem kategoriespezifischen [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) verfügbar.

Kategorien haben keinen CommandType und unterstützen keine Benutzerinteraktion. Beispielsweise können Kategorien nicht zum SelectedItem in einem Elementkatalog werden, und sie sind nicht an einen Befehl in einem Befehlskatalog gebunden. Wie andere Katalogelementeigenschaften können Kategorieeigenschaften wie [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md) und [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) durch Aufrufen von [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)abgerufen werden.

> [!IMPORTANT]
> [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) sollte [**UI COLLECTION \_ \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) zurückgeben, wenn [ui \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) für ein Element angefordert wird, dem keine Kategorie zugeordnet ist.

 

### <a name="declare-the-controls-in-markup"></a>Deklarieren der Steuerelemente im Markup

Kataloge müssen wie alle Menübandsteuerelemente im Markup deklariert werden. Ein Katalog wird im Markup als Elementkatalog oder Befehlskatalog identifiziert, und verschiedene Präsentationsdetails werden deklariert. Im Gegensatz zu anderen Steuerelementen müssen Kataloge nur das Basissteuerelement oder den Sammlungscontainer im Markup deklariert werden. Die tatsächlichen Auflistungen werden zur Laufzeit aufgefüllt. Wenn ein Katalog im Markup deklariert wird, wird das *Type-Attribut* verwendet, um anzugeben, ob der Katalog ein Elementkatalog eines Befehlskatalogs ist.

Für jedes der hier erläuterten Steuerelemente stehen eine Reihe optionaler Layoutattribute zur Verfügung. Diese Attribute bieten Entwicklereinstellungen für das Framework, die sich direkt darauf auswirken, wie ein Steuerelement aufgefüllt und in einem Menüband angezeigt wird. Die im Markup anwendbaren Einstellungen beziehen sich auf die Anzeige- und Layoutvorlagen und -verhaltensweisen, die unter [Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)erläutert werden.

Wenn ein bestimmtes Steuerelement layouteinstellungen nicht direkt im Markup zulässt oder die Layouteinstellungen nicht angegeben sind, definiert das Framework steuerelementspezifische Anzeigekonventionen basierend auf dem verfügbaren Bildschirmspeicherplatz.

In den folgenden Beispielen wird veranschaulicht, wie Sie eine Reihe von Katalogen in ein Menüband integrieren.

### <a name="command-declarations"></a>Befehlsdeklarationen

Befehle sollten mit einem *CommandName-Attribut* deklariert werden, das zum Zuordnen eines Steuerelements oder einer Gruppe von Steuerelementen zum Befehl verwendet wird.

Ein *CommandId-Attribut,* das zum Binden eines Befehls an einen Befehlshandler beim Kompilieren des Markups verwendet wird, kann hier ebenfalls angegeben werden. Wenn keine ID angegeben wird, wird eine vom Framework generiert.


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



### <a name="control-declarations"></a>Steuerelementdeklarationen

Dieser Abschnitt enthält Beispiele, die das grundlegende Steuerelementmarkup veranschaulichen, das für die verschiedenen Katalogtypen erforderlich ist. Sie zeigen, wie sie die Katalogsteuerelemente deklarieren und einem Befehl über das *CommandName-Attribut* zuordnen.

Das folgende Beispiel zeigt eine Steuerelementdeklaration für [**dropDownGallery,**](windowsribbon-element-dropdowngallery.md) wobei das *Type-Attribut* verwendet wird, um anzugeben, dass es sich um einen Befehlskatalog handelt.


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



Das folgende Beispiel zeigt eine Steuerelementdeklaration für [**splitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)


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



Das folgende Beispiel zeigt eine Steuerelementdeklaration für [**inRibbonGallery.**](windowsribbon-element-inribbongallery.md)

> [!Note]  
> Da [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) so konzipiert ist, dass eine Teilmenge der Elementauflistung im Menüband angezeigt wird, ohne ein Dropdownmenü zu aktivieren, stellt es eine Reihe optionaler Attribute bereit, die die Größe und das Elementlayout bei der Menübandinitialisierung steuern. Diese Attribute sind für **inRibbonGallery** eindeutig und nicht in den anderen dynamischen Steuerelementen verfügbar.

 


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



Das folgende Beispiel zeigt eine Steuerelementdeklaration für das [**ComboBox -Steuerelement.**](windowsribbon-element-combobox.md)


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Erstellen eines Befehlshandlers

Für jeden Befehl benötigt das Menübandframework einen entsprechenden Befehlshandler in der Hostanwendung. Befehlshandler werden von der Menübandhostanwendung implementiert und von der [**IUICommandHandler-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) abgeleitet.

> [!Note]  
> Mehrere Befehle können an einen einzelnen Befehlshandler gebunden werden.

 

Ein Befehlshandler dient zwei Zwecken:

-   [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) antwortet auf Anforderungen zum Aktualisieren von Eigenschaften. Die Werte der Befehlseigenschaften, z. B. [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) oder [UI \_ PKEY \_ Label,](windowsribbon-reference-properties-uipkey-label.md)werden durch Aufrufe von [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) oder [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)festgelegt.
-   [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) reagiert auf Ausführungsereignisse. Diese Methode unterstützt die folgenden drei Ausführungszustände, die vom [**\_ EXECUTIONVERB-Parameter**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) der Benutzeroberfläche angegeben werden.
    -   Der Ausführungsstatus führt befehle aus, an die der Handler gebunden ist, oder führt einen Commit an diese aus.
    -   Der Vorschauzustand zeigt eine Vorschau aller Befehle an, an die der Handler gebunden ist. Dies führt im Wesentlichen die Befehle aus, ohne ein Commit für das Ergebnis auszuführen.
    -   Der CancelPreview-Zustand bricht alle Befehle in der Vorschau ab. Dies ist erforderlich, um das Durchlaufen eines Menüs oder einer Liste zu unterstützen und sequenziell eine Vorschau anzuzeigen und die Ergebnisse nach Bedarf rückgängig zu machen.

Im folgenden Beispiel wird ein Katalogbefehlshandler veranschaulicht.


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



### <a name="bind-the-command-handler"></a>Binden des Befehlshandlers

Nachdem Sie einen Befehlshandler definiert haben, muss der Befehl an den Handler gebunden werden.

Im folgenden Beispiel wird veranschaulicht, wie ein Katalogbefehl an einen bestimmten Befehlshandler gebunden wird. In diesem Fall sind sowohl die [**ComboBox-**](windowsribbon-element-combobox.md) als auch die Katalogsteuerelemente an ihre jeweiligen Befehlshandler gebunden.


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



### <a name="initialize-a-collection"></a>Initialisieren einer Auflistung

Im folgenden Beispiel wird eine benutzerdefinierte Implementierung von [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) für element- und command-Kataloge veranschaulicht.

Die CItemProperties-Klasse in diesem Beispiel wird von [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)abgeleitet. Zusätzlich zur erforderlichen [**IUISimplePropertySet::GetValue-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)implementiert die CItemProperties-Klasse eine Reihe von Hilfsfunktionen für die Initialisierung und Indexnachverfolgung.


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



### <a name="handle-collection-events"></a>Behandeln von Sammlungsereignissen

Im folgenden Beispiel wird eine IUICollectionChangedEvent-Implementierung veranschaulicht.


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

[Sammlungseigenschaften](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Erstellen einer Menübandanwendung](windowsribbon-stepbystep.md)
</dt> <dt>

[Grundlegendes zu Befehlen und Steuerelementen](windowsribbon-commandscontrols.md)
</dt> <dt>

[Richtlinien für die Menübandbenutzerfreundlichkeit](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menübandentwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Katalogbeispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

 