---
title: Kontext-Popup
description: Ein Kontext-Popup ist das Prinzipalsteuerelement in der ContextPopup-Ansicht des Windows Menübandframeworks.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964413"
---
# <a name="context-popup"></a>Kontext-Popup

Ein Kontext-Popup ist das Prinzipalsteuerelement in der [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) des Windows Menübandframeworks. Es handelt sich um ein umfangreiches Kontextmenüsystem, das nur vom Framework als Erweiterung für eine Menübandimplementierung verfügbar gemacht wird. Das Framework macht das Kontext-Popup nicht als unabhängiges Steuerelement verfügbar.

-   [Komponenten des Kontext-Popups](#context-popup)
-   [Implementieren des Kontext-Popups](#implement-the-context-popup)
    -   [Markup](#markup)
    -   [Code](#code)
-   [Kontext-Popupeigenschaften](#context-popup-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="components-of-the-context-popup"></a>Komponenten des Kontext-Popups

Das Kontext-Popup ist ein logischer Container für das Kontextmenü und Mini-Toolbar Untersteuerelemente, die über die [**ContextMenu-**](windowsribbon-element-contextmenu.md) bzw. [**MiniToolbar-Markupelemente**](windowsribbon-element-minitoolbar.md) verfügbar gemacht werden:

-   [**ContextMenu**](windowsribbon-element-contextmenu.md) macht ein Menü mit Befehlen und Katalogen verfügbar.
-   Die [**MiniToolbar**](windowsribbon-element-minitoolbar.md) macht eine unverankerte Symbolleiste verschiedener Befehle, Kataloge und komplexer Steuerelemente verfügbar, z. B. das [Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md) und das [Kombinationsfeld](windowsribbon-controls-combobox.md).

Jedes Untersteuerelement kann höchstens einmal in einem Kontext-Popup angezeigt werden.

Der folgende Screenshot veranschaulicht das Kontext-Popup und die zugehörigen Untersteuerelemente.

![Screenshot mit Callouts, die die kontextbezogenen Ui-Komponenten des Menübands anzeigen.](images/controls/contextpopup.png)

Das Kontext-Popup ist rein konzeptionell und macht keine Benutzeroberflächenfunktionalität selbst verfügbar, z. B. Positionierung oder Größenanpassung.

> [!Note]  
> Das Kontext-Popup wird in der Regel angezeigt, indem Sie mit der rechten Maustaste (oder über die Tastenkombination UMSCHALT+F10) auf ein objekt von Interesse klicken. Die Schritte, die zum Anzeigen des Kontext-Popups erforderlich sind, werden jedoch von der Anwendung definiert.

 

## <a name="implement-the-context-popup"></a>Implementieren des Kontext-Popups

Ähnlich wie bei anderen Windows Menüband-Frameworksteuerelementen wird das Kontext-Popup über eine Markupkomponente implementiert, die die Präsentationsdetails und eine Codekomponente angibt, die ihre Funktionalität steuert.

In der folgenden Tabelle sind die Steuerelemente aufgeführt, die von den einzelnen Kontext-Popup-Untersteuerelementen unterstützt werden.



| Control                                                                  | Mini-Toolbar | Kontextmenü |
|--------------------------------------------------------------------------|--------------|--------------|
| [Schaltfläche](windowsribbon-controls-button.md)                              | x            | x            |
| [Kontrollkästchen](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Kombinationsfeld](windowsribbon-controls-combobox.md)                         | x            |              |
| [Dropdownschaltfläche](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Dropdown-Farbwähler](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Dropdownkatalog](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Hilfeschaltfläche](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Katalog im Menüband](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Schaltfläche "Teilen"](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Katalog mit geteilten Schaltflächen](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Umschaltfläche](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>Markup

Jedes Kontext-Popup-Untersteuerelement muss einzeln im Markup deklariert werden.

### <a name="mini-toolbar"></a>Mini-Toolbar

Beim Hinzufügen von Steuerelementen zu einer Kontext-Popup-Minisymbolleiste sollten die folgenden beiden Empfehlungen berücksichtigt werden:

-   Steuerelemente sollten stark erkennbar sein und offensichtliche Funktionen bereitstellen. Vertrautheit ist entscheidend, da Bezeichnungen und QuickInfos nicht für Mini-Toolbar-Steuerelemente verfügbar gemacht werden.
-   Jeder Befehl, der von einem -Steuerelement verfügbar gemacht wird, sollte an anderer Stelle auf der Menübandbenutzeroberfläche angezeigt werden. Die Mini-Toolbar unterstützt keine Tastaturnavigation.

Im folgenden Beispiel wird das grundlegende Markup für ein [**MiniToolbar-Element**](windowsribbon-element-minitoolbar.md) veranschaulicht, das drei [Button-Steuerelemente](windowsribbon-controls-button.md) enthält.

> [!Note]  
> Ein [**MenuGroup-Element**](windowsribbon-element-menugroup.md) wird für jede Zeile von Steuerelementen in der Minisymbolleiste angegeben.

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Kontextmenü

Im folgenden Beispiel wird das grundlegende Markup für ein [**ContextMenu-Element**](windowsribbon-element-contextmenu.md) veranschaulicht, das drei [Button-Steuerelemente](windowsribbon-controls-button.md) enthält.

> [!Note]  
> Jede Gruppe von Steuerelementen im [**MenuGroup-Element**](windowsribbon-element-menugroup.md) wird durch eine horizontale Leiste im Kontextmenü getrennt.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Obwohl ein Kontext-Popup höchstens eines jedes Untersteuerelements enthalten kann, sind mehrere [**ContextMenu-**](windowsribbon-element-contextmenu.md) und [**MiniToolbar-Elementdeklarationen**](windowsribbon-element-minitoolbar.md) im Menübandmarkup gültig. Dadurch kann eine Anwendung verschiedene Kombinationen von Kontextmenü- und Mini-Toolbar-Steuerelementen unterstützen, basierend auf den von der Anwendung definierten Kriterien, z. B. dem Arbeitsbereichskontext.

Weitere Informationen finden Sie im [**ContextMap-Element.**](windowsribbon-element-contextmap.md)

Im folgenden Beispiel wird das grundlegende Markup für das [**ContextPopup-Element**](windowsribbon-element-contextpopup.md) veranschaulicht.


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>Code

Um ein Kontext-Popup aufzurufen, wird die [**IUIContextualUI::ShowAtLocation-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) aufgerufen, wenn das Fenster der obersten Ebene der Menübandanwendung eine WM \_ CONTEXTMENU-Benachrichtigung empfängt.

In diesem Beispiel wird veranschaulicht, wie die WM \_ CONTEXTMENU-Benachrichtigung in der WndProc()-Methode der Menübandanwendung behandelt wird.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



Im folgenden Beispiel wird veranschaulicht, wie eine Menübandanwendung das Kontext-Popup mithilfe der [**IUIContextualUI::ShowAtLocation-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) an einer bestimmten Bildschirmposition anzeigen kann.

GetCurrentContext() hat den Wert , `cmdContextMap` wie im vorherigen Markupbeispiel definiert.

g \_ pApplication ist ein Verweis auf die [**IUIFramework-Schnittstelle.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



Der Verweis auf [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) kann freigegeben werden, bevor das Kontext-Popup verworfen wird, wie im vorherigen Beispiel gezeigt. Der Verweis muss jedoch zu einem bestimmten Zeitpunkt freigegeben werden, um Speicherverluste zu vermeiden.

> [!Caution]  
> Die Mini-Toolbar hat einen integrierten Ausblendeffekt, der auf der Nähe des Mauszeigers basiert. Aus diesem Grund wird empfohlen, die Mini-Toolbar so nah wie möglich am Mauszeiger angezeigt werden. Andernfalls wird der Mini-Toolbar aufgrund der in Konfliktstehenden Anzeigemechanismen möglicherweise nicht wie erwartet gerendert.

 

## <a name="context-popup-properties"></a>Kontext-Popupeigenschaften

Dem Kontext-Popup-Steuerelement sind keine Eigenschaftenschlüssel zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[ContextPopup-Beispiel](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 