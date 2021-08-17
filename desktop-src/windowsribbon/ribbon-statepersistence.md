---
title: Beibehalten des Menübandzustands
description: Das Windows -Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und -einstellungen über Anwendungssitzungen hinweg zu erhalten.
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

Das Windows -Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und -einstellungen über Anwendungssitzungen hinweg zu erhalten.

-   [Introduction (Einführung)](#introduction)
-   [Eine vorhersagbare Erfahrung](#a-predictable-experience)
-   [Menüband speichern Einstellungen](#save-ribbon-settings)
-   [Menüband Einstellungen](#load-ribbon-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Verschiedene Aspekte eines Menübands, einschließlich Konfigurations- und Interaktionseinstellungen, können von einem Benutzer zur Laufzeit angepasst werden, um die Benutzerfreundlichkeit und Produktivität zu verbessern. Das Menübandframework bietet die Funktionalität zum Beibehalten dieser Einstellungen über Anwendungssitzungen hinweg über zwei Methoden, die in der Implementierung der [**IUIRibbon-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) definiert sind: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) und [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Eine vorhersagbare Erfahrung

Die [](https://msdn.microsoft.com/library/cc872782.aspx) Menüband-Benutzerfreundlichkeitsrichtlinien empfehlen, dass Menübandanwendungen den Status des Menübands (abgesehen von der zuletzt ausgewählten Registerkarte) beibehalten sollten, wenn die Anwendung geschlossen wird, um eine möglichst vorhersagbare Benutzererfahrung zu bieten. Auf diese Weise können beim Starten derselben Anwendung die Einstellungen und Anpassungen aus der vorherigen Sitzung wiederhergestellt werden, und der Benutzer kann davon ausgehen, dass er weiterhin auf die gleiche Weise mit der Anwendung interagiert, wie er sie verlassen hat.

Menübandeinstellungen, die zur Laufzeit geändert und anwendungssitzungsübergreifend beibehalten werden können, werden im Kontextmenü Befehl aufgeführt. Dazu gehören:

-   Befehle, die vom Benutzer der [Symbolleisten-Befehlsliste](windowsribbon-controls-quickaccesstoolbar.md) für den Schnellzugriff hinzugefügt wurden. Wird von einem [**IUICollection-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) über den [ \_ PKEY \_ ItemsSource-Eigenschaftsschlüssel der Benutzeroberfläche](windowsribbon-reference-properties-uipkey-itemssource.md) angegeben.

    Der folgende Screenshot zeigt das Kontextmenü **Befehl zur** Symbolleiste für den Schnellzugriff hinzufügen.

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

-   Der bevorzugte [Andockzustand der Symbolleiste für](windowsribbon-controls-quickaccesstoolbar.md) den Schnellzugriff. Wird durch den [**UI \_ CONTROLDOCK-Wert**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) des [ \_ PKEY \_ QuickAccessToolbarDock-Eigenschaftsschlüssels der Benutzeroberfläche](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) angegeben.

    Dieser Screenshot zeigt die [Symbolleiste für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md) an der Standardposition der Anwendungstitelleiste und die Symbolleiste Schnellzugriff anzeigen unter dem **Menübandkontextmenü** Befehl.

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt die Symbolleiste [für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md) unterhalb des Menübands.

    ![Screenshot der Symbolleiste für den Schnellzugriff, die unter dem Menüband angedockt ist.](images/controls/qat-dockbottom.png)

-   Der Status des Menübands wurde minimiert, wie durch den booleschen Wert des [ \_ \_ PKEY-Eigenschaftsschlüssels](windowsribbon-reference-properties-uipkey-minimized.md) für die Benutzeroberfläche minimiert.

    > [!Note]  
    > Der minimierte Zustand des Menübands entspricht nicht dem reduzierten Menübandzustand. Wenn sich das Menüband im reduzierten Zustand befindet, wird es vollständig ausgeblendet und kann nicht mit ihm interagiert werden. Das Framework ruft diesen Zustand automatisch auf, wenn das Anwendungsfenster horizontal oder vertikal so groß ist, dass das Menüband den Anwendungsarbeitsbereich verdeckt. Das Framework stellt das Menüband wieder auf, wenn die Größe des Anwendungsfensters erhöht wird.

     

    Dieser Screenshot zeigt das Kontextmenü **Befehl zum Minimieren** des Menübands.

    ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt ein minimiertes Menüband.

    ![Screenshot des minimierten Microsoft Paint-Menübands.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Menüband speichern Einstellungen

Die [**IUIRibbon::SaveSettingsToStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) schreibt eine binäre Darstellung des persistenten Menübandzustands (im vorherigen Abschnitt beschrieben) in ein [IStream-Objekt.](/windows/win32/api/objidl/nn-objidl-istream) Die Anwendung speichert dann den Inhalt des IStream-Objekts in einer Datei oder Windows Registrierung.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Schreiben des Menübandzustands in ein [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) mithilfe der [**IUIRibbon::SaveSettingsToStream-Methode erforderlich**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) ist.


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



## <a name="load-ribbon-settings"></a>Menüband Einstellungen

Die [**IUIRibbon::LoadSettingsFromStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) wird verwendet, um die persistenten Menübandzustandsinformationen abzurufen, die von der [**IUIRibbon::SaveSettingsToStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) als [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) gespeichert werden. Die Informationen im IStream-Objekt werden auf die Menübandbenutzeroberfläche angewendet, wenn die Anwendung initialisiert wird.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Laden des Menübandzustands aus einem [IStream-Objekt](/windows/win32/api/objidl/nn-objidl-istream) mit der [**IUIRibbon::LoadSettingsFromStream-Methode erforderlich**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) ist.


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



Um eine optimale Leistung zu erzielen, sollte die [**IUIRibbon::LoadSettingsFromStream-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) während der Frameworkin initialisierungsphase von der [**IUIApplication::OnViewChanged-Rückruffunktion**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) aufgerufen werden, wie im folgenden Beispiel gezeigt.


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



Mehrere Instanzen derselben Menübandframeworkanwendung können jeden Menübandzustand unabhängig voneinander als separate [IStream-Objekte](/windows/win32/api/objidl/nn-objidl-istream) oder als Gruppe über ein einzelnes IStream-Objekt verwalten.

Beim Synchronisieren des Menübandzustands über eine Gruppe von Anwendungsinstanzen hinweg muss jedes Fenster der obersten Ebene auf eine [WM \_ ACTIVATE-Benachrichtigung](../inputdev/wm-activate.md) lauschen. Das deaktivierte Fenster der obersten Ebene speichert seinen Menübandzustand mithilfe der [**IUIRibbon::SaveSettingsToStream-Methode,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) und das aktivierte Fenster der obersten Ebene lädt seinen Menübandzustand mithilfe der [**IUIRibbon::LoadSettingsFromStream-Methode.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolleiste für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 