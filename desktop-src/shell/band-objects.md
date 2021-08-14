---
description: Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4.0 eingeführt, um einen Anzeigebereich neben dem Browserbereich zu bieten.
title: Erstellen von benutzerdefinierten Explorer-Leisten, Tool-Bändern und Desk-Bändern
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9a57cc5bc8afa3e973c6d4d99b8bcee186287a6c9278407b900f84500d7d0e51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461741"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Erstellen von benutzerdefinierten Explorer-Balken, Toolbändern und Deskbändern

Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4.0 eingeführt, um einen Anzeigebereich neben dem Browserbereich zu bieten. Im Grunde handelt es sich um ein untergeordnetes Fenster innerhalb Windows Internet Explorer Fensters, und es kann verwendet werden, um Informationen anzuzeigen und auf die gleiche Weise mit dem Benutzer zu interagieren. Explorer-Balken werden am häufigsten als vertikaler Bereich auf der linken Seite des Browserbereichs angezeigt. Eine Explorer-Leiste kann jedoch auch horizontal unterhalb des Browserbereichs angezeigt werden.

![Screenshot der vertikalen und horizontalen Explorer-Balken](images/expl1.jpg)

Es gibt eine Vielzahl von möglichen Verwendungsmöglichkeiten für die Explorer-Leiste. Benutzer können auf verschiedene Arten auswählen, welche Option sie anzeigen  möchten, z.  B. im Untermenü Explorer-Leiste des Menüs Ansicht oder durch Klicken auf eine Symbolleistenschaltfläche. Internet Explorer bietet mehrere Standardmäßige Explorer-Balken, einschließlich Favoriten und Suche.

Eine der Möglichkeiten zum Anpassen von Internet Explorer ist das Hinzufügen einer benutzerdefinierten Explorer-Leiste. Wenn sie implementiert und registriert ist, wird sie dem **Untermenü Explorer-Leiste** des Menüs **Ansicht** hinzugefügt. Wenn diese Option vom Benutzer ausgewählt wird, kann der Anzeigebereich der Explorer-Leiste verwendet werden, um Informationen anzuzeigen und Benutzereingaben auf die gleiche Weise wie ein normales Fenster zu übernehmen.

![Screenshot der Explorer-Balken](images/expl2.jpg)

Um eine benutzerdefinierte Explorer-Leiste zu erstellen, müssen Sie ein *Bandobjekt implementieren und registrieren.* Bandobjekte wurden mit Version 4.71 der Shell eingeführt und bieten Ähnliches wie normale Fenster. Da sie jedoch Component Object Model (COM) sind und entweder in Internet Explorer shell enthalten sind, werden sie etwas anders implementiert. Einfache Bandobjekte wurden verwendet, um die in der ersten Grafik angezeigten Explorer-Beispielleisten zu erstellen. Die Implementierung des vertikalen Explorer-Balkenbeispiels wird in einem späteren Abschnitt ausführlich erläutert.

## <a name="tool-bands"></a>Toolbänder

Ein *Toolband* ist ein Bandobjekt, das mit Microsoft Internet Explorer 5 eingeführt wurde, um die Windows-Symbolleistenfunktion zu unterstützen. Die Internet Explorer symbolleiste ist tatsächlich ein Steuerelement für die [Symbolleiste,](../controls/rebar-controls.md) das mehrere Symbolleistensteuerelemente [enthält.](../controls/toolbar-control-reference.md) Indem Sie ein Toolband erstellen, können Sie diesem Rebar-Steuerelement ein Band hinzufügen. Wie Explorer-Balken ist ein Toolband jedoch ein allgemeines Fenster.

![Screenshot von Toolbändern](images/toolband1.jpg)

Benutzer zeigen eine Symbolleiste an, indem sie sie  im Untermenü Symbolleisten des **Menüs** Ansicht oder im Kontextmenü auswählen, das durch Klicken mit der rechten Maustaste auf den Symbolleistenbereich angezeigt wird.

## <a name="desk-bands"></a>DeskBands

