---
description: Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4,0 eingeführt, um einen Anzeigebereich neben dem Browserbereich bereitzustellen.
title: Erstellen von benutzerdefinierten Explorer-Leisten, Tool-Bändern und Desk-Bändern
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104571323"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Erstellen von benutzerdefinierten Explorer-leisten, Toolbands und Desk-Bändern

Die Explorer-Leiste wurde mit Microsoft Internet Explorer 4,0 eingeführt, um einen Anzeigebereich neben dem Browserbereich bereitzustellen. Es handelt sich im Grunde um ein untergeordnetes Fenster innerhalb des Windows Internet Explorer-Fensters, das zum Anzeigen von Informationen und zum interagieren mit dem Benutzer auf die gleiche Weise verwendet werden kann. Explorer-Balken werden am häufigsten als vertikaler Bereich auf der linken Seite des Browser Bereichs angezeigt. Eine Explorer-Leiste kann jedoch auch horizontal unter dem Browserbereich angezeigt werden.

![Screenshot, in dem die vertikalen und horizontalen Explorer-Leisten angezeigt werden.](images/expl1.jpg)

Es gibt eine breite Palette möglicher Verwendungsmöglichkeiten für die Explorer-Leiste. Benutzer können auf verschiedene Arten auswählen, welche Option angezeigt werden soll. Sie können Sie auch im Untermenü der **Explorer-Leiste** des Menüs **Ansicht** auswählen oder auf eine Symbolleisten Schaltfläche klicken. Internet Explorer bietet einige Standard-Explorer-leisten, einschließlich Favoriten und suchen.

Eine der Möglichkeiten, wie Sie Internet Explorer anpassen können, besteht darin, eine benutzerdefinierte Explorer-Leiste hinzuzufügen. Wenn Sie implementiert und registriert ist, wird Sie dem Untermenü der **Explorer-Leiste** im Menü **Ansicht** hinzugefügt. Wenn Sie vom Benutzer ausgewählt wird, kann der Anzeigebereich der Explorer-Leiste verwendet werden, um Informationen anzuzeigen und die Benutzereingaben auf die gleiche Weise wie ein normales Fenster zu übernehmen.

![Screenshot der Explorer-leisten](images/expl2.jpg)

Um eine benutzerdefinierte Explorer-Leiste zu erstellen, müssen Sie ein *Band Objekt* implementieren und registrieren. Band Objekte wurden mit Version 4,71 der Shell eingeführt und bieten ähnliche Funktionen wie normale Fenster. Da es sich jedoch um Component Object Model (com)-Objekte handelt, die entweder in Internet Explorer oder in der Shell enthalten sind, werden Sie etwas anders implementiert. Einfache Band Objekte wurden verwendet, um die Beispiel-Explorer-leisten zu erstellen, die in der ersten Grafik angezeigt werden. Die Implementierung des Beispiels für die vertikale Explorer-Leiste wird in einem späteren Abschnitt ausführlich erläutert.

## <a name="tool-bands"></a>Tool Bänder

Ein *Toolband* ist ein Band Objekt, das mit Microsoft Internet Explorer 5 eingeführt wurde, um die Windows Radio Toolbar-Funktion zu unterstützen. Die Internet Explorer-Symbolleiste ist tatsächlich ein Grund leisten-Steuerelement, das mehrere Toolbar- [Steuer](../controls/rebar-controls.md) [Elemente](../controls/toolbar-control-reference.md)enthält. Wenn Sie ein Toolband erstellen, können Sie ein Band zu diesem Grund leisten-Steuerelement hinzufügen. Ähnlich wie Explorer-Balken ist ein Toolband jedoch ein allgemeines Fenster.

![Screenshot der Tool Bänder](images/toolband1.jpg)

Benutzer zeigen eine Symbolleiste an, indem Sie Sie im Untermenü "Symbolleisten" des Menüs **Ansicht** oder im Kontextmenü auswählen, das angezeigt wird, indem Sie mit der rechten Maustaste auf den Symbol **leisten** Bereich klicken.

## <a name="desk-bands"></a>Desk-Bänder

Mithilfe von Band Objekten können auch Desk- *Bänder* erstellt werden. Während die grundlegende Implementierung von Explorer-leisten vergleichbar ist, sind die Desk-Bänder nicht mit Internet Explorer verknüpft. Ein Desk-Band ist im Grunde genommen eine Möglichkeit, ein Andock bares Fenster auf dem Desktop zu erstellen. Der Benutzer wählt ihn aus, indem er mit der rechten Maustaste auf die Taskleiste klickt und ihn aus dem Untermenü **Symbolleisten** auswählt.

![Screenshot, der ein Beispiel für einen Desk-Band anzeigt.](images/desk2.png)

Anfänglich werden die Desk-Bänder auf der Taskleiste angedockt.

![Screenshot, in dem die in der Taskleiste angedockten Desk-Bänder angezeigt werden.](images/desk1.jpg)

Der Benutzer kann dann das Desk-Band auf den Desktop ziehen und als normales Fenster angezeigt werden.

![Screenshot der Desk-Bänder](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementieren von Band Objekten

Die folgenden Themen werden erörtert.

-   [Grundlagen zu Band Objekten](#band-object-basics)
-   [Band Registrierung](#band-registration)
-   [Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Grundlagen zu Band Objekten

Obwohl Sie ähnlich wie normale Fenster verwendet werden können, handelt es sich bei Band Objekten um COM-Objekte, die in einem Container vorhanden sind. Explorer-Balken sind in Internet Explorer enthalten, und Desk-Bänder sind in der Shell enthalten. Obwohl Sie unterschiedliche Funktionen bedienen, ist Ihre grundlegende Implementierung sehr ähnlich. Der Hauptunterschied besteht darin, wie das Band Objekt registriert wird, das wiederum den Objekttyp und den zugehörigen Container steuert. In diesem Abschnitt werden die Aspekte der Implementierung erläutert, die allen Band Objekten gemeinsam sind. Weitere Implementierungsdetails finden Sie [in einem einfachen Beispiel für eine benutzerdefinierte Explorer-Leiste](#a-simple-example-of-a-custom-explorer-bar) .

Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) und [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)müssen alle Band Objekte die folgenden Schnittstellen implementieren.

-   [**Ideskband**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Zusätzlich zum Registrieren Ihres Klassen Bezeichners (CLSID) müssen die Explorer-Leiste und die Desk-Band-Objekte auch für die entsprechende Komponenten Kategorie registriert werden. Beim Registrieren der Komponenten Kategorie wird der Objekttyp und der zugehörige Container bestimmt. Toolbänder verwenden eine andere Registrierungs Prozedur und verfügen nicht über einen Kategoriebezeichner (CATID). Die CATIDs für die drei-Band-Objekte, die Sie benötigen, sind:



| Bandtyp               | Komponentenkategorie |
|-------------------------|--------------------|
| Vertikale Explorer-Leiste   | CATID- \_ Infoband    |
| Horizontale Explorer-Leiste | CATID- \_ Kommas    |
| Desk-Band               | CATID \_ Desktop    |



 

Weitere Informationen zum Registrieren von Band Objekten finden Sie unter [Band Registrierung](#band-registration) .

Wenn das Band Objekt Benutzereingaben akzeptieren soll, muss auch [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)implementiert werden. Zum Hinzufügen von Elementen zum Kontextmenü für Explorer-oder-Desk-Bänder muss das Band Objekt [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)exportieren. Tool Bänder unterstützen keine Kontextmenüs.

Da ein untergeordnetes Fenster von Band Objekten implementiert wird, müssen Sie auch eine Fenster Prozedur zum Verarbeiten von Windows-Messaging implementieren.

Band Objekte können über die [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) -Schnittstelle des Containers Befehle an ihren Container senden. Um den Schnittstellen Zeiger zu erhalten, rufen Sie die [**iinputobjectsite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode des Containers auf, und Fragen Sie IID \_ IOleCommandTarget. Anschließend senden Sie mit [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec)Befehle an den Container. Die Befehlsgruppe ist "cgid \_ Deskband". Wenn die [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) -Methode eines Band Objekts aufgerufen wird, verwendet der Container den *dwbandid* -Parameter, um dem Band Objekt einen Bezeichner zuzuweisen, der für drei der Befehle verwendet wird. Vier **IOleCommandTarget:: exec** -Befehls-IDs werden unterstützt.

-   DBID \_ bandinfochanged

    Die Informationen des Bands wurden geändert. Legen Sie den *pvaIn* -Parameter auf den Bezeichner des Bands fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde. Der Container Ruft die **ideskband:: GetBandInfo** -Methode des Band Objekts auf, um die aktualisierten Informationen anzufordern.

-   DBID \_ maximizeband

    Maximieren Sie das Band. Legen Sie den *pvaIn* -Parameter auf den Bezeichner des Bands fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde.

-   DBID \_ showonly

    Schalten Sie andere Bänder im Container ein oder aus. Legen Sie den *pvaIn* -Parameter auf den unbekannten VT- \_ Typ mit einem der folgenden Werte fest:

    

    | Wert | BESCHREIBUNG                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | Kro  | Ein Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Band Objekts. Alle anderen Desk-Bänder werden ausgeblendet. |
    | 0     | Alle Desk-Bänder ausblenden.                                                                                        |
    | 1     | Alle Desk-Bänder anzeigen.                                                                                        |

    

     

-   DBID- \_ pushchevron

    [Version 5](versions.md). Zeigen Sie ein Chevron-Menü an. Der Container sendet eine [**RB- \_ pushchevron**](../controls/rb-pushchevron.md) -Nachricht, und das Band Objekt empfängt eine [RBN \_ chevronpush](../controls/rbn-chevronpushed.md) -Benachrichtigung, die ihn auffordert, das Chevron-Menü anzuzeigen. Legen Sie den *nCmdexecopt* -Parameter der [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) -Methode auf den Band Bezeichner fest, der beim letzten Aufruf von [**ideskband:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)empfangen wurde. Legen Sie den *pvaIn* -Parameter der **IOleCommandTarget:: exec** -Methode auf den VT \_ I4-Typ mit einem von der Anwendung definierten Wert fest. Es wird als Wert des *lappvalue* der RBN-chevronpushbenachrichtigung an das Band Objekt übergeben \_ .

### <a name="band-registration"></a>Band Registrierung

Ein Band Objekt muss als OLE-Prozess interner Server registriert werden, der das Apartment Threading unterstützt. Der Standardwert für den Server ist eine Menü Text Zeichenfolge. Bei Explorer-leisten wird diese im Untermenü der **Explorer-Leiste** im Internet Explorer- **Ansichts** Menü angezeigt. Für Tool Bänder wird es im Menü " **Symbolleisten** " im Menü " **Ansicht** " von Internet Explorer angezeigt. Für Desk-Bänder wird Sie im Untermenü **Symbolleisten** des Kontextmenüs der Taskleiste angezeigt. Wie bei Menü Ressourcen führt das Platzieren eines kaufmännischen und-Zeichens (&) vor einem Buchstaben zu unterstrichen und ermöglicht Tastenkombinationen. Beispielsweise ist die Menü Zeichenfolge für die vertikale Explorer-Leiste, die in der ersten Grafik angezeigt wird, "Sample &Vertical Explorer Bar".

Zunächst ruft Internet Explorer mithilfe der Komponenten Kategorien eine Enumeration der registrierten Explorer-Balken Objekte aus der Registrierung ab. Um die Leistung zu verbessern, wird diese Enumeration zwischengespeichert, sodass anschließend die hinzugefügten Explorer-leisten übersehen werden. Wenn Sie erzwingen möchten, dass Windows Internet Explorer den Cache neu erstellt und eine neue Explorer-Leiste erkennt, löschen Sie die folgenden Registrierungsschlüssel während der Registrierung der neuen Explorer-Leiste:

**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **verwerfbare** \\ **postsetup**- \\ **Komponenten Kategorien** \\ **{00021493-0000-0000-C000-000000000046}-Aufzählung** \\ 

**HKEY \_ Aktuelle \_ Benutzer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **verwerfbare** \\ **postsetup**- \\ **Komponenten Kategorien** \\ **{00021494-0000-0000-C000-000000000046}-Aufzählung** \\ 

> [!Note]  
> Da für jeden Benutzer ein Explorer-leisten Cache erstellt wird, muss Ihre Setup Anwendung möglicherweise alle Benutzer Registrierungs Strukturen auflisten oder einen Stub pro Benutzer hinzufügen, der ausgeführt wird, wenn sich der Benutzer zum ersten Mal anmeldet.

 

Im Allgemeinen wird der grundlegende Registrierungs Eintrag für ein Band Objekt folgendermaßen angezeigt.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Bei Toolbands muss auch die CLSID Ihres Objekts bei Internet Explorer registriert sein. Weisen Sie zu diesem Zweck einen Wert unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Toolbar** mit dem Namen der CLSID-GUID des toolbandobjekts zu, wie hier gezeigt. Der Datenwert wird ignoriert, sodass der Werttyp unwichtig ist.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Es gibt mehrere optionale Werte, die auch der Registrierung hinzugefügt werden können. Der folgende Wert ist z. b. erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten. der angezeigte Wert ist kein Beispiel, sondern der tatsächliche Wert, der verwendet werden soll.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Wenn Sie in Verbindung mit dem oben gezeigten Wert verwendet werden, ist auch der folgende optionale Wert erforderlich, wenn Sie die Explorer-Leiste zum Anzeigen von HTML verwenden möchten. Dieser Wert sollte auf den Speicherort der Datei festgelegt werden, die den HTML-Inhalt für die Explorer-Leiste enthält.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Ein weiterer Optionaler Wert definiert die Standardbreite oder Höhe der Explorer-Leiste, je nachdem, ob es sich um vertikal bzw. horizontal handelt.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

Der barsize-Wert muss auf die Breite oder Höhe des Balkens festgelegt werden. Der Wert erfordert acht Bytes und wird in der Registrierung als binärer Wert abgelegt. Die ersten vier Bytes geben die Größe im Hexadezimal Format in Pixel an, beginnend ab dem äußersten linken Byte. Die letzten vier Bytes sind reserviert und sollten auf 0 (null) festgelegt werden.

Beispielsweise werden hier die vollständigen Registrierungseinträge für eine HTML-fähige Explorer-Leiste mit einer Standardbreite von 291 (0x123) Pixel angezeigt.

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

Die Registrierung der CATID eines Band Objekts kann Programm gesteuert behandelt werden. Erstellen Sie ein Komponenten Kategorien-Manager-Objekt (CLSID \_ stdcomponentcategoriesmgr), und fordern Sie einen Zeiger auf seine [**ikatregister**](/windows/win32/api/comcat/nn-comcat-icatregister) -Schnittstelle an. Übergeben Sie die CLSID und die CATID des Band Objekts an [**iskiregister:: registerclassimplcategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Ein einfaches Beispiel für eine benutzerdefinierte Explorer-Leiste

Dieses Beispiel durchläuft die Implementierung der vertikalen Beispiel-Explorer-Leiste, die in der Einführung gezeigt wird.

Das grundlegende Verfahren zum Erstellen einer benutzerdefinierten Explorer-Leiste sieht wie folgt aus.

1.  [Implementieren Sie die Funktionen, die von der DLL benötigt werden](#dll-functions).
2.  [Implementieren Sie die erforderlichen COM-Schnittstellen.](#required-interface-implementations)
3.  [Implementieren Sie alle gewünschten optionalen com-Schnittstellen.](#optional-interface-implementations)
4.  [Registrieren Sie die CLSID des Objekts und ggf. die Komponenten Kategorie.](#clsid-registration)
5.  Erstellen Sie ein untergeordnetes Fenster von Internet Explorer, dessen Größenanpassung an den Anzeigebereich der Explorer-Leiste angepasst ist.
6.  [Verwenden Sie das untergeordnete Fenster, um Informationen anzuzeigen und mit dem Benutzer zu interagieren.](#the-window-procedure)

Die sehr einfache Implementierung, die im Explorer-leisten Beispiel verwendet wird, kann tatsächlich für den Typ der Explorer-Leiste oder einen Desk-Band verwendet werden, indem Sie Sie einfach für die entsprechende Komponenten Kategorie registrieren. Anspruchsvollere Implementierungen müssen für den Anzeigebereich und Container jedes Objekt Typs angepasst werden. Allerdings kann ein Großteil dieser Anpassung erreicht werden, indem der Beispielcode übernommen und erweitert wird, indem vertraute Windows-Programmiertechniken auf das untergeordnete Fenster angewendet werden. Beispielsweise können Sie Steuerelemente für Benutzerinteraktion oder Grafiken hinzufügen, um eine umfassendere Anzeige zu erhalten.

### <a name="dll-functions"></a>DLL-Funktionen

Alle drei Objekte werden in einer einzelnen DLL verpackt, die die folgenden Funktionen verfügbar macht.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Die ersten drei Funktionen sind Standard Implementierungen und werden hier nicht erläutert. Die Klassenfactoryimplementierung ist auch Standard.

### <a name="required-interface-implementations"></a>Erforderliche Schnittstellen Implementierungen

Das Beispiel für die vertikale Explorer-Leiste implementiert die vier erforderlichen Schnittstellen: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)und [**ideskband**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) als Teil der cexplorerbar-Klasse. Die Implementierungen Konstruktor, Dekonstruktor und **IUnknown** sind unkompliziert und werden hier nicht erläutert. Sehen Sie sich den Beispielcode an, um ausführliche Informationen zu erhalten.

Die folgenden Schnittstellen werden ausführlich erläutert.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [Ideskband](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Wenn der Benutzer eine Explorer-Leiste auswählt, ruft der Container die [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) -Methode des entsprechenden Band Objekts auf. Der Parameter " *pUnkSite* " wird auf den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger der Site festgelegt.

Im Allgemeinen sollte eine [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) -Implementierung die folgenden Schritte ausführen:

1.  Geben Sie einen beliebigen Website Zeiger frei, der derzeit aufbewahrt wird.
2.  Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) über gegebene Zeiger auf **null** festgelegt ist, wird das Band entfernt. **SetSite** kann S OK zurückgeben \_ .
3.  Wenn der an [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) über gegebene Zeiger nicht **null** ist, wird eine neue Site festgelegt. **SetSite** sollte folgende Aktionen ausführen:
    1.  Ruft [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf der Site für die [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) -Schnittstelle auf.
    2.  Rufen Sie [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) auf, um das Handle des übergeordneten Fensters zu erhalten. Speichern Sie das Handle für die spätere Verwendung. Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , wenn es nicht mehr benötigt wird.
    3.  Erstellen Sie das Fenster des Band Objekts als untergeordnetes Element des Fensters, das Sie im vorherigen Schritt abgerufen haben. Erstellen Sie Sie nicht als sichtbares Fenster.
    4.  Wenn das Band Objekt [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)implementiert, nennen Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) -Schnittstelle auf der Website. Speichern Sie den Zeiger auf diese Schnittstelle, um Sie später zu verwenden.
    5.  Wenn alle Schritte erfolgreich sind, geben Sie S \_ OK zurück. Andernfalls wird der OLE-definierte Fehlercode zurückgegeben, der den Fehler angibt.

Das Beispiel für eine Explorer-Leiste implementiert [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) auf folgende Weise. Im folgenden Code ist " *m \_ psite* " eine private Member-Variable, die den [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) -Zeiger enthält und *m \_ hwndParent* das Handle des übergeordneten Fensters enthält. In diesem Beispiel wird auch die Fenster Erstellung behandelt. Wenn das Fenster nicht vorhanden ist, erstellt diese Methode das Fenster der Explorer-Leiste als untergeordnetes Element des übergeordneten Fensters, das von **SetSite** abgerufen wird. Das Handle des untergeordneten Fensters wird in *m \_ HWND* gespeichert.


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



Die [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) -Implementierung des Beispiels umschließt einfach einen Aufrufen der [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode der Site und verwendet dabei den von [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)gespeicherten Website Zeiger.


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



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer Ruft die [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle der Explorer-Leiste auf, damit die Explorer-Leiste persistente Daten laden oder speichern kann. Wenn keine persistenten Daten vorhanden sind, müssen die Methoden weiterhin einen Erfolgs Code zurückgeben. Die **IPersistStream** -Schnittstelle erbt von [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist), sodass fünf Methoden implementiert werden müssen.

-   [**Ipersistent:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream:: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream:: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream:: GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

Im Beispiel für eine Explorer-Leiste werden keine persistenten Daten verwendet, und es ist nur eine minimale Implementierung von [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)vorhanden. [**Ipersistent:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) gibt die CLSID des Objekts (CLSID \_ sampleexplor\) zurück, und der Rest gibt entweder s \_ OK, s \_ false oder E \_ notimpl zurück.

### <a name="ideskband"></a>Ideskband

Die [**ideskband**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) -Schnittstelle ist spezifisch für Band Objekte. Zusätzlich zu seiner einzigen Methode erbt sie von [**idockingwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), das wiederum von [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)erbt.

Es gibt zwei [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) -Methoden: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) und [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). Die Implementierung von **GetWindow** in der Explorer-Leiste gibt das untergeordnete Fenster Handle der Explorer-Leiste ( *m \_ HWND*) zurück. Die kontextbezogene Hilfe ist nicht implementiert, sodass **ContextSensitiveHelp** **E \_ notimpl** zurückgibt.

Die [**idockingwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) -Schnittstelle verfügt über drei Methoden.

-   [**Idockingwindow:: showdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**Idockingwindow:: closedw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**Idockingwindow:: resizeborderdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

Die [**resizeborderdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) -Methode wird nicht mit einem beliebigen Typ von Band Objekt verwendet und sollte immer E \_ notimpl zurückgeben. Die [**showdw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) -Methode zeigt das Fenster der Explorer-Leiste an oder blendet es aus, abhängig vom Wert des Parameters.


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



Die [**closedw**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) -Methode zerstört das Fenster der Explorer-Leiste.


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



Die verbleibende Methode [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)ist für **ideskband** spezifisch. Internet Explorer verwendet es, um den Bezeichner und den Anzeigemodus der Explorer-Leiste anzugeben. Internet Explorer kann auch eine oder mehrere Informationen von der Explorer-Leiste anfordern, indem er den **dwMask** -Member der [**deskbandinfo**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) -Struktur ausfüllt, der als dritter Parameter übergeben wird. **GetBandInfo** sollte den Bezeichner und den Anzeigemodus speichern und die **deskbandinfo** -Struktur mit den angeforderten Daten ausfüllen. Das Beispiel für eine Explorer-Leiste implementiert **GetBandInfo** , wie im folgenden Codebeispiel gezeigt.


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



### <a name="optional-interface-implementations"></a>Optionale Schnittstellen Implementierungen

Es gibt zwei Schnittstellen, die nicht erforderlich sind. Dies kann jedoch nützlich sein, um Folgendes zu implementieren: [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Das Beispiel für eine Explorer-Leiste implementiert **iinputobject**. Informationen zum Implementieren von **IContextMenu** finden Sie in der Dokumentation.

### <a name="iinputobject"></a>Iinputobject

Die [**iinputobject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) -Schnittstelle muss implementiert werden, wenn ein Band Objekt Benutzereingaben akzeptiert. Internet Explorer implementiert [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) und verwendet **iinputobject** , um den richtigen Benutzereingabe Fokus zu erhalten, wenn es mehr als ein eigenständiges Fenster hat. Es gibt drei Methoden, die von einer Explorer-Leiste implementiert werden müssen.

-   [**Iinputobject:: uiactivateio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**Iinputobject:: hasfocusio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**Iinputobject:: translateacceleratorio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer ruft [**uiactivateio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) auf, um der Explorer-Leiste mitzuteilen, dass Sie aktiviert oder deaktiviert wird. Wenn diese aktiviert ist, ruft das Explorer-Balken Beispiel [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) auf, um den Fokus auf das Fenster festzulegen.

Internet Explorer ruft [**hasfocusio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) auf, wenn versucht wird, zu bestimmen, welches Fenster den Fokus besitzt. Wenn das Fenster der Explorer-Leiste oder einer der untergeordneten Elemente den Fokus besitzt, sollte **hasfocusio** den Wert s OK zurückgeben \_ . Wenn dies nicht der Fall ist, sollte der Wert S false zurückgeben \_

[**Translateacceleratorio**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) ermöglicht dem Objekt die Verarbeitung von Tastatur Accelerators. Das Beispiel für eine Explorer-Leiste implementiert diese Methode nicht, daher gibt es "false" zurück \_ .

Die Implementierung von [**iinputobjectsite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) in der Beispiel Leiste sieht wie folgt aus.


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

Wie bei allen COM-Objekten muss die CLSID der Explorer-Leiste registriert werden. Damit das-Objekt ordnungsgemäß mit Internet Explorer funktioniert, muss es auch für die entsprechende Komponenten Kategorie (CATID \_ Infoband) registriert werden. Der relevante Code Abschnitt für die Explorer-Leiste wird im folgenden Codebeispiel gezeigt.


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



Bei der Registrierung von Band Objekten im Beispiel werden normale com-Prozeduren verwendet.

Zusätzlich zur CLSID muss der-Band Objekt Server auch für eine oder mehrere Komponenten Kategorien registriert werden. Dies ist der Hauptunterschied in der Implementierung zwischen vertikalen und horizontalen Explorer-Balken Beispielen. Dieser Prozess wird durch das Erstellen eines Komponenten Kategorien-Manager-Objekts (CLSID \_ stdcomponentcategoriesmgr) und das Verwenden der [**icatregister:: registerclassimplcategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) -Methode zum Registrieren des Band Objekt Servers behandelt. In diesem Beispiel wird die Registrierung der Komponenten Kategorie behandelt, indem die CLSID und die CATID des Explorer-Balken Beispiels an eine private Funktion –**registercomcat**– übergeben werden, wie im folgenden Codebeispiel gezeigt.


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



### <a name="the-window-procedure"></a>Die Fenster Prozedur

Da ein Band Objekt ein untergeordnetes Fenster für seine Anzeige verwendet, muss es eine Fenster Prozedur zum Verarbeiten von Windows-Messaging implementieren. Das Band Beispiel verfügt über minimale Funktionalität, sodass die Fenster Prozedur nur fünf Nachrichten verarbeitet:

-   [**WM- \_ nccreate**](../winmsg/wm-nccreate.md)
-   [**WM- \_ Paint**](../gdi/wm-paint.md)
-   [**WM- \_ Befehl**](../menurc/wm-command.md)
-   [**WM- \_ SetFocus**](../inputdev/wm-setfocus.md)
-   [**WM- \_ killfokus**](../inputdev/wm-killfocus.md)

Die Prozedur kann problemlos erweitert werden, um weitere Nachrichten zur Unterstützung weiterer Funktionen zu bieten.


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



Der WM- \_ Befehls Handler gibt einfach NULL zurück. Der WM-Zeichnungs \_ Handler erstellt die einfache Textanzeige, die im Beispiel der Explorer-Leiste in der Einführung angezeigt wird.


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



Die "WM \_ SetFocus"-und "WM \_ killfocus"-Handler informieren die Website über eine Fokus Änderung, indem Sie die [**iinputobjectsite:: onfocuschangeis**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) -Methode der Site aufrufen.


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



Band Objekte bieten eine flexible und leistungsstarke Möglichkeit, die Funktionen von Internet Explorer zu erweitern, indem benutzerdefinierte Explorer-leisten erstellt werden. Durch die Implementierung eines Desk-Bands können Sie die Funktionen von normalen Fenstern erweitern. Obwohl einige COM-Programmierung erforderlich ist, ist es letztendlich, ein untergeordnetes Fenster für Ihre Benutzeroberfläche bereitzustellen. Von dort aus kann der Großteil der Implementierung vertraute Windows-Programmiertechniken verwenden. Das hier beschriebene Beispiel verfügt zwar nur über eingeschränkte Funktionalität, veranschaulicht aber alle notwendigen Features eines Band Objekts und kann problemlos erweitert werden, um eine eindeutige und leistungsstarke Benutzeroberfläche zu erstellen.

 

 
