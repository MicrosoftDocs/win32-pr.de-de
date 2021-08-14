---
title: Beibehalten des Menübandzustands
description: Das Windows-Frameworks (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und -einstellungen anwendungssitzungenübergreifend beizubehalten.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e506d1cc8138f569dc21b491cc11ed58411131c0dd80532c19043c5974995e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707941"
---
# <a name="persisting-ribbon-state"></a>Beibehalten des Menübandzustands

Das Windows-Frameworks (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und -einstellungen anwendungssitzungenübergreifend beizubehalten.

-   [Introduction (Einführung)](#introduction)
-   [Eine vorhersagbare Benutzeroberfläche](#a-predictable-experience)
-   [Menüband Einstellungen speichern](#save-ribbon-settings)
-   [Einstellungen des Menübands laden](#load-ribbon-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Verschiedene Aspekte eines Menübands, einschließlich Konfigurations- und Interaktionseinstellungen, können von einem Benutzer zur Laufzeit angepasst werden, um die Benutzerfreundlichkeit und Produktivität zu verbessern. Das Menübandframework bietet die Funktionalität, diese Einstellungen über Anwendungssitzungen hinweg durch zwei Methoden beizubehalten, die in der Implementierung der [**IUIRibbon-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) definiert sind: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) und [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Eine vorhersagbare Benutzeroberfläche

In den Richtlinien für die [Menübandbenutzerfreundlichkeit](https://msdn.microsoft.com/library/cc872782.aspx) wird empfohlen, dass Menübandanwendungen den Status des Menübands (abgesehen von der letzten ausgewählten Registerkarte) beibehalten sollten, wenn die Anwendung geschlossen wird, um eine möglichst vorhersagbare Benutzeroberfläche bereitzustellen. Auf diese Weise können beim Starten derselben Anwendung die Einstellungen und Anpassungen aus der vorherigen Sitzung wiederhergestellt werden, und der Benutzer kann davon ausgehen, dass die Interaktion mit der Anwendung auf die gleiche Weise fortgesetzt wird, wie sie sie verlassen hat.

Menübandeinstellungen, die zur Laufzeit geändert und anwendungsübergreifend beibehalten werden können, sind im Kontextmenü Befehl aufgeführt. Dazu gehören:

-   Befehle, die der Befehlsliste der Symbolleiste für den [Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md) durch den Benutzer hinzugefügt wurden. Wird durch ein [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) über den [ \_ PKEY \_ ItemsSource-Eigenschaftenschlüssel](windowsribbon-reference-properties-uipkey-itemssource.md) der Benutzeroberfläche angegeben.

    Der folgende Screenshot zeigt das Kontextmenü Befehl zum Hinzufügen zur Symbolleiste für **den Schnellzugriff.**

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

-   Der bevorzugte Andockstatus [der Symbolleiste für den Schnellzugriff.](windowsribbon-controls-quickaccesstoolbar.md) Angegeben durch den [**UI \_ CONTROLDOCK-Wert**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) des [ \_ UI-PKEY \_ QuickAccessToolbarDock-Eigenschaftsschlüssels.](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md)

    Dieser Screenshot zeigt die [Symbolleiste für](windowsribbon-controls-quickaccesstoolbar.md) den Schnellzugriff in der Standardposition der Anwendungstitelleiste und die **Symbolleiste Schnellzugriff anzeigen unterhalb des Menübandkontextmenüs** Befehl.

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt die [Symbolleiste für](windowsribbon-controls-quickaccesstoolbar.md) den Schnellzugriff unterhalb des Menübands.

    ![Screenshot der Symbolleiste für den Schnellzugriff, die unter dem Menüband angedockt ist.](images/controls/qat-dockbottom.png)

-   Der minimierte Status des Menübands, wie durch den booleschen Wert des [ \_ \_ PKEY-Eigenschaftenschlüssels](windowsribbon-reference-properties-uipkey-minimized.md) der Benutzeroberfläche minimiert angegeben.

    > [!Note]  
    > Der minimierte Status des Menübands entspricht nicht dem reduzierten Zustand des Menübands. Wenn sich das Menüband im reduzierten Zustand befindet, wird es vollständig ausgeblendet und kann nicht interagiert werden. Das Framework ruft diesen Zustand automatisch auf, wenn das Anwendungsfenster horizontal oder vertikal verkleinert wird, bis das Menüband den Anwendungsarbeitsbereich verdeckt. Das Framework stellt das Menüband wieder her, wenn die Größe des Anwendungsfensters erhöht wird.

     

    Dieser Screenshot zeigt das Kontextmenü **Menüband minimieren** Befehl.

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt ein minimiertes Menüband.

    ![Screenshot des minimierten Microsoft Paint-Menübands.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Menüband Einstellungen speichern

Die [**IUIRibbon::SaveSettingsToStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) schreibt eine binäre Darstellung des persistenten Menübandzustands (im vorherigen Abschnitt beschrieben) in ein [IStream-Objekt.](/windows/win32/api/objidl/nn-objidl-istream) Die Anwendung speichert dann den Inhalt des IStream-Objekts in einer Datei oder der Windows Registrierung.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der erforderlich ist, um den Menübandzustand mithilfe der [**IUIRibbon::SaveSettingsToStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) in ein [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) zu schreiben.


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a>Einstellungen des Menübands laden

Die [**IUIRibbon::LoadSettingsFromStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) wird verwendet, um die permanenten Menübandzustandsinformationen abzurufen, die von der [**IUIRibbon::SaveSettingsToStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) als [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) gespeichert werden. Die Informationen im IStream-Objekt werden auf die Menüband-Benutzeroberfläche angewendet, wenn die Anwendung initialisiert wird.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Laden des Menübandzustands aus einem [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) mit der [**IUIRibbon::LoadSettingsFromStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) erforderlich ist.


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



Um eine optimale Leistung zu erzielen, sollte die [**IUIRibbon::LoadSettingsFromStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) während der Frameworkinitialisierungsphase von der [**IUIApplication::OnViewChanged-Rückruffunktion**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) aufgerufen werden, wie im folgenden Beispiel gezeigt.


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



Mehrere Instanzen der gleichen Menübandframeworkanwendung können jeden Menübandzustand unabhängig voneinander als separate [IStream-Objekte](/windows/win32/api/objidl/nn-objidl-istream) oder als Gruppe über ein einzelnes IStream-Objekt verwalten.

Beim Synchronisieren des Menübandzustands für eine Gruppe von Anwendungsinstanzen muss jedes Fenster der obersten Ebene auf eine [WM \_ ACTIVATE-Benachrichtigung](../inputdev/wm-activate.md) lauschen. Das Fenster der obersten Ebene, das deaktiviert wird, speichert seinen Menübandzustand mithilfe der [**IUIRibbon::SaveSettingsToStream-Methode,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) und das fenster der obersten Ebene, das aktiviert wird, lädt seinen Menübandzustand mithilfe der [**IUIRibbon::LoadSettingsFromStream-Methode.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolleiste für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 