---
title: Kontext-Popup
description: Ein Kontext-Popup ist das Prinzipal Steuerelement in der contextpopup-Ansicht des Windows-Menüband-Frameworks.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339283"
---
# <a name="context-popup"></a>Kontext-Popup

Ein Kontext-Popup ist das Prinzipal Steuerelement in der [**contextpopup-Ansicht**](windowsribbon-element-contextpopup.md) des Windows-Menüband-Frameworks. Es handelt sich um ein umfangreiches Kontextmenü System, das nur vom Framework als Erweiterung einer Multifunktionsleisten-Implementierung verfügbar gemacht wird – das Framework macht das Kontext-Popup nicht als unabhängiges Steuerelement verfügbar.

-   [Komponenten des Kontext-Popups](#context-popup)
-   [Implementieren des Kontext-Popups](#implement-the-context-popup)
    -   [Markup](#markup)
    -   [Code](#code)
-   [Kontext-Popup Eigenschaften](#context-popup-properties)
-   [Zugehörige Themen](#related-topics)

## <a name="components-of-the-context-popup"></a>Komponenten des Kontext-Popups

Das Kontext-Popup ist ein logischer Container für das Kontextmenü und Mini-Toolbar unter Steuerelemente, die über das [**ContextMenu**](windowsribbon-element-contextmenu.md) -bzw. das [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Markup Element verfügbar gemacht werden:

-   Das [**ContextMenu-Objekt**](windowsribbon-element-contextmenu.md) stellt ein Menü mit Befehlen und Galerien bereit.
-   Die [**MiniToolbar**](windowsribbon-element-minitoolbar.md) macht eine unverankerte Symbolleiste verschiedener Befehle, Galerien und komplexer Steuerelemente verfügbar, wie z. b. das [Schriftart-Steuer](windowsribbon-controls-fontcontrol.md) Element und das Kombinations [Feld](windowsribbon-controls-combobox.md).

Jede unter Kontrolle kann höchstens einmal in einem Kontext-Popup vorkommen.

Der folgende Screenshot veranschaulicht das Kontext-Popup und seine zugehörigen untergeordneten Steuerelemente.

![Screenshot mit Legenden, die die Kontextmenü-Komponenten der Multifunktionsleiste anzeigen.](images/controls/contextpopup.png)

Das Kontext-Popup ist rein konzeptionell und macht keine Benutzeroberflächen Funktionen selbst verfügbar, wie z. b. Positionierung oder Größenanpassung.

> [!Note]  
> Das Kontext-Popup Fenster wird in der Regel angezeigt, wenn Sie mit der rechten Maustaste auf die Maus (oder über die Tastenkombination UMSCHALT + F10) für ein interessantes Objekt klicken. Die Schritte, die zum Anzeigen des Kontext-Popup erforderlich sind, werden jedoch von der Anwendung definiert.

 

## <a name="implement-the-context-popup"></a>Implementieren des Kontext-Popups

Ähnlich wie andere Steuerelemente des Windows-Menüband-Frameworks wird das Kontext-Popup über eine Markup Komponente implementiert, die die Darstellungs Details und eine Code Komponente angibt, die ihre Funktionalität regelt.

In der folgenden Tabelle sind die Steuerelemente aufgelistet, die von den einzelnen Kontext-Popup unter Steuerelementen unterstützt werden.



| Control                                                                  | Mini-Toolbar | Kontextmenü |
|--------------------------------------------------------------------------|--------------|--------------|
| [Schaltfläche](windowsribbon-controls-button.md)                              | x            | x            |
| [Kontrollkästchen](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Kombinations Feld](windowsribbon-controls-combobox.md)                         | x            |              |
| [Dropdown Schaltfläche](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Dropdown-Katalog](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Hilfe Schaltfläche](windowsribbon-controls-helpbutton.md)                     |              |              |
| [In-Ribbon-Katalog](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Split Button-Katalog](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>Markup

Jedes Kontext-Popup-unter Steuerelement muss einzeln im Markup deklariert werden.

### <a name="mini-toolbar"></a>Mini-Toolbar

Beim Hinzufügen von Steuerelementen zu einem Kontext-Popup Mini Symbol Toolbar sollten die folgenden beiden Empfehlungen berücksichtigt werden:

-   Steuerelemente sollten stark erkennbar sein und offensichtliche Funktionen bereitstellen. Vertrautheit ist Schlüssel, da Bezeichnungen und Quick Infos nicht für Mini-Toolbar Steuerelemente verfügbar gemacht werden.
-   Jeder von einem Steuerelement bereitgestellte Befehl sollte an anderer Stelle in der Menüband-Benutzeroberfläche angezeigt werden. Der Mini-Toolbar unterstützt keine Tastaturnavigation.

Im folgenden Beispiel wird das grundlegende Markup für ein [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element veranschaulicht, das drei [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelemente enthält.

> [!Note]  
> Ein [**MenuGroup**](windowsribbon-element-menugroup.md) -Element wird für jede Zeile von Steuerelementen in der Mini Symbolleiste angegeben.

 


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

Im folgenden Beispiel wird das grundlegende Markup für ein [**ContextMenu**](windowsribbon-element-contextmenu.md) -Element veranschaulicht, das drei [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelemente enthält.

> [!Note]  
> Jede Gruppe von Steuerelementen im [**MenuGroup**](windowsribbon-element-menugroup.md) -Element wird durch einen horizontalen Balken im Kontextmenü getrennt.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Obwohl ein Kontext-Popup höchstens eine der untergeordneten Steuerelemente enthalten kann, sind mehrere [**ContextMenu**](windowsribbon-element-contextmenu.md) -und [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element Deklarationen im Menüband-Markup gültig. Dadurch kann eine Anwendung verschiedene Kombinationen von Kontextmenü und Mini-Toolbar Steuerelementen basierend auf den von der Anwendung definierten Kriterien (z. b. Arbeitsbereichs Kontext) unterstützen.

Weitere Informationen finden Sie unter dem [**contextmap**](windowsribbon-element-contextmap.md) -Element.

Im folgenden Beispiel wird das grundlegende Markup für das [**contextpopup**](windowsribbon-element-contextpopup.md) -Element veranschaulicht.


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

Zum Aufrufen eines Kontext-Popups wird die [**iuicontextualui:: showatlocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) -Methode aufgerufen, wenn das Fenster der Multifunktionsleiste auf oberster Ebene eine WM- \_ ContextMenu-Benachrichtigung empfängt.

In diesem Beispiel wird veranschaulicht, wie die WM- \_ ContextMenu-Benachrichtigung in der WndProc ()-Methode der Multifunktionsleistenanwendung behandelt wird.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



Im folgenden Beispiel wird veranschaulicht, wie eine Multifunktionsleistenanwendung das Kontext-Popup an einer bestimmten Bildschirmposition mithilfe der Methode [**iuicontextualui:: showatlocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) anzeigen kann.

GetCurrentContext () hat den Wert, `cmdContextMap` wie im vorangehenden Markup Beispiel definiert.

g \_ papplication ist ein Verweis auf die [**iuiframework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) -Schnittstelle.


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



Der Verweis auf [**iuicontextualui**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) kann freigegeben werden, bevor das Kontext-Popup verworfen wird, wie im vorherigen Beispiel gezeigt. Allerdings muss der Verweis zu einem bestimmten Zeitpunkt freigegeben werden, um Speicher Verluste zu vermeiden.

> [!Caution]  
> Der Mini-Toolbar verfügt über einen integrierten Ausblend Effekt, der auf der Nähe des Mauszeigers basiert. Aus diesem Grund empfiehlt es sich, die Mini-Toolbar so nah wie möglich mit dem Mauszeiger anzuzeigen. Andernfalls werden die Mini-Toolbar aufgrund der in Konflikt stehenden Anzeige Mechanismen möglicherweise nicht wie erwartet angezeigt.

 

## <a name="context-popup-properties"></a>Kontext-Popup Eigenschaften

Dem Kontext-Popup Steuerelement sind keine Eigenschaften Schlüssel zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[Contextpopup-Beispiel](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 