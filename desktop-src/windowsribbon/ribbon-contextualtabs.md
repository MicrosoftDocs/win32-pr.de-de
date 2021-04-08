---
title: Anzeigen kontextbezogener Registerkarten
description: In einer Windows-Menü Band Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes Registerkarten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Windows-Multifunktionsleiste, Kontext Registerkarten
- Menüband, kontextbezogene Registerkarten
- Anzeigen von kontextbezogenen Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727368"
---
# <a name="displaying-contextual-tabs"></a>Anzeigen kontextbezogener Registerkarten

In einer Windows-Menü Band Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes [Register](windowsribbon-controls-tab.md) Karten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert

-   [Introduction (Einführung)](#introduction)
-   [Implementieren kontextbezogener Registerkarten](#implementing-contextual-tabs)
    -   [Markup](#markup)
    -   [Code](#code)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Im Gegensatz zu Kern Registerkarten, die verschiedene allgemeine Befehle enthalten, die unabhängig vom Arbeitsbereichs Kontext relevant sind, enthalten kontextabhängige Registerkarten in der Regel mindestens einen Befehl, der nur für ein ausgewähltes oder hervorgehobenes Objekt anwendbar ist.

Wenn ein Objekt ausgewählt oder im Arbeitsbereich Anwendung hervorgehoben wird, sind für den Typ und den Kontext des Objekts möglicherweise unterschiedliche Befehle erforderlich, die auf einer Kontext Registerkarte keine Organisations-oder funktionale Bedeutung haben. In diesen Fällen sind möglicherweise mehrere kontextabhängige Registerkarten, die in einer [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md)enthalten sind, erforderlich. Wenn Sie z. b. ein Bild auswählen, das in einer Tabellenzelle enthalten ist, sind möglicherweise zwei Kontext Registerkarten erforderlich, auf denen sowohl die Tabellen-

> [!Note]  
> Zusätzlich zu mehreren kontextbezogenen Registerkarten unterstützt das Menüband-Framework auch mehrere Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Steuerelemente in einem Menüband.

 

Beim Anzeigen kontextbezogener Registerkarten erzwingt das Menüband-Framework einen grundlegenden Satz von Verhalten, die Folgendes umfassen:

-   Kontext Registerkarten werden in der Reihenfolge positioniert, in der Sie deklariert werden, und rechts von den Haupt Registerkarten in der Zeile der Multifunktionsleiste.
-   Wenn die Größe des Menübands geändert wird, werden Registerkarten skaliert und Registerkarten Bezeichnungen abgeschnitten, wenn der Speicherplatz erforderlich ist. Sichtbare Kontext Registerkarten erhalten jedoch eine höhere Anzeige Priorität, in der Sie zuletzt skaliert und abgeschnitten werden.
-   Die Bezeichnung für eine [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) wird in der Titelleiste der Anwendung angezeigt und umfasst alle zugeordneten Kontext Registerkarten.
-   Wenn mehrere [Register](windowsribbon-controls-tabgroup.md) Karten-Gruppen Steuerelemente gleichzeitig angezeigt werden, wird eine von fünf eindeutigen Farben dem Hintergrund der einzelnen Registerkarten Gruppen in der Titelleiste der Anwendung zugewiesen. Diese Farbe wird auch als Hervorhebungs Farbe für die Kontext Registerkarten in der Registerkarten Gruppe verwendet.
-   Die Farb Zuweisung der [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) basiert auf der Reihenfolge, in der die Registerkarten Gruppenelemente im Markup deklariert werden. Die Farben werden durch das Framework definiert und können nicht von der Anwendung angegeben werden.
-   Die vom Framework definierten Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Farben können indirekt über die Eigenschaften Schlüssel der [Frameworkeigenschaften](windowsribbon-reference-properties-framework.md) geändert werden. Weitere Informationen finden Sie unter [Anpassen von Menüband-Farben](ribbon-color.md).
-   Wenn zu einem beliebigen Zeitpunkt mehr als fünf Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Steuerelemente angezeigt werden, werden die zugeordneten Farben von dem Framework in den einzelnen Zyklen
-   Die maximale Anzahl von [Register](windowsribbon-controls-tab.md) Karten-Steuerelementen in einem Menüband ist auf 100 beschränkt. Dies schließt kontextabhängige Registerkarten ein, die sichtbar sind oder nicht.

Der folgende Screenshot zeigt eine Kontext Registerkarte aus Windows 7 Paint.

![Screenshot, der ein Kontext abhängiges Registerkarten-Steuerelement anzeigt.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Implementieren kontextbezogener Registerkarten

In diesem Abschnitt werden die Implementierungsdetails der Kontext Registerkarten des Menübands erläutert und erläutert, wie Sie in eine Menü Bandanwendung integriert werden.

### <a name="markup"></a>Markup

In den folgenden Beispielen wird das grundlegende Markup für ein [**TabGroup**](windowsribbon-element-tabgroup.md) -Element veranschaulicht, das zwei kontextabhängige Registerkarten enthält.

In diesem Code Abschnitt werden die Befehls Deklarationen [**TabGroup**](windowsribbon-element-tabgroup.md) und [Tab](windowsribbon-controls-tab.md) angezeigt.


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



In diesem Code Abschnitt werden die Steuerelement Deklarationen veranschaulicht, die erforderlich sind, um zwei Kontext Registerkarten innerhalb einer [**TabGroup**](windowsribbon-element-tabgroup.md)anzuzeigen.


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a>Code

[Benutzeroberfläche \_ Pkey \_ contextavailable](windowsribbon-reference-properties-uipkey-contextavailable.md) ist der einzige Eigenschafts Schlüssel, der durch das Framework definiert wird, um die Sichtbarkeit und den Zustand von kontextbezogenen Registerkarten anzugeben. Wenn ein Objekt im Anwendungs Arbeitsbereich ausgewählt wird, kann dieser Eigenschaft einer von drei Werten aus der [**UI \_ contextavailability**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) -Enumeration zugewiesen werden, die festlegt, ob eine kontextabhängige Registerkarte vorhanden ist, und wenn dies der Fall ist, ob Sie als aktive Registerkarte angezeigt wird.

Eine Anwendung fordert ein Update der [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) an, indem Sie die [UI \_ pkey \_ contextavailable](windowsribbon-reference-properties-uipkey-contextavailable.md) -Eigenschaft für ungültig erklärt und aktualisiert, wenn der Arbeitsbereichs Kontext geändert wird.

In den folgenden Code Abschnitten wird veranschaulicht, wie eine Kontext Registerkarte angezeigt wird, wenn ein Bild in einem Anwendungs Arbeitsbereich ausgewählt wird.


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menüband-Entwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 