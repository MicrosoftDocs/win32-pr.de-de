---
title: Migrieren zum Windows Menübandframework
description: Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogen basiert, kann zur vielfältigen, dynamischen und kontextgesteuerten Benutzeroberfläche des Windows-Menübandframework-Befehlssystems migriert werden.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows Menüband, Migrieren zu
- Menüband, Migrieren zu
- Migrieren zum Windows Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841120"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>Migrieren zum Windows Menübandframework

Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogen basiert, kann zur vielfältigen, dynamischen und kontextgesteuerten Benutzeroberfläche des Windows-Menübandframework-Befehlssystems migriert werden. Dies ist eine einfache und effektive Möglichkeit, die Anwendung zu modernisieren und zu verbessern und gleichzeitig die Barrierefreiheit, Benutzerfreundlichkeit und Aufserfbarkeit ihrer Funktionalität zu verbessern.

## <a name="introduction"></a>Einführung

Im Allgemeinen umfasst die Migration einer vorhandenen Anwendung zum Menübandframework Folgendes:

-   Entwerfen eines Menübandlayouts und einer Steuerelementorganisation, die die Funktionalität der vorhandenen Anwendung verfügbar macht und flexibel genug ist, um neue Funktionen zu unterstützen.
-   Anpassen des Codes der vorhandenen Anwendung.
-   Migrieren vorhandener Anwendungsressourcen (Zeichenfolgen und Bilder) zum Menübandframework.

> [!Note]  
> Die [Richtlinien für die Menübandbenutzeroberfläche](https://msdn.microsoft.com/library/cc872782.aspx) sollten überprüft werden, um zu ermitteln, ob die Anwendung ein geeigneter Kandidat für eine Menüband-Benutzeroberfläche ist.

 

## <a name="design-the-ribbon-layout"></a>Entwerfen des Menübandlayouts

Potenzielle Designs der Menübandbenutzeroberfläche und Steuerelementlayouts können durch Ausführen der folgenden Schritte identifiziert werden:

1.  Inventarisierung aller vorhandenen Funktionen.
2.  Übersetzen dieser Funktionalität in Menübandbefehle.
3.  Organisieren der Befehle in logische Gruppen.

### <a name="take-inventory"></a>Inventarisierung

Im Menübandframework wird die Funktionalität, die von einer Anwendung verfügbar gemacht wird, die den Zustand oder die Ansicht eines Arbeitsbereichs oder Dokuments bearbeitet, als Befehl betrachtet. Was einen Befehl bildet, kann variieren und hängt von der Art und Domäne der vorhandenen Anwendung ab.

In der folgenden Tabelle sind einige grundlegende Befehle für eine hypothetische Textbearbeitungsanwendung aufgeführt:



| Symbol           | id     | BESCHREIBUNG               |
|------------------|--------|---------------------------|
| \_ID-DATEI \_ NEU    | 0xE100 | Neues Dokument              |
| \_ID-DATEI \_ SPEICHERN   | 0xE103 | Dokument speichern             |
| ID \_ FILE \_ SAVEAS | 0xE104 | Speichern unter... (Dialogfeld)       |
| \_ID-DATEI \_ GEÖFFNET   | 0xE101 | Öffnen... (Dialogfeld)          |
| ID \_ FILE \_ EXIT   | 0xE102 | Beenden der Anwendung      |
| ID \_ BEARBEITEN \_ UNDO   | 0xE12B | Rückgängig                      |
| ID \_ EDIT \_ CUT    | 0xE123 | Ausgewählten Text ausschneiden         |
| ID \_ BEARBEITEN \_ KOPIEREN   | 0xE122 | Kopieren des ausgewählten Texts        |
| ID \_ BEARBEITEN \_ EINFÜGEN  | 0xE125 | Einfügen von Text aus der Zwischenablage |
| ID \_ BEARBEITEN \_ LÖSCHEN  | 0xE120 | Löschen des ausgewählten Texts      |
| ID \_ VIEW \_ ZOOM   | 1242   | Zoom... (Dialogfeld)          |



 

Sehen Sie sich beim Erstellen eines Inventars von Befehlen über vorhandene Menüs und Symbolleisten hinaus. Berücksichtigen Sie alle Möglichkeiten, wie ein Benutzer mit dem Arbeitsbereich interagieren kann. Auch wenn nicht jeder Befehl für die Aufnahme in das Menüband geeignet ist, kann diese Übung sehr gut Befehle verfügbar machen, die zuvor von Ebenen der Benutzeroberfläche verdeckt wurden.

### <a name="translate"></a>Translate

Nicht jeder Befehl muss auf der Menüband-Benutzeroberfläche dargestellt werden. Wenn Sie beispielsweise Text eingeben, eine Auswahl ändern, scrollen oder die Einfügemarke mit der Maus verschieben, gelten alle als Befehle im hypothetischen Text-Editor. Diese sind jedoch nicht geeignet, um sie in einer Befehlsleiste verfügbar zu machen, da jede eine direkte Interaktion mit der Benutzeroberfläche der Anwendung umfasst.

Im Gegensatz dazu können einige Funktionen nicht als Befehl im herkömmlichen Sinn gedacht werden. Anstatt z. B. in einem Dialogfeld zu sein, können Seitenrandanpassungen für Drucker im Menüband als Gruppe von Spinner-Steuerelementen in einer kontextbezogenen Registerkarte oder im Anwendungsmodus [dargestellt werden.](ribbon-applicationmodes.md)

> [!Note]  
> Notieren Sie sich die numerische ID, die jedem Befehl zugewiesen werden kann. Einige Benutzeroberflächenframeworks, z. B. Microsoft Foundation Classes (MFC), definieren IDs für Befehle wie das Datei- und Bearbeitungsmenü (0xE100 0xE200).

 

### <a name="organize"></a>Organisieren

Bevor Sie versuchen, die Befehlsinventur zu organisieren, sollten Sie die [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Menübandbenutzeroberfläche auf bewährte Methoden beim Implementieren einer Menüband-Benutzeroberfläche überprüfen.

Im Allgemeinen können die folgenden Regeln auf die Menübandbefehlsorganisation angewendet werden:

-   Befehle, die für die Datei oder die gesamte Anwendung ausgeführt werden, gehören höchstwahrscheinlich zum [Anwendungsmenü](windowsribbon-controls-applicationmenu.md).
-   Häufig verwendete Befehle wie Ausschneiden, Kopieren und Einfügen (wie im Text-Editor-Beispiel) werden in der Regel auf einer Standardregisterkarte für die Startseite platziert. In komplexeren Anwendungen können sie an anderer Stelle auf der Menüband-Benutzeroberfläche dupliziert werden.
-   Wichtige oder häufig verwendete Befehle rechtfertigen möglicherweise die Standardmäßige Aufnahme in die [Symbolleiste für den Schnellzugriff.](windowsribbon-controls-quickaccesstoolbar.md)

Das Menübandframework bietet auch ContextMenu- und MiniToolbar-Steuerelemente über die ContextPopup-Ansicht. Diese Features sind nicht obligatorisch, aber wenn Ihre Anwendung über ein oder mehrere vorhandene Kontextmenüs verfügt, kann die Migration der befehle, die sie enthalten, die Wiederverwendung der vorhandenen Codebasis mit automatischer Bindung an vorhandene Ressourcen ermöglichen.

Da jede Anwendung anders ist, lesen Sie die Richtlinien, und versuchen Sie, sie so weit wie möglich anzuwenden. Eines der Ziele des Menübandframework ist es, eine vertraute, konsistente Benutzeroberfläche zu bieten, und dieses Ziel ist besser erreichbar, wenn Entwürfe für neue Anwendungen vorhandene Menübandanwendungen so weit wie möglich spiegeln.

## <a name="adapt-your-code"></a>Anpassen des Codes

Nachdem die Menübandbefehle identifiziert und in logische Gruppierungen organisiert wurden, hängt die Anzahl der Schritte, die beim Integrieren des Menübandframework in vorhandenen Anwendungscode erforderlich sind, von der Komplexität der ursprünglichen Anwendung ab. Im Allgemeinen gibt es drei grundlegende Schritte:

-   Erstellen Sie das Menübandmarkup basierend auf der Befehlsorganisations- und Layoutspezifikation.
-   Ersetzen Sie legacy-Menü- und Symbolleistenfunktionen durch Menübandfunktionen.
-   Implementieren Sie einen IUICommandHandler-Adapter.

### <a name="create-the-markup"></a>Erstellen des Markups

Die Liste der Befehle sowie ihre Organisation und ihr Layout werden über die Menüband-Markupdatei deklariert, die vom [Menüband-Markupcompiler verwendet wird.](windowsribbon-intentcl.md)

> [!Note]  
> Viele der erforderlichen Schritte zum Anpassen einer vorhandenen Anwendung ähneln denen, die zum Starten einer neuen Menübandanwendung erforderlich sind. Weitere Informationen finden Sie im Tutorial [Erstellen einer Menübandanwendung](windowsribbon-stepbystep.md) für eine neue Menübandanwendung.

 

Das Menübandmarkup enthält zwei hauptabschnitte. Der erste Abschnitt ist ein Manifest von Befehlen und den zugehörigen Ressourcen (Zeichenfolgen und Bilder). Der zweite Abschnitt gibt die Struktur und Platzierung von Steuerelementen auf dem Menüband an.

Das Markup für den einfachen Text-Editor könnte in etwa wie im folgenden Beispiel aussehen:

> [!Note]  
> Bild- und Zeichenfolgenressourcen werden weiter unten in diesem Artikel behandelt.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Um zu vermeiden, dass Symbole, die von einem Benutzeroberflächenframework wie MFC definiert werden, neu definiert werden, verwendet das vorherige Beispiel etwas andere Symbolnamen für jeden Befehl (ID FILE NEW im Vergleich zu \_ \_ ID \_ CMD \_ NEW). Die numerische ID, die jedem Befehl zugewiesen ist, muss jedoch unverändert bleiben.

Um die Markupdatei in eine Anwendung zu integrieren, konfigurieren Sie einen benutzerdefinierten Buildschritt, um den Menüband-Markupcompiler UICC.exe. Die resultierenden Header- und Ressourcendateien werden dann in das vorhandene Projekt integriert. Wenn die Beispielanwendung des Text-Editor-Menübands den Namen "RibbonPad" hat, ist eine Benutzerdefinierte Buildbefehlszeile erforderlich, die der folgenden ähnelt:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Der Markupcompiler erstellt eine Binärdatei, eine Headerdatei (H) und eine Ressourcendatei (RC). Da die vorhandene Anwendung wahrscheinlich über eine vorhandene RC-Datei verfügt, schließen Sie die generierten H- und RC-Dateien in diese RC-Datei ein, wie im folgenden Beispiel gezeigt:


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Ersetzen von Legacymenüs und Symbolleisten

Das Ersetzen von Standardmenüs und Symbolleisten durch ein Menüband in einer Legacyanwendung erfordert Folgendes:

1.  Entfernen Sie Verweise auf Symbolleisten- und Menüressourcen aus der Ressourcendatei der Anwendung.
2.  Löschen Sie den gesamten Initialisierungscode der Symbolleiste und Menüleiste.
3.  Löschen Sie code, der zum Anfügen einer Symbolleiste oder Menüleiste an das Fenster der obersten Ebene der Anwendung verwendet wird.
4.  Instanziieren Sie das Menübandframework.
5.  Fügen Sie das Menüband an das Fenster der obersten Ebene der Anwendung an.
6.  Laden Sie das kompilierte Markup.

> [!IMPORTANT]
> Vorhandene Statusleisten- und Tastenkombinationstabellen sollten beibehalten werden, da das Menübandframework diese Funktionen nicht ersetzt.

 

Im folgenden Beispiel wird veranschaulicht, wie das Framework mit [**IUIFramework::Initialize initialisiert**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)wird:


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



Im folgenden Beispiel wird veranschaulicht, wie [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) zum Laden des kompilierten Markups verwendet wird:


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



Die CApplication-Klasse, auf die oben verwiesen wird, muss ein Paar von COM-Schnittstellen (Component Object Model) implementieren, die vom Menübandframework definiert werden: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) und [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) stellt die Hauptrückrufschnittstelle zwischen dem Framework und der Anwendung bereit (z. B. wird die Höhe des Menübands über [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)kommuniziert), während die Rückrufe für einzelne Befehle als Reaktion [**auf IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)bereitgestellt werden.

**Tipp:** Einige Anwendungsframeworks, z. B. MFC, erfordern, dass die Höhe der Menübandleiste beim Rendern des Dokumentraums der Anwendung berücksichtigt wird. In diesen Fällen ist das Hinzufügen eines ausgeblendeten Fensters zum Überlagern der Menübandleiste und zum Erzwingen des Dokumentraums auf die gewünschte Höhe erforderlich. Ein Beispiel für diesen Ansatz, bei dem eine Layoutfunktion basierend auf der von der [**IUIRibbon::GetHeight-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) zurückgegebenen Menübandhöhe aufgerufen wird, finden Sie im [HTMLEditRibbon-Beispiel.](windowsribbon-htmleditribbonsample.md)

Im folgenden Codebeispiel wird eine [**IUIApplication::OnViewChanged-Implementierung**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) veranschaulicht:


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementieren eines IUICommandHandler-Adapters

Je nach Entwurf der ursprünglichen Anwendung ist es möglicherweise einfacher, mehrere Befehlshandlerimplementierungen oder einen einzigen Überbrückungsbefehlshandler zu verwenden, der die Befehlslogik der vorhandenen Anwendung aufruft. Viele Anwendungen verwenden WM \_ COMMAND-Nachrichten für diesen Zweck, wobei es ausreichend ist, einen einzigen allzweckbasierten Befehlshandler bereitzustellen, der WM \_ COMMAND-Nachrichten einfach an das Fenster der obersten Ebene weiterleitet.

Dieser Ansatz erfordert jedoch eine besondere Behandlung für Befehle wie **Beenden** oder **Schließen.** Da das Menüband während der Verarbeitung einer Fenstermeldung nicht zerstört werden kann, sollte die WM \_ CLOSE-Nachricht an den UI-Thread der Anwendung gesendet und nicht synchron verarbeitet werden, wie im folgenden Beispiel gezeigt:


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Migrieren von Ressourcen

Wenn das Manifest von Befehlen definiert wurde, die Struktur des Menübands deklariert wurde und der Anwendungscode zum Hosten des Menübandframeworks angepasst wurde, ist der letzte Schritt die Angabe von Zeichenfolgen- und Imageressourcen für jeden Befehl.

> [!Note]  
> Zeichenfolgen- und Bildressourcen werden in der Regel in der Markupdatei bereitgestellt. Sie können jedoch programmgesteuert generiert oder ersetzt werden, indem die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) implementiert wird.

 

### <a name="string-resources"></a>Zeichenfolgenressourcen

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) ist die gängigste Zeichenfolgeneigenschaft, die für einen Befehl definiert ist. Diese werden als Textbeschriftungen für Registerkarten, Gruppen und einzelne Steuerelemente gerendert. Eine Bezeichnungszeichenfolge aus einem Legacymenüelement kann in der Regel ohne große Bearbeitung für **Command.LabelTitle** wiederverwendet werden.

Mit der Einführung des Menübands haben sich jedoch die folgenden Konventionen geändert:

-   Das Suffix mit den Auslassungszeichen (...), das zum Angeben eines Befehls zum Starten des Dialogs verwendet wird, ist nicht mehr erforderlich.
-   Das ampersand (&) kann weiterhin verwendet werden, um eine Tastenkombination für einen Befehl anzugeben, der in einem Menü angezeigt wird, aber die vom Framework unterstützte [**Command.Keytip-Eigenschaft**](windowsribbon-element-command-keytip.md) erfüllt einen ähnlichen Zweck.

In Bezug auf das Text-Editor-Beispiel können die folgenden Zeichenfolgen für LabelTitle und Keytip angegeben werden:



| Symbol           | Ursprüngliche Zeichenfolge | LabelTitle-Zeichenfolge | Keytip-Zeichenfolge |
|------------------|-----------------|-------------------|---------------|
| ID \_ FILE \_ NEW    | &Neu            | &Neu              | N             |
| ID \_ FILE \_ SAVE   | &Speichern           | &Speichern             | E             |
| ID \_ FILE \_ SAVEAS | Save &As...       | Speichern Sie &unter .          | Ein             |
| ID \_ FILE \_ OPEN   | &Öffnen...          | &amp;Open             | O             |
| ID \_ FILE \_ EXIT   | &Beenden           | &Beenden             | X             |
| ID \_ BEARBEITEN \_ RÜCKGÄNGIG   | &Rückgängig           | Rückgängig              | Z             |
| ID \_ EDIT \_ CUT    | Cu&t            | Cu&t              | X             |
| ID \_ EDIT \_ COPY   | &Kopieren           | &Kopieren             | C             |
| ID EDIT PASTE (EINFÜGEN DER ID \_ \_ BEARBEITEN)  | &Einfügen          | &Einfügen            | V             |
| ID \_ EDIT \_ CLEAR  | &Löschen         | &Löschen           | D             |
| ZOOM \_ DER ID-ANSICHT \_   | &Zoom...          | Zoom              | Z             |



 