Bandobjekte können auch zum Erstellen von *Deskbändern verwendet werden.* Die grundlegende Implementierung ähnelt Explorer-Balken, aber Desk-Bänder stehen nicht mit Internet Explorer. Eine Deskband ist im Grunde eine Möglichkeit, ein andockbares Fenster auf dem Desktop zu erstellen. Der Benutzer wählt sie aus, indem er mit der rechten Maustaste auf die Taskleiste klickt und sie im Untermenü **Symbolleisten** auswählt.

![Screenshot, der eine Beispieldesk desk-Band zeigt.](images/desk2.png)

Anfangs werden Die Deskbänder an die Taskleiste angedockt.

![Screenshot: An der Taskleiste angedockte Deskbänder](images/desk1.jpg)

Der Benutzer kann dann das Deskband auf den Desktop ziehen und wird als normales Fenster angezeigt.

![Screenshot von Deskbändern](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementieren von Bandobjekten

Die folgenden Themen werden erläutert.

-   [Grundlagen zu Bandobjekten](#band-object-basics)
-   [Bandregistrierung](#band-registration)
-   [Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Grundlagen zu Bandobjekten

Obwohl sie ähnlich wie normale Fenster verwendet werden können, sind Bandobjekte COM-Objekte, die in einem Container vorhanden sind. Explorer-Balken sind in Internet Explorer, und Deskbänder sind in der Shell enthalten. Obwohl sie verschiedene Funktionen erfüllen, ist ihre grundlegende Implementierung sehr ähnlich. Der Hauptunterschied besteht in der Registrierung des Bandobjekts, das wiederum den Typ des Objekts und dessen Container steuert. In diesem Abschnitt werden die Aspekte der Implementierung erläutert, die allen Bandobjekten gemeinsam sind. Weitere [Implementierungsdetails finden Sie unter](#a-simple-example-of-a-custom-explorer-bar) Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste.

Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)müssen alle Bandobjekte die folgenden Schnittstellen implementieren.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**Iobjectwithsite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**Ipersiststream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Zusätzlich zum Registrieren des Klassenbezeichners (CLSID) müssen die Explorer-Balken- und Deskbandobjekte auch für die entsprechende Komponentenkategorie registriert werden. Das Registrieren der Komponentenkategorie bestimmt den Objekttyp und dessen Container. Toolgruppen verwenden ein anderes Registrierungsverfahren und verfügen nicht über einen Kategoriebezeichner (CATID). Die CATIDs für die drei Bandobjekte, die sie erfordern, sind:



| Bandtyp               | Komponentenkategorie |
|-------------------------|--------------------|
| Vertikale Explorer-Leiste   | CATID \_ InfoBand    |
| Horizontale Explorer-Leiste | CATID \_ CommBand    |
| Desk Band               | CATID \_ DeskBand    |



 

Weitere [Informationen zum Registrieren von](#band-registration) Bandobjekten finden Sie unter Bandregistrierung.

Wenn das Bandobjekt Benutzereingaben akzeptieren soll, muss es auch [**IInputObject implementieren.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) Zum Hinzufügen von Elementen zum Kontextmenü für Explorer-Balken- oder -Deskbänder muss das Bandobjekt [**IContextMenu exportieren.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Toolbänder unterstützen keine Kontextmenüs.

Da Bandobjekte ein untergeordnetes Fenster implementieren, müssen sie auch eine Fensterprozedur implementieren, um Windows verarbeiten.

Bandobjekte können Befehle über die [**IOleCommandTarget-Schnittstelle**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) des Containers an ihren Container senden. Um den Schnittstellenzeiger zu erhalten, rufen Sie die [**IInputObjectSite::QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) des Containers auf, und fragen Sie nach IID \_ IOleCommandTarget. Anschließend senden Sie Befehle mit [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec)an den Container. Die Befehlsgruppe ist CGID \_ DeskBand. Wenn die [**IDeskBand::GetBandInfo-Methode**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) eines Bandobjekts aufgerufen wird, verwendet der Container den *dwBandID-Parameter,* um dem Bandobjekt einen Bezeichner zu zuweisen, der für drei der Befehle verwendet wird. Vier **IOleCommandTarget::Exec-Befehls-IDs** werden unterstützt.

-   DBID \_ BANDINFOCHANGED

    Die Bandinformationen haben sich geändert. Legen Sie *den pvaIn-Parameter* auf den Bandbezeichner fest, der beim letzten Aufruf von [**IDeskBand::GetBandInfo empfangen wurde.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) Der Container aufruft die **IDeskBand::GetBandInfo-Methode** des Bandobjekts, um die aktualisierten Informationen an fordern.

-   DBID \_ MAXIMIZEBAND

    Maximieren Sie das Band. Legen Sie *den pvaIn-Parameter* auf den Bandbezeichner fest, der beim letzten Aufruf von [**IDeskBand::GetBandInfo empfangen wurde.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)

-   DBID \_ SHOWONLY

    Aktivieren oder deaktivieren Sie andere Bänder im Container. Legen Sie *den pvaIn-Parameter* mit einem der folgenden Werte auf den Typ VT \_ UNKNOWN fest:

    

    | Wert | Beschreibung                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | Punk  | Ein Zeiger auf die [**IUnknown-Schnittstelle des Bandobjekts.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Alle anderen Deskbänder werden ausgeblendet. |
    | 0     | Blendet alle Deskbänder aus.                                                                                        |
    | 1     | Alle Deskbands anzeigen.                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [Version 5.](versions.md) Anzeigen eines Chevronmenüs. Der Container sendet eine [**RB \_ PUSHCHEVRON-Nachricht,**](../controls/rb-pushchevron.md) und das Bandobjekt empfängt eine [RBN-CHEVRONPUSHED-Benachrichtigung, \_](../controls/rbn-chevronpushed.md) die ihn zur Anzeige des Chevronmenüs aufgefordert. Legen Sie den *Parameter nCmdExecOpt* der [**IOleCommandTarget::Exec-Methode**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) auf den Bandbezeichner fest, der beim letzten Aufruf von [**IDeskBand::GetBandInfo empfangen wurde.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) Legen Sie den *pvaIn-Parameter* der **IOleCommandTarget::Exec-Methode** auf den Typ VT \_ I4 mit einem anwendungsdefinierten Wert fest. Es wird als *lAppValue-Wert* der RBN-CHEVRONPUSHED-Benachrichtigung an das Bandobjekt \_ übergeben.

### <a name="band-registration"></a>Bandregistrierung

Ein Bandobjekt muss als OLE-Prozessserver registriert werden, der Apartmentthreading unterstützt. Der Standardwert für den Server ist eine Menütextzeichenfolge. Für Explorer-Balken wird sie im Untermenü **Explorer-Leiste** des **menüs** ansicht Internet Explorer angezeigt. Für Toolbänder wird sie im Untermenü **Symbolleisten** des  Menüs ansicht Internet Explorer angezeigt. Für Desk-Bänder wird sie im Untermenü **Symbolleisten** des Kontextmenüs der Taskleiste angezeigt. Wie bei Menüressourcen führt das Platzieren eines ampersand (&) vor einem Buchstaben dazu, dass es unterstrichen wird und Tastenkombinationen aktiviert wird. Die Menüzeichenfolge für die vertikale Explorer-Leiste, die in der ersten Grafik angezeigt wird, ist beispielsweise "Sample &Vertical Explorer Bar".

Anfänglich ruft Internet Explorer mithilfe der Komponentenkategorien eine Enumeration der registrierten Explorer-Bar-Objekte aus der Registrierung ab. Um die Leistung zu erhöhen, wird diese Enumeration zwischengespeichert, sodass anschließend hinzugefügte Explorer-Balken übersehen werden. Um zu erzwingen, dass Windows Internet Explorer den Cache neu erstellen und eine neue Explorer-Leiste erkennen, löschen Sie die folgenden Registrierungsschlüssel während der Registrierung der neuen Explorer-Leiste:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021493-0000-0000-C000-0000000000046}** \\ **Enum**

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021494-0000-0000-C000-0000000000046}** \\ **Enum**

> [!Note]  
> Da für jeden Benutzer ein Explorer-Balkencache erstellt wird, muss Ihre Setupanwendung möglicherweise alle Benutzerregistrierungsstrukturen auflisten oder einen pro Benutzer ausgeführten Stub hinzufügen, wenn sich der Benutzer zum ersten Mal anmeldet.

 

Im Allgemeinen wird der grundlegende Registrierungseintrag für ein Bandobjekt wie folgt angezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Toolbänder müssen auch die CLSID ihres Objekts bei Internet Explorer registriert haben. Weisen Sie hierzu einen Wert unter **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Toolbar** mit dem Namen mit der CLSID-GUID des Toolbandobjekts zu, wie hier gezeigt. Sein Datenwert wird ignoriert, sodass der Werttyp unwichtig ist.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Es gibt mehrere optionale Werte, die auch der Registrierung hinzugefügt werden können. Beispielsweise ist der folgende Wert erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten. Der angezeigte Wert ist kein Beispiel, sondern der tatsächliche Wert, der verwendet werden soll.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

In Verbindung mit dem oben gezeigten Wert ist auch der folgende optionale Wert erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten. Dieser Wert sollte auf den Speicherort der Datei festgelegt werden, die den HTML-Inhalt für die Explorer-Leiste enthält.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Ein anderer optionaler Wert definiert die Standardbreite oder -höhe der Explorer-Leiste, je nachdem, ob sie vertikal oder horizontal ist.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

Der BarSize-Wert sollte auf die Breite oder Höhe des Balkens festgelegt werden. Der Wert erfordert acht Bytes und wird als Binärwert in der Registrierung platziert. Die ersten vier Bytes geben die Größe in Pixel im Hexadezimalformat an, beginnend mit dem ganz links liegenden Byte. Die letzten vier Bytes sind reserviert und sollten auf 0 (null) festgelegt werden.

Beispielsweise werden hier die vollständigen Registrierungseinträge für eine HTML-fähige Explorer-Leiste mit einer Standardbreite von 291 Pixeln (0x123) angezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

Sie können die Registrierung der CATID eines Bandobjekts programmgesteuert verarbeiten. Erstellen Sie ein Komponentenkategorien-Manager-Objekt (CLSID \_ StdComponentCategoriesMgr), und fordern Sie einen Zeiger auf die [**zugehörige ICatRegister-Schnittstelle**](/windows/win32/api/comcat/nn-comcat-icatregister) an. Übergeben Sie die CLSID und CATID des Bandobjekts an [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste

Dieses Beispiel durchläuft die Implementierung der vertikalen Explorer-Leiste, die in der Einführung gezeigt wird.

Das grundlegende Verfahren zum Erstellen einer benutzerdefinierten Explorer-Leiste lautet wie folgt.

1.  [Implementieren Sie die funktionen, die von der DLL benötigt werden.](#dll-functions)
2.  [Implementieren Sie die erforderlichen COM-Schnittstellen.](#required-interface-implementations)
3.  [Implementieren Sie alle gewünschten optionalen COM-Schnittstellen.](#optional-interface-implementations)
4.  [Registrieren Sie die CLSID des Objekts und bei Bedarf die Komponentenkategorie.](#clsid-registration)
5.  Erstellen Sie ein untergeordnetes Fenster mit Internet Explorer größe, das an den Anzeigebereich der Explorer-Leiste angepasst ist.
6.  [Verwenden Sie das untergeordnete Fenster, um Informationen anzuzeigen und mit dem Benutzer zu interagieren.](#the-window-procedure)

Die sehr einfache Implementierung, die im Explorer-Balkenbeispiel verwendet wird, kann tatsächlich für einen Der-Explorer-Bar-Typ oder ein Desk-Band verwendet werden, indem sie einfach für die entsprechende Komponentenkategorie registriert wird. Komplexere Implementierungen müssen für die Anzeigeregion und den Container jedes Objekttyps angepasst werden. Ein Großteil dieser Anpassung kann jedoch erreicht werden, indem der Beispielcode verwendet und erweitert wird, indem vertraute Windows Programmiertechniken auf das untergeordnete Fenster angewendet werden. Beispielsweise können Sie Steuerelemente für die Benutzerinteraktion oder Grafiken für eine umfangreichere Anzeige hinzufügen.

### <a name="dll-functions"></a>DLL-Funktionen

Alle drei Objekte sind in einer einzelnen DLL gepackt, die die folgenden Funktionen verfügbar macht.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**Dllgetclassobject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Die ersten drei Funktionen sind Standardimplementierungen und werden hier nicht erläutert. Die Class Factory-Implementierung ist ebenfalls standard.

### <a name="required-interface-implementations"></a>Erforderliche Schnittstellenimplementierungen

Das vertikale Explorer-Balkenbeispiel implementiert die vier erforderlichen Schnittstellen: [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IObjectWithSite,**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)und [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) als Teil der CExplorerBar-Klasse. Die Konstruktor-, Destruktor- und **IUnknown-Implementierungen** sind unkompliziert und werden hier nicht erläutert. Sehen Sie sich den Beispielcode an, um ausführliche Informationen zu erhalten.

Die folgenden Schnittstellen werden ausführlich erläutert.

-   [Iobjectwithsite](#iobjectwithsite)
-   [Ipersiststream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>Iobjectwithsite

Wenn der Benutzer eine Explorer-Leiste auswählt, ruft der Container die [**IObjectWithSite::SetSite-Methode**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) des entsprechenden Bandobjekts auf. Der *Parameter "libSite"* wird auf den [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) der Website festgelegt.

Im Allgemeinen sollte eine [**SetSite-Implementierung**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) die folgenden Schritte ausführen:

1.  Geben Sie alle Sitezeiger frei, die derzeit gehalten werden.
2.  Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) übergebene Zeiger auf **NULL** festgelegt ist, wird das Band entfernt. **SetSite** kann S \_ OK zurückgeben.
3.  Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) übergebene Zeiger ungleich **NULL** ist, wird eine neue Website festgelegt. **SetSite** sollte folgende Schritte ausführen:
    1.  Rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der Website für die [**IOleWindow-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) auf.
    2.  Rufen Sie [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) auf, um das Handle des übergeordneten Fensters abzurufen. Speichern Sie das Handle zur späteren Verwendung. Geben Sie [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) frei, wenn es nicht mehr benötigt wird.
    3.  Erstellen Sie das Fenster des Bandobjekts als untergeordnetes Element des Im vorherigen Schritt abgerufenen Fensters. Erstellen Sie es nicht als sichtbares Fenster.
    4.  Wenn das Bandobjekt [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)implementiert, rufen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der Website für seine [**IInputObjectSite-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) auf. Store den Zeiger auf diese Schnittstelle zur späteren Verwendung.
    5.  Wenn alle Schritte erfolgreich sind, geben Sie S \_ OK zurück. Falls nicht, geben Sie den OLE-definierten Fehlercode zurück, der angibt, was fehlgeschlagen ist.

Im Beispiel der Explorer-Leiste wird [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) wie folgt implementiert. Im folgenden Code ist *m \_ pSite* eine private Membervariable, die den [**IInputObjectSite-Zeiger**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) und *m \_ hwndParent* das Handle des übergeordneten Fensters enthält. In diesem Beispiel wird auch die Fenstererstellung behandelt. Wenn das Fenster nicht vorhanden ist, erstellt diese Methode das Fenster der Explorer-Leiste als entsprechend dimensioniertes untergeordnetes Element des übergeordneten Fensters, das von **SetSite** abgerufen wird. Das Handle des untergeordneten Fensters wird in *m \_ hwnd* gespeichert.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



Die [**GetSite-Implementierung**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) des Beispiels umschließt einfach einen Aufruf der [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) der Website mithilfe des von [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)gespeicherten Standortzeigers.


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>Ipersiststream

Internet Explorer ruft die [**IPersistStream-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersiststream) der Explorer-Leiste auf, damit die Explorer-Leiste persistente Daten laden oder speichern kann. Wenn keine persistenten Daten vorhanden sind, müssen die Methoden trotzdem einen Erfolgscode zurückgeben. Die **IPersistStream-Schnittstelle** erbt von [**IPersist,**](/windows/win32/api/objidl/nn-objidl-ipersist)sodass fünf Methoden implementiert werden müssen.

-   [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream::IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream::Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream::GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

Das Explorer-Balkenbeispiel verwendet keine persistenten Daten und verfügt nur über eine minimale Implementierung von [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) gibt die CLSID (CLSID \_ SampleExplorerBar) des Objekts zurück, und der Rest gibt entweder S \_ OK, S \_ FALSE oder E \_ NOTIMPL zurück.

### <a name="ideskband"></a>IDeskBand

Die [**IDeskBand-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) ist spezifisch für Bandobjekte. Zusätzlich zu ihrer einzigen Methode erbt sie von [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), das wiederum von [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)erbt.

Es gibt zwei [**IOleWindow-Methoden:**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) und [**IOleWindow::ContextSensitiveHelp.**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp) Die Implementierung von **GetWindow** im Explorer-Balkenbeispiel gibt das untergeordnete Fensterhandle der Explorer-Leiste m *\_ hwnd zurück.* Kontextbezogene Hilfe ist nicht implementiert, **sodass ContextSensitiveHelp** **E \_ NOTIMPL** zurückgibt.

Die [**IDockingWindow-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) verfügt über drei Methoden.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

Die [**ResizeBorderDW-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) wird nicht mit einem Bandobjekttyp verwendet und sollte immer E \_ NOTIMPL zurückgeben. Die [**ShowDW-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) zeigt das Fenster der Explorer-Leiste abhängig vom Wert ihres Parameters an oder blendet es aus.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



Die [**CloseDW-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) zerstört das Fenster der Explorer-Leiste.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



Die verbleibende Methode, [**GetBandInfo,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)ist für **IDeskBand** spezifisch. Internet Explorer verwendet sie, um den Bezeichner und anzeigemodus der Explorer-Leiste anzugeben. Internet Explorer können auch informationen von der Explorer-Leiste anfordern, indem sie den **dwMask-Member** der [**DESKBANDINFO-Struktur**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) ausfüllen, der als dritter Parameter übergeben wird. **GetBandInfo** sollte den Bezeichner und den Anzeigemodus speichern und die **DESKBANDINFO-Struktur** mit den angeforderten Daten füllen. Im Beispiel für die Explorer-Leiste wird **GetBandInfo** implementiert, wie im folgenden Codebeispiel gezeigt.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Optionale Schnittstellenimplementierungen

Es gibt zwei Schnittstellen, die nicht erforderlich sind, aber für die Implementierung nützlich sein können: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) und [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Im Explorer-Balkenbeispiel wird **IInputObject** implementiert. Informationen zum Implementieren von **IContextMenu** finden Sie in der Dokumentation.

### <a name="iinputobject"></a>IInputObject

Die [**IInputObject-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) muss implementiert werden, wenn ein Bandobjekt Benutzereingaben akzeptiert. Internet Explorer implementiert [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) und verwendet **IInputObject,** um den Richtigen Benutzereingabefokus beizubehalten, wenn mehr als ein enthaltenes Fenster enthalten ist. Es gibt drei Methoden, die von einer Explorer-Leiste implementiert werden müssen.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer ruft [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) auf, um die Explorer-Leiste darüber zu informieren, dass sie aktiviert oder deaktiviert wird. Bei Aktivierung ruft das Beispiel für die Explorer-Leiste [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) auf, um den Fokus auf das Fenster festzulegen.

Internet Explorer ruft [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) auf, wenn versucht wird, zu bestimmen, welches Fenster den Fokus besitzt. Wenn das Fenster der Explorer-Leiste oder eines seiner Nachfolger den Fokus hat, sollte **HasFocusIO** S \_ OK zurückgeben. Falls nicht, sollte S FALSE zurückgegeben \_ werden.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) ermöglicht dem Objekt die Verarbeitung von Tastaturbeschleunigungen. Im Explorer-Balkenbeispiel wird diese Methode nicht implementiert, daher wird S \_ FALSE zurückgegeben.

Die Implementierung von [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) in der Beispielleiste sieht wie folgt aus.


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>CLSID-Registrierung

Wie bei allen COM-Objekten muss die CLSID der Explorer-Leiste registriert werden. Damit das Objekt ordnungsgemäß mit Internet Explorer funktioniert, muss es auch für die entsprechende Komponentenkategorie (CATID \_ InfoBand) registriert werden. Der entsprechende Codeabschnitt für die Explorer-Leiste wird im folgenden Codebeispiel gezeigt.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



Die Registrierung von Bandobjekten im Beispiel verwendet normale COM-Prozeduren.

Zusätzlich zur CLSID muss der Bandobjektserver auch für eine oder mehrere Komponentenkategorien registriert werden. Dies ist tatsächlich der Hauptunterschied in der Implementierung zwischen den vertikalen und horizontalen Explorer-Balkenbeispielen. Dieser Prozess wird behandelt, indem ein Komponentenkategorien-Manager-Objekt (CLSID \_ StdComponentCategoriesMgr) erstellt und die [**ICatRegister::RegisterClassImplCategories-Methode**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) verwendet wird, um den Bandobjektserver zu registrieren. In diesem Beispiel wird die Registrierung der Komponentenkategorie verarbeitet, indem die CLSID und CATID des Explorer-Balkenbeispiels an eine private Funktion (**RegisterComCat)** übergeben werden, wie im folgenden Codebeispiel gezeigt.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>Die Fensterprozedur

Da ein Bandobjekt ein untergeordnetes Fenster für seine Anzeige verwendet, muss es eine Fensterprozedur implementieren, um Windows Messaging zu verarbeiten. Das Bandbeispiel verfügt über minimale Funktionalität, sodass die Fensterprozedur nur fünf Nachrichten verarbeitet:

-   [**WM \_ NCCREATE**](../winmsg/wm-nccreate.md)
-   [**WM \_ PAINT**](../gdi/wm-paint.md)
-   [**\_WM-BEFEHL**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**WM \_ KILLFOCUS**](../inputdev/wm-killfocus.md)

Das Verfahren kann problemlos erweitert werden, um zusätzliche Nachrichten aufzunehmen, um weitere Features zu unterstützen.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



Der WM \_ COMMAND-Handler gibt einfach 0 (null) zurück. Der WM \_ PAINT-Handler erstellt die einfache Textanzeige, die im Beispiel der Explorer-Leiste in der Einführung gezeigt wird.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



Die WM \_ SETFOCUS- und WM \_ KILLFOCUS-Handler informieren die Website über eine Fokusänderung, indem sie die [**IInputObjectSite::OnFocusChangeIS-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) der Website aufrufen.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Bandobjekte bieten eine flexible und leistungsstarke Möglichkeit, die Funktionen von Internet Explorer zu erweitern, indem sie benutzerdefinierte Explorer-Balken erstellen. Durch die Implementierung einer Deskband können Sie die Funktionen von normalen Fenstern erweitern. Obwohl eine COM-Programmierung erforderlich ist, dient sie letztendlich dazu, ein untergeordnetes Fenster für Ihre Benutzeroberfläche bereitzustellen. Von dort aus kann der Großteil der Implementierung vertraute Windows Programmiertechniken verwenden. Obwohl das hier beschriebene Beispiel nur eingeschränkte Funktionen aufweist, veranschaulicht es alle erforderlichen Features eines Bandobjekts und kann leicht erweitert werden, um eine eindeutige und leistungsfähige Benutzeroberfläche zu erstellen.

 

 
