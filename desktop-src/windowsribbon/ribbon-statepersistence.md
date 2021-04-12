---
title: Beibehalten des Multifunktionsleisten Status
description: Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315764"
---
# <a name="persisting-ribbon-state"></a>Beibehalten des Multifunktionsleisten Status

Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.

-   [Introduction (Einführung)](#introduction)
-   [Vorhersagbare Darstellung](#a-predictable-experience)
-   [Menüband-Einstellungen speichern](#save-ribbon-settings)
-   [Menüband-Einstellungen laden](#load-ribbon-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Verschiedene Aspekte eines Menübands, einschließlich der Einstellungen für Konfiguration und Interaktion, können von einem Benutzer zur Laufzeit angepasst werden, um die Benutzerfreundlichkeit und Produktivität zu verbessern. Das Multifunktionsleisten-Framework stellt die Funktionalität bereit, um diese Einstellungen über mehrere Anwendungs Sitzungen hinweg durch zwei Methoden zu erhalten, die in der Implementierung der [**iuiribbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) -Schnittstelle definiert sind: [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) und [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).

## <a name="a-predictable-experience"></a>Vorhersagbare Darstellung

Mit den [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzer Leistung wird empfohlen, dass Multifunktionsleisten Anwendungen den Zustand des Menübands (abgesehen von der letzten ausgewählten Registerkarte) beibehalten, wenn die Anwendung geschlossen wird. Auf diese Weise können, wenn dieselbe Anwendung gestartet wird, die Einstellungen und Anpassungen aus der vorherigen Sitzung wieder hergestellt werden, und der Benutzer kann davon ausgehen, dass die Interaktion mit der Anwendung auf die gleiche Weise wie Sie verlassen wird.

Menü Band Einstellungen, die zur Laufzeit geändert und über Anwendungs Sitzungen hinweg beibehalten werden, werden im Kontextmenü des Befehls aufgeführt. Dazu gehören:

-   Befehle, die vom Benutzer der Symbolleisten-Befehlsliste für den [schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) hinzugefügt werden. Wird von einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [UI \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel angegeben.

    Der folgende Screenshot zeigt den Kontextmenü Befehl **Hinzufügen zum schnell Zugriff-Symbolleiste** .

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

-   Der bevorzugte Symbolleisten-Andock Zustand des [schnell Zugriffs](windowsribbon-controls-quickaccesstoolbar.md) . Wird durch den [**UI- \_ controldock**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) -Wert der [UI \_ pkey \_ quickaccesstoolbardock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) -Eigenschafts Taste angegeben.

    Dieser Screenshot zeigt die Symbolleiste für den [schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) in der Standardposition der Titelleiste der Anwendung und die **Symbolleiste für den schnell Zugriff anzeigen unter dem** Kontextmenü Befehl des Menübands.

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt die [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) unterhalb des Menübands.

    ![Screenshot der Symbolleiste für den schnell Zugriff, die unter dem Menüband angedockt ist.](images/controls/qat-dockbottom.png)

-   Der von der Multifunktionsleiste minimierte Zustand, wie durch den booleschen Wert des [ \_ \_ minimierten](windowsribbon-reference-properties-uipkey-minimized.md) Eigenschafts Schlüssels der UI pkey angegeben.

    > [!Note]  
    > Der minimierte Zustand des Menübands entspricht nicht dem Zustand "Multifunktionsleisten reduziert". Im reduzierten Zustand ist das Menüband vollständig ausgeblendet und kann nicht mit interagiert werden. Das Framework ruft diesen Zustand automatisch auf, wenn das Anwendungsfenster auf die Größe (horizontal oder vertikal) reduziert wird, bis zu dem Punkt, an dem die Multifunktionsleiste den Anwendungs Arbeitsbereich verdeckt. Das-Framework stellt das Menüband wieder her, wenn die Größe des Anwendungsfensters erweitert wird.

     

    Dieser Screenshot zeigt den Menübefehl "Menü **Band Kontext minimieren** ".

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    Dieser Screenshot zeigt eine minimierte Multifunktionsleiste.

    ![Screenshot des minimierten Microsoft Paint-Menübands.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>Menüband-Einstellungen speichern

Die [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode schreibt eine binäre Darstellung des permanenten Menüband-Zustands (im vorherigen Abschnitt beschrieben) in ein [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt. Die Anwendung speichert dann den Inhalt des IStream-Objekts in einer Datei oder in der Windows-Registrierung.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Schreiben des multifunktionsleistenzustands in ein [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt mithilfe der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode erforderlich ist.


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



## <a name="load-ribbon-settings"></a>Menüband-Einstellungen laden

Die [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode wird verwendet, um die permanenten Informationen des Ribbon-Zustands abzurufen, die von der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode als [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt gespeichert werden. Die Informationen im IStream-Objekt werden auf die Multifunktionsleisten-Benutzeroberfläche angewendet, wenn die Anwendung initialisiert wird.

Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Laden des Menüband-Zustands aus einem [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt mit der [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode erforderlich ist.


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



Um eine optimale Leistung zu erzielen, sollte die [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode während der Framework-Initialisierungsphase von der [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) -Rückruffunktion aufgerufen werden, wie im folgenden Beispiel gezeigt.


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



Mehrere Instanzen der gleichen Multifunktionsleisten-Framework-Anwendung können jeden Menüband-Zustand unabhängig als separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekte oder als Gruppe durch ein einzelnes IStream-Objekt verwalten.

Beim Synchronisieren des Menüband-Zustands über eine Gruppe von Anwendungs Instanzen hinweg muss jedes Fenster der obersten Ebene auf eine [WM- \_ Aktivierungs](../inputdev/wm-activate.md) Benachrichtigung lauschen. Das deaktivierte Fenster der obersten Ebene speichert den Multifunktionsleisten Zustand mithilfe der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode, und das Fenster der obersten Ebene, das aktiviert wird, lädt seinen Multifunktionsleisten Zustand mithilfe der [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolleiste für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 