Im Folgenden finden Sie eine Liste anderer Zeichenfolgeneigenschaften, die für die meisten Befehle festgelegt werden sollten:

-   [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Registerkarten, Gruppen und andere Funktionen der Menüband-Benutzeroberfläche können jetzt mit allen angegebenen Zeichenfolgen- und Bildressourcen deklariert werden.

Im folgenden Menübandmarkupbeispiel werden verschiedene Zeichenfolgenressourcen veranschaulicht:


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Imageressourcen

Das Menübandframework unterstützt Bildformate, die ein viel umfangreicheres Aussehen und Gefühl bieten als die Bildformate, die von vorherigen Menü- und Symbolleistenkomponenten unterstützt werden.

Für Windows 8 und höher unterstützt das Menübandframework die folgenden Grafikformate: 32-Bit-ARGB-Bitmapdateien (BMP) und PNG-Dateien (Portable Network Graphics) mit Transparenz.

Für Windows 7 und früher müssen Bildressourcen dem in Windows verwendeten BMP-Standardgrafikformat entsprechen.

> [!Note]  
> Vorhandene Bilddateien können in beide Formate konvertiert werden. Die Ergebnisse können jedoch weniger zufriedenstellend sein, wenn die Bilddateien keine Antialiasing und Transparenz unterstützen.

 

Es ist nicht möglich, eine einzelne Standardgröße für Bildressourcen im Menübandframework anzugeben. Um jedoch [das adaptive Layout](windowsribbon-templates.md) von Steuerelementen zu unterstützen, können Bilder in zwei Größen (groß und klein) angegeben werden. Alle Bilder im Menübandframework werden entsprechend der DPI-Auflösung (Dots per Inch) der Anzeige skaliert, wobei die genaue gerenderte Größe von dieser DPI-Einstellung abhängt. Weitere Informationen finden Sie unter [Angeben von Menübandbildressourcen.](windowsribbon-imageformats.md)

Im folgenden Beispiel wird veranschaulicht, wie auf einen Satz dpi-spezifischer Bilder im Markup verwiesen wird:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben von Menübandbildressourcen](windowsribbon-imageformats.md)
</dt> </dl>

 

 