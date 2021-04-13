---
title: Migrieren zum Windows-Menü Band Framework
description: Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche des Windows-Menü Band Framework-befehlssystems migriert werden.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows-Menüband, Migrieren zu
- Multifunktionsleiste, Migrieren zu
- Migrieren zu Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473596"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>Migrieren zum Windows-Menü Band Framework

Eine Anwendung, die auf herkömmlichen Menüs, Symbolleisten und Dialogfeldern basiert, kann auf die umfangreiche, dynamische und Kontext gesteuerte Benutzeroberfläche des Windows-Menü Band Framework-befehlssystems migriert werden. Dies ist eine einfache und effektive Möglichkeit, um die Anwendung zu modernisieren und zu beleben und gleichzeitig die Barrierefreiheit, die Benutzerfreundlichkeit und die Auffindbarkeit ihrer Funktionalität zu verbessern.

## <a name="introduction"></a>Einführung

Im allgemeinen umfasst die Migration einer vorhandenen Anwendung zum Menüband-Framework Folgendes:

-   Entwerfen eines Menüband-Layouts und einer Steuerelement Organisation, das die Funktionalität der vorhandenen Anwendung verfügbar macht und flexibel genug ist, um neue Funktionen zu unterstützen.
-   Anpassen des Codes der vorhandenen Anwendung.
-   Migrieren vorhandener Anwendungs Ressourcen (Zeichen folgen und Bilder) zum Menüband-Framework.

> [!Note]  
> Die [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzeroberfläche sollten überprüft werden, um festzustellen, ob die Anwendung für eine Multifunktionsleisten-Benutzeroberfläche geeignet ist

 

## <a name="design-the-ribbon-layout"></a>Entwerfen des Menüband-Layouts

Mögliche Entwurfs-und Steuerelement Layouts der Multifunktionsleiste können durch Ausführen der folgenden Schritte identifiziert werden:

1.  Bestandsaufnahme aller vorhandenen Funktionen.
2.  Übersetzen dieser Funktionalität in Menü Band Befehle.
3.  Organisieren der Befehle in logische Gruppen.

### <a name="take-inventory"></a>Inventur übernehmen

Im Menüband-Framework werden die Funktionen, die von einer Anwendung verfügbar gemacht werden, die den Zustand oder die Ansicht eines Arbeitsbereichs oder Dokuments bearbeitet, als Befehl angesehen. Was einen Befehl ausmacht, kann variieren und hängt von der Art und Domäne der vorhandenen Anwendung ab.

In der folgenden Tabelle sind die grundlegenden Befehle für eine hypothetische Text Bearbeitungs Anwendung aufgeführt:



| Symbol           | id     | BESCHREIBUNG               |
|------------------|--------|---------------------------|
| ID- \_ Datei \_ neu    | 0xe100 | Neues Dokument              |
| ID- \_ Datei \_ Speichern   | 0xe103 | Dokument speichern             |
| ID- \_ Datei ( \_ SaveAs) | 0xe104 | Speichern unter... Dialog       |
| ID- \_ Datei \_ geöffnet   | 0xe101 | Öffnen Sie... Dialog          |
| ID- \_ Datei \_ Beenden   | 0xe102 | Beenden der Anwendung      |
| ID- \_ Bearbeitung \_ rückgängig   | 0xe12b | Rückgängig                      |
| ID- \_ Bearbeitungs \_ Ausschnitt    | 0xe123 | Ausgewählten Text ausschneiden         |
| ID zum \_ Bearbeiten der \_ Kopie   | 0xe122 | Ausgewählten Text kopieren        |
| ID \_ Bearbeiten, \_ Einfügen  | 0xe125 | Text aus Zwischenablage einfügen |
| ID- \_ Bearbeitung \_ Löschen  | 0xe120 | Ausgewählten Text löschen      |
| Vergrößern der ID- \_ Ansicht \_   | 1242   | Zoom... Dialog          |



 

Sehen Sie sich die vorhandenen Menüs und Symbolleisten an, wenn Sie ein Inventar von Befehlen aufbauen. Denken Sie daran, wie Benutzer mit dem Arbeitsbereich interagieren können. Obwohl nicht jeder Befehl für die Einbindung in das Menüband geeignet ist, kann diese Übung sehr gut Befehle verfügbar machen, die zuvor von Benutzeroberflächen Ebenen verdeckt wurden.

### <a name="translate"></a>Translate

Nicht jeder Befehl muss in der Menüband-Benutzeroberfläche dargestellt werden. Wenn Sie z. b. Text eingeben, eine Auswahl ändern, einen Bildlauf durchführen oder die Einfügemarke mit der Maus bewegen, sind diese als Befehle im hypothetischen Text-Editor qualifiziert. Diese können jedoch nicht in einer Befehlsleiste verfügbar gemacht werden, da jeweils eine direkte Interaktion mit der Benutzeroberfläche der Anwendung besteht.

Im Gegensatz dazu werden einige Funktionen möglicherweise nicht als Befehl im herkömmlichen Sinne betrachtet. Anstatt z. b. in einem Dialogfeld verborgen zu sein, können Seitenränder im Menüband als Gruppe von Spinner-Steuerelementen in einer Kontext Registerkarte oder im [Anwendungsmodus](ribbon-applicationmodes.md)dargestellt werden.

> [!Note]  
> Notieren Sie sich die numerische ID, die jedem Befehl zugewiesen werden kann. Einige Benutzeroberflächen-Frameworks, wie z. b. Microsoft Foundation Classes (MFC), definieren IDs für Befehle, z. b. die Datei und das Bearbeitungs Menü (0xe100 bis 0xe200).

 

### <a name="organize"></a>Organisieren

Bevor Sie versuchen, die Befehls Inventur zu organisieren, sollten Sie die [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzeroberfläche auf bewährte Methoden beim Implementieren einer Multifunktionsleisten-Benutzeroberfläche

Im Allgemeinen können die folgenden Regeln auf die Menü Band Befehls Organisation angewendet werden:

-   Befehle, die für die Datei oder die gesamte Anwendung ausgeführt werden, gehören höchstwahrscheinlich im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md).
-   Häufig verwendete Befehle, wie z. b. Ausschneiden, kopieren und Einfügen (wie im Beispiel Text-Editor), werden in der Regel auf einer Standard Registerkarte Home abgelegt. In komplexeren Anwendungen können Sie an anderer Stelle in der Menüband-Benutzeroberfläche dupliziert werden.
-   Wichtige oder häufig verwendete Befehle können die Standard Einbindung in der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)rechtfertigen.

Das Menüband-Framework stellt außerdem die ContextMenu-und MiniToolbar-Steuerelemente über die contextpopup-Ansicht bereit. Diese Features sind nicht obligatorisch, aber wenn Ihre Anwendung über mindestens ein vorhandenes Kontextmenü verfügt, kann die Verwendung der enthaltenen Befehle möglicherweise die Wiederverwendung der vorhandenen Codebasis mit automatischer Bindung an vorhandene Ressourcen ermöglichen.

Da jede Anwendung unterschiedlich ist, lesen Sie die Richtlinien, und versuchen Sie, Sie so umfassend wie möglich anzuwenden. Eines der Ziele des Multifunktionsleisten-Frameworks ist das Bereitstellen einer vertrauten, konsistenten Benutzer Darstellung. dieses Ziel ist besser, wenn die Entwürfe für neue Anwendungen vorhandene Multifunktionsleisten-Anwendungen so weit wie möglich spiegeln.

## <a name="adapt-your-code"></a>Anpassen Ihres Codes

Nachdem die Menüband-Befehle identifiziert und in logische Gruppierungen organisiert wurden, hängt die Anzahl der Schritte, die bei der Einbindung des Multifunktionsleisten-Frameworks in vorhandenen Anwendungscode aufgetreten sind, von der Komplexität der ursprünglichen Anwendung ab. Im Allgemeinen gibt es drei grundlegende Schritte:

-   Erstellen Sie das Menüband-Markup auf der Grundlage der Befehls Organisation und Layoutspezifikation.
-   Ersetzen Sie die Legacy Menü-und Symbolleisten Funktionalität durch Multifunktionsleisten-Funktionalität
-   Implementieren Sie einen iuicommandhandler-Adapter.

### <a name="create-the-markup"></a>Markup erstellen

Die Liste der Befehle sowie deren Organisation und Layout werden über die Menüband-Markup Datei deklariert, die vom [Menüband-Markup Compiler](windowsribbon-intentcl.md)verwendet wird.

> [!Note]  
> Viele der Schritte, die erforderlich sind, um eine vorhandene Anwendung anzupassen, ähneln den Schritten, die zum Starten einer neuen Multifunktionsleistenanwendung erforderlich sind. Weitere Informationen finden Sie im Tutorial [Erstellen einer Menüband-Anwendung](windowsribbon-stepbystep.md) für eine neue Exemplarische Vorgehensweise für eine Menüband-Anwendung.

 

Es gibt zwei primäre Abschnitte zum Menü Band Markup. Der erste Abschnitt ist ein Manifest von Befehlen und den zugehörigen Ressourcen (Zeichen folgen und Bilder). Der zweite Abschnitt gibt die Struktur und die Platzierung von Steuerelementen auf dem Menüband an.

Das Markup für den einfachen Text-Editor kann in etwa wie im folgenden Beispiel aussehen:

> [!Note]  
> Bild-und Zeichen folgen Ressourcen werden weiter unten in diesem Artikel behandelt.

 


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



Um das erneute definieren von Symbolen zu vermeiden, die von einem UI-Framework wie MFC definiert werden, verwendet das vorherige Beispiel für jeden Befehl etwas andere Symbolnamen (ID- \_ Datei \_ New und ID \_ cmd \_ New). Die numerische ID, die den einzelnen Befehlen zugewiesen ist, muss jedoch unverändert bleiben.

Um die Markup Datei in eine Anwendung zu integrieren, konfigurieren Sie einen benutzerdefinierten Buildschritt, um den Menü Band Markup Compiler (UICC.exe) auszuführen. Die resultierenden Header-und Ressourcen Dateien werden dann in das vorhandene Projekt integriert. Wenn die Menüband-Anwendung für den Beispiel Text-Editor den Namen "ribbonpad" hat, ist eine benutzerdefinierte Buildbefehlszeile ähnlich der folgenden erforderlich:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Der Markup Compiler erstellt eine Binärdatei, eine Header Datei (H) und eine Ressourcen Datei (RC). Da die vorhandene Anwendung wahrscheinlich über eine vorhandene RC-Datei verfügt, müssen Sie die generierten H-und RC-Dateien in diese RC-Datei einschließen, wie im folgenden Beispiel gezeigt:


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



### <a name="replace-legacy-menus-and-toolbars"></a>Legacy Menüs und Symbolleisten ersetzen

Zum Ersetzen von Standardmenüs und Symbolleisten durch ein Menüband in einer Legacy Anwendung ist Folgendes erforderlich:

1.  Entfernen Sie Symbolleisten-und Menü Ressourcen Verweise aus der Ressourcen Datei der Anwendung.
2.  Löscht den gesamten Initialisierungs Code der Symbolleisten-und Menüleiste.
3.  Löschen Sie den Code, der zum Anfügen einer Symbolleiste oder einer Menüleiste an das Fenster der obersten Ebene der Anwendung verwendet wird.
4.  Instanziieren Sie das Menüband-Framework.
5.  Fügen Sie das Menüband an das Fenster der obersten Ebene der Anwendung an.
6.  Laden Sie das kompilierte Markup.

> [!IMPORTANT]
> Vorhandene Statusleiste und Tastatur Verknüpfungs Tabellen sollten beibehalten werden, da das Menüband-Framework diese Features nicht ersetzt.

 

Im folgenden Beispiel wird veranschaulicht, wie das Framework mithilfe von [**iuiframework:: Initialisieren**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)initialisiert wird:


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



Im folgenden Beispiel wird veranschaulicht, wie [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) verwendet wird, um das kompilierte Markup zu laden:


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



Die capplication-Klasse, auf die oben verwiesen wird, muss ein paar von Component Object Model (com)-Schnittstellen implementieren, die durch das Menüband-Framework definiert werden: [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) und [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**Iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) stellt die Haupt Rückruf Schnittstelle zwischen dem Framework und der Anwendung bereit (z. b. wird die Höhe des Menübands über [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)kommuniziert), während die Rückrufe für einzelne Befehle als Antwort auf [**iuiapplication:: onkreateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)bereitgestellt werden.

**Tipp:** Einige Anwendungs Frameworks, wie z. b. MFC, erfordern, dass die Höhe der Menü Band Leiste beim Rendern des Dokument Raums der Anwendung berücksichtigt wird. In diesen Fällen ist das Hinzufügen eines ausgeblendeten Fensters zum Überlagern der Menü Band Leiste und das Erzwingen des Dokument Raums zur gewünschten Höhe erforderlich. Ein Beispiel für diesen Ansatz, bei dem eine Layoutfunktion basierend auf der von der [**iuiribbon:: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) -Methode zurückgegebenen Menüband-Höhe aufgerufen wird, finden Sie im [htmleditribbon-Beispiel](windowsribbon-htmleditribbonsample.md).

Im folgenden Codebeispiel wird eine [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) -Implementierung veranschaulicht:


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



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementieren eines iuicommandhandler-Adapters

Abhängig vom Entwurf der ursprünglichen Anwendung ist es möglicherweise einfacher, mehrere Befehls Handlerimplementierungen zu haben, oder einen einzelnen Bridging-Befehls Handler, der die vorhandene Anwendungs Befehls Logik aufruft. Viele Anwendungen verwenden \_ für diesen Zweck WM-befehlsnachrichten, bei denen es ausreichend ist, einen einzelnen Befehls Handler für alle Zwecke bereitzustellen, der einfach WM- \_ Befehls Meldungen an das Fenster der obersten Ebene weiterleitet.

Bei diesem Ansatz ist jedoch eine spezielle Behandlung für Befehle wie " **Exit** " oder " **Close**" erforderlich. Da das Menüband nicht zerstört werden kann, während es eine Fenster Nachricht verarbeitet, \_ sollte die WM close-Nachricht an den UI-Thread der Anwendung gesendet werden und sollte nicht synchron verarbeitet werden, wie im folgenden Beispiel gezeigt:


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

Wenn das Manifest der Befehle definiert wurde, die Struktur des Menübands deklariert wurde und der Anwendungscode zum Hosten des Menüband-Frameworks angepasst wurde, ist der letzte Schritt die Angabe von Zeichen folgen-und Bild Ressourcen für jeden Befehl.

> [!Note]  
> Zeichen folgen-und Bild Ressourcen werden in der Regel in der Markup Datei bereitgestellt. Sie können jedoch Programm gesteuert durch Implementieren der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode generiert oder ersetzt werden.

 

### <a name="string-resources"></a>Zeichen folgen Ressourcen

[**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) ist die häufigste Zeichen folgen Eigenschaft, die für einen Befehl definiert ist. Diese werden als Text Beschriftungen für Registerkarten, Gruppen und einzelne Steuerelemente gerendert. Eine Bezeichnungs Zeichenfolge aus einem Legacy Menü Element kann in der Regel für einen **Befehl. labeltitle** ohne große Bearbeitung wieder verwendet werden.

Die folgenden Konventionen haben sich jedoch bei der Einführung des Menübands geändert:

-   Das Auslassungs Zeichen (...), das verwendet wird, um einen Befehl zum Starten des Dialog Felds anzugeben, ist nicht mehr erforderlich.
-   Das kaufmännische und-Objekt (&) kann weiterhin verwendet werden, um eine Tastenkombination für einen Befehl anzugeben, der in einem Menü angezeigt wird, die vom Framework unterstützte [**Command. KeyTip**](windowsribbon-element-command-keytip.md) -Eigenschaft erfüllt jedoch einen ähnlichen Zweck.

Wenn Sie auf das Beispiel Text-Editor zurückverweisen, können die folgenden Zeichen folgen für "labeltitle" und "KeyTip" angegeben werden:



| Symbol           | Ursprüngliche Zeichenfolge | Labeltitle-Zeichenfolge | KeyTip-Zeichenfolge |
|------------------|-----------------|-------------------|---------------|
| ID- \_ Datei \_ neu    | Neu &            | Neu &              | N             |
| ID- \_ Datei \_ Speichern   | &speichern           | &speichern             | E             |
| ID- \_ Datei ( \_ SaveAs) | &speichern unter...       | &speichern unter          | A             |
| ID- \_ Datei \_ geöffnet   | &geöffnet...          | &amp;Open             | O             |
| ID- \_ Datei \_ Beenden   | &Beenden           | &Beenden             | X             |
| ID- \_ Bearbeitung \_ rückgängig   | &rückgängig machen           | Rückgängig              | Z             |
| ID- \_ Bearbeitungs \_ Ausschnitt    | Cu&t            | Cu&t              | X             |
| ID zum \_ Bearbeiten der \_ Kopie   | &Kopie           | &Kopie             | C             |
| ID \_ Bearbeiten, \_ Einfügen  | &einfügen          | &einfügen            | V             |
| ID- \_ Bearbeitung \_ Löschen  | &löschen         | &löschen           | D             |
| Vergrößern der ID- \_ Ansicht \_   | &Zoom...          | Zoom              | Z             |



 

Im folgenden finden Sie eine Liste anderer Zeichen folgen Eigenschaften, die für die meisten Befehle festgelegt werden sollten:

-   [**Command. labeldescription**](windowsribbon-element-command-labeldescription.md)
-   [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md)

Registerkarten, Gruppen und andere Funktionen der Multifunktionsleisten-Benutzeroberfläche können jetzt mit allen angegebenen Zeichen folgen-und Bild Ressourcen deklariert werden.

Im folgenden Menüband-Markup Beispiel werden verschiedene Zeichen folgen Ressourcen veranschaulicht:


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



### <a name="image-resources"></a>Bild Ressourcen

Das Menüband-Framework unterstützt Bildformate, die ein viel reicheres Aussehen und Gefühl bieten als die Bildformate, die von vorherigen Menü-und Symbolleisten Komponenten unterstützt

Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.

Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.

> [!Note]  
> Vorhandene Bilddateien können in beide Formate konvertiert werden. Die Ergebnisse sind jedoch möglicherweise kleiner als zufriedenstellend, wenn die Bilddateien Antialiasing und Transparenz nicht unterstützen.

 

Es ist nicht möglich, eine einzelne Standardgröße für Bild Ressourcen im Menüband-Framework anzugeben. Um das [Adaptive Layout](windowsribbon-templates.md) von Steuerelementen zu unterstützen, können Bilder jedoch in zwei Größen (groß und klein) angegeben werden. Alle Bilder im Menüband-Framework werden entsprechend der dpi-Auflösung (dpi) der Anzeige mit der exakten gerenderten Größe skaliert, die von dieser dpi-Einstellung abhängig ist. Weitere Informationen finden Sie unter [Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md) .

Im folgenden Beispiel wird veranschaulicht, wie auf einen Satz von dpi-spezifischen Bildern im Markup verwiesen wird:


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

[Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md)
</dt> </dl>

 

 