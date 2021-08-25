---
description: In Windows Vista integriert der Tablet PC-Eingabebereich neue AutoVervollständigen-Funktionen, mit denen die AutoVervollständigen-Liste einer Anwendung in Echtzeit aktualisiert werden kann, wenn die Ink-Funktion eines Benutzers im Eingabebereich erkannt wird.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Verwenden der AutoVervollständigen-Funktion des Eingabebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb0589cca00a45d007c7df6a605f051161c07a62c864504780c307693fe8897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934379"
---
# <a name="using-input-panel-autocomplete"></a>Verwenden der AutoVervollständigen-Funktion des Eingabebereichs

In Windows Vista integriert der Tablet PC-Eingabebereich neue AutoVervollständigen-Funktionen, mit denen die AutoVervollständigen-Liste einer Anwendung in Echtzeit aktualisiert werden kann, wenn die Ink-Funktion eines Benutzers im Eingabebereich erkannt wird. Darüber hinaus befindet sich die AutoVervollständigen-Liste der Anwendung an einem geeigneten Ort für Benutzer des Eingabebereichs. Ohne automatische Vervollständigung des Eingabebereichs ist die Verwendung von AutoVervollständigen-Features mit dem Eingabebereich ein schwieriger Prozess, bei dem Benutzer ein Zeichen nach dem anderen einfügen und den Eingabebereich verschieben müssen, um auf AutoVervollständigen-Vorschläge zu zugreifen. Mit der Integration ist AutoVervollständigen ein leistungsstarkes Tool für Tablet PC-Benutzer, das die Eingabe von Text im Eingabebereich beschleunigt und vereinfacht.

![Eingabebereich mit Der AutoVervollständigen-Liste](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Es gibt drei Optionen, wie eine Anwendung die Automatische Vervollständigungsintegration des Eingabebereichs nutzen kann. Anwendungen, die AutoVervollständigen-Funktionen enthalten, die mit shell autocomplete (über die [**IAutoComplete-Schnittstelle)**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) oder .NET Framework AutoVervollständigen (über die [AutoCompleteMode-Enumeration)](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) erstellt wurden, erhalten die AutoVervollständigen-Integration des Eingabebereichs ohne Codeänderungen. Anwendungen, die benutzerdefinierte Textfelder für die automatische Vervollständigung enthalten, können die Automatische Vervollständigungs-API des Eingabebereichs verwenden, um die gleiche Funktionalität zu erhalten.

In allen Fällen können Sie diese Änderungen an der AutoVervollständigen-Liste der Anwendung vorgenommen, ohne die Benutzeroberfläche oder Vorhersagelogik zu duplizieren oder zu ändern, die von einer Anwendung zum Generieren einer AutoVervollständigen-Liste verwendet wird. Die AutoVervollständigen-Liste ist weiterhin Besitzer, der von der Anwendung gezeichnet wird, und der Inhalt der AutoVervollständigen-Liste ist identisch mit dem Text, der direkt in das Bearbeitungsfeld eingefügt wurde.

Die Integration der automatischen Vervollständigung des Eingabebereichs wird auf dem Windows Vista-Betriebssystem oder in neueren Versionen unterstützt. Die Integration der automatischen Vervollständigung des Eingabebereichs ist ab Windows Vista in shell autocomplete und ab .NET Framework Version 3.0 in die Windows Forms-Entwicklung integriert. Während [**IAutoComplete und**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) beide unter früheren Versionen von Windows ausgeführt werden, wird die Integration der automatischen Vervollständigung des Eingabebereichs unter Microsoft Windows XP Tablet PC Edition oder früheren Betriebssystemen nicht unterstützt. Wenn Sie die automatische Vervollständigung des Eingabebereichs auf früheren Versionen des Tablet-PCs ausführen, werden Anwendungen auf das Verhalten vor der Integration zurückversetzt.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Gründe für die Integration von Listen zur automatischen Vervollständigung von Anwendungen in den Eingabebereich

Die Integration der AutoVervollständigen-Liste einer Anwendung ermöglicht benutzern, die Text in ein Textfeld eingeben, das autovervollständigen-Funktionen enthält, die maximale Einfachheit und Geschwindigkeit der Eingabe. Darüber hinaus wird eine Anwendung, die die Integration der automatischen Vervollständigung des Eingabebereichs enthält, sofort so angezeigt, als ob sie mit dem Tablet PC entwickelt wurde, wodurch die Anwendung für Tablet PC-Benutzer ansprechender wird.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Interaktion zwischen Eingabebereich und AutoVervollständigen-Liste ohne Integration

Verwenden des Eingabebereichs zum Eingeben von Text in ein Textfeld, das eine AutoVervollständigen-Liste enthält, aber nicht in den Eingabebereich integriert ist:

1.  Der Benutzer platziert den Fokus in das Textfeld und öffnet den Eingabebereich.
2.  Der Benutzer schreibt ein oder zwei Zeichen.
3.  Der Benutzer tippt auf **Einfügen.** Der Eingabebereich gibt den Text in das Textfeld der Anwendung ein. Die AutoVervollständigen-Liste der Anwendung wird angezeigt und wird wahrscheinlich teilweise oder vollständig durch den Eingabebereich verdeckt.
4.  Der Benutzer zieht den Eingabebereich, um die AutoVervollständigen-Liste der Anwendung zu entdecken.
5.  Angenommen, der richtige Eintrag ist in der AutoVervollständigen-Liste enthalten, kann der Benutzer diesen Eintrag jetzt auswählen. Andernfalls muss der Benutzer die Schritte 2 und 3 wiederholen.

Dies ist eindeutig ein umständlicher Prozess. Die Erwartungen des Benutzers an die Funktionsweise einer AutoVervollständigen-Liste sind gestrichelt, und die Fähigkeit des Benutzers, Aufgaben auszuführen, ist betroffen.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Verbesserung der Interaktion zwischen Eingabebereich und AutoVervollständigen-Liste mit Integration

Verwenden des Eingabebereichs zum Eingeben von Text in ein Textfeld, das eine AutoVervollständigen-Liste enthält, die in den Eingabebereich integriert ist:

1.  Der Benutzer platziert den Fokus in das Textfeld und öffnet den Eingabebereich.
2.  Der Benutzer schreibt ein oder zwei Zeichen. Die AutoVervollständigen-Liste der Anwendung wird direkt über oder direkt unterhalb des Eingabebereichs angezeigt, wenn der Benutzer Text schreibt.
3.  Der Benutzer wählt den Eintrag aus der AutoVervollständigen-Liste aus. Der Eintrag wird direkt in das Textfeld der Anwendung eingefügt, oder der Benutzer wiederholt Schritt 2, bis der richtige Eintrag angezeigt wird.

Aufgrund der Integration wird die Liste AutoVervollständigen angezeigt und aktualisiert, während der Benutzer im Eingabebereich schreibt. Darüber hinaus ist die Liste so positioniert, dass der Benutzer beim Schreiben bequem darauf zugreifen kann und nicht durch den Eingabebereich verdeckt wird. Wenn der Benutzer schließlich ein Element aus einer AutoVervollständigen-Liste auswählt, wird das Element direkt in das Texteingabefeld der Anwendung eingefügt, sodass der Benutzer den Schritt zum Einfügen von Text aus dem Eingabebereich umgehen kann.

![Eingabebereich mit Outlook Express AutoVervollständigen-Liste](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Standardmäßige AutoVervollständigen-Komponenten, die die Integration der automatischen Vervollständigung des Eingabebereichs enthalten

Sowohl [**IAutoComplete als**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) auch [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) enthalten eine integrierte Integration der AutoVervollständigen-Funktion des Eingabebereichs. Anwendungen, die eine dieser Standardkomponenten für die automatische Vervollständigung verwenden, können die Funktionen der automatischen Vervollständigung des Eingabebereichs mit wenig bis gar keiner zusätzlichen Arbeit nutzen. Während die automatische Vervollständigung des Eingabebereichs nur unter Windows Vista oder neuen Versionen des Windows-Betriebssystems unterstützt wird, erhalten Anwendungen, die vor der Veröffentlichung von Windows Vista mit **IAutoComplete** erstellt wurden, die automatische Vervollständigung des Eingabebereichs automatisch, wenn sie unter Windows Vista ausgeführt werden. Die folgenden Abschnitte enthalten weitere Informationen zu den spezifischen **IAutoComplete-** und AutoCompleteMode-Elementen, die die AutoVervollständigen-Integration des Eingabebereichs enthalten.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Automatische Vervollständigung der Shell mit AutoVervollständigen-Integration des Eingabebereichs

Anwendungen, die [**IAutoComplete verwenden,**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) erhalten die Automatische Vervollständigungsintegration im Eingabebereich kostenlos. Während die Shell-AUTOVERVOLLSTÄNDIGEN-APIs in Windows 2000 oder darüber enthalten sind, wird die Integration der automatischen Vervollständigung des Eingabebereichs nur unter Windows Vista und neueren Versionen unterstützt. Anwendungen, die vor der Veröffentlichung von Windows Vista erstellt wurden und **IAutoComplete** verwenden, erhalten jedoch automatisch die Automatische Vervollständigung des Eingabebereichs, wenn sie unter Windows Vista ausgeführt werden.

Um die Vorteile der automatischen Vervollständigung von Tablets auf diese Weise nutzen zu können, müssen Sie das AutoVervollständigen-Objekt **(CLSID \_ AutoVervollständigen) verwenden.** Wenn Sie AutoVervollständigen-Funktionen für URLs oder Dateinamen bereitstellen möchten, verwenden Sie die [**SHAutoComplete-Funktion,**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) um das AutoVervollständigen-Objekt zu erstellen.

Zusätzlich zu [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)können Sie [**IAutoComplete2-**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) oder [**IAutoCompleteDropDown-S**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)direkt implementieren und trotzdem die Automatische Vervollständigung des Eingabebereichs automatisch erhalten.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integration der automatischen Vervollständigung des Eingabebereichs in .NET Framework Anwendungen

Ab .NET Framework 3.0 enthalten Windows Formulartextfelder AutoVervollständigen. Windows Das Formulartextfeld AutoVervollständigen basiert auf der Shell AutoVervollständigen, was bedeutet, dass auch die AutoVervollständigen-Integration des Eingabebereichs integriert ist. .NET Framework 3.0 wird auf der downlevel-Ebene von Windows Editionen unterstützt, die vor Windows Vista veröffentlicht wurden. Da die Integration der automatischen Vervollständigung des Eingabebereichs jedoch nur unter Windows Vista oder höher unterstützt wird, funktioniert die Integration der automatischen Vervollständigung des Eingabebereichs nur in einer .NET Framework 3.0-Anwendung, wenn sie unter Windows Vista oder höher installiert wird.

Anwendungen, die die AutoVervollständigen-Integration des Eingabebereichs in .NET Framework 3.0 nutzen möchten, müssen ein Windows [Forms-TextFeld](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) mit aktivierter [AutoCompleteMode-Eigenschaft](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) verwenden. Sie müssen keine zusätzlichen Schritte unternehmen, als Windows Die automatische Vervollständigung von Formularen funktioniert, um die Vorteile der Integration der automatischen Vervollständigung des Eingabebereichs zu nutzen.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Direktes Verwenden von ApIs für die automatische Vervollständigung des Eingabebereichs

Entwickler benutzerdefinierter AutoVervollständigen-Textfelder müssen direkt mit den AutoVervollständigen-APIs des Eingabebereichs arbeiten, um die verbesserte Texteingabeerfahrung zu erhalten, die die Integration der automatischen Vervollständigung des Eingabebereichs in ihren Anwendungen ermöglicht. Die ApIs für die automatische Vervollständigung des Eingabebereichs sind als Teil des Betriebssystems Windows Vista und als Teil des Tablet Platform SDK, Version 1.9 oder höher, enthalten. Die AutoVervollständigen-Schnittstellen des Eingabebereichs sind COM-basierte Schnittstellen.

Im folgenden Abschnitt wird die detaillierte Arbeit dieser Schnittstellen für eine C++-Anwendung beschrieben. Diese COM-Schnittstellen können jedoch in den meisten Sprachen, einschließlich C, mithilfe \# von COM-Interop implementiert werden.

Um die Automatische Vervollständigung des Eingabebereichs in ein benutzerdefiniertes Textfeld autovervollständigen zu implementieren, sind die beiden erforderlichen Schnittstellen die [**ITipAutocompleteProvider-Schnittstelle**](itipautocompleteprovider.md) und die [**ITipAutocompleteClient-Schnittstelle.**](itipautocompleteclient.md) Die Definitionen für diese Schnittstellen befinden sich in TipAutoComplete.h und TipAutoComplete \_ i.c.

Zunächst muss eine Anwendung eine AutoVervollständigen-Anbieterklasse definieren und instanziieren, die [**ITipAutocompleteProvider**](itipautocompleteprovider.md) für jedes Texteingabefeld implementiert, das eine AutoVervollständigen-Liste enthält. Diese Klasse verwaltet die Anwendungsseite der AutoVervollständigen-Integration. Alle AutoVervollständigen-Anforderungen aus dem Eingabebereich werden vom AutoVervollständigen-Client über den AutoVervollständigen-Anbieter der Anwendung an die Anwendung übermittelt. Der AutoVervollständigen-Anbieter der Anwendung muss sowohl Zugriff auf das HWND für die AutoVervollständigen-Liste der Anwendung als auch auf den HWIND für das zugeordnete Texteingabefeld haben. Darüber hinaus müssen die folgenden Methoden von **ITipAutocompleteProvider** implementiert werden:

-   [**ITipAutocompleteProvider::UpdatePendingText-Methode:**](itipautocompleteprovider-updatependingtext.md)Diese Methode wird vom AutoVervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich geschrieben hat. Nach Dem Empfang dieser Benachrichtigung ist der Anbieter dafür verantwortlich, eine AutoVervollständigen-Liste zu generieren, als ob der Text in das Texteingabefeld der Anwendung eingefügt worden wäre. Die Zeichenfolge wird mit der **ITipAutocompleteProvider::UpdatePendingText-Methode** an den AutoVervollständigen-Anbieter übergeben und enthält nur den Text, der sich derzeit im Eingabebereich befindet. Wenn das Texteingabefeld zusätzlichen Text enthält, liegt es daher in der Verantwortung des Anbieters, ihn ordnungsgemäß an den vom Client gesendeten Text anfügen. Die Zeichenfolgenübergabe durch **die ITipAutocompleteProvider::UpdatePendingText-Methode** sollte als Ersatz für die aktuelle Auswahl im Feld behandelt werden. Wenn es keine aktuelle Auswahl gibt, sollte sie an der Position der aktuellen Einfügemarke platziert werden. Nachdem die AutoVervollständigen-Liste generiert wurde, sollte der Anbieter die [**ITipAutocompleteProvider::Show-Methode**](itipautocompleteprovider-show.md) aufrufen, die **TRUE** übergabe, um die AutoVervollständigen-Liste anzuzeigen. Die Anwendung sollte Aufrufe von **UpdatePendingText** nicht zwischenspeichern, sondern jeden zusätzlichen Aufruf von **UpdatePendingText** als Abbruch des vorherigen Aufrufs behandeln, um zu vermeiden, dass eine veraltete AutoVervollständigen-Listenbenutzeroberfläche blinkt. Im folgenden Beispielcode werden diese Vorgehensweisen veranschaulicht.

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**ITipAutocompleteProvider::Show-Methode:**](itipautocompleteprovider-show.md)Diese Methode wird von [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md)aufgerufen, kann aber auch jederzeit vom AutoVervollständigen-Client aufgerufen werden. Nach Dem Empfang dieses Aufrufs muss der AutoVervollständigen-Anbieter den AutoVervollständigen-Anbieter ausblenden oder anzeigen, wie durch den -Parameter angegeben. Vor der Anzeige der AutoVervollständigen-Liste wird vom AutoVervollständigen-Anbieter erwartet, dass er den AutoVervollständigen-Client darüber abspricht, wo die AutoVervollständigen-Liste positioniert werden soll. Weitere Informationen zum Positionieren der AutoVervollständigen-Liste finden Sie weiter oben in diesem Artikel.

Als Nächstes sollte die Anwendung die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) von Active Template Library (ATL) verwenden, um eine Instanz der [**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md) mit der Klassen-ID **CLSID \_ TipAutoCompleteClient** als Prozessserver zu erstellen und dann den Anbieter beim Client zu registrieren. Die [**ITipAutocompleteClient::AdviseProvider-Methode**](itipautocompleteclient-adviseprovider.md) des AutoVervollständigen-Clients registriert den Anbieter beim Client, damit der Client das AutoVervollständigen-Anbieterobjekt der Anwendung aufrufen kann. Wenn tiptsf.dll System nicht vorhanden ist, schlägt die **CoCreateInstance-Funktion** fehl und gibt **REGDB \_ E \_ CLASSNOTREG zurück.** An diesem Punkt kann die Anwendung ihr [**ITipAutocompleteProvider-Objekt**](itipautocompleteprovider.md) verwerfen und so fortfahren, als ob der Eingabebereich nicht vorhanden wäre, da er auf einem solchen System nicht vorhanden ist.

Die Anwendung kann eine Instanz von [**ITipAutocompleteClient**](itipautocompleteclient.md) oder eine Instanz pro Textfeld erstellen. Bei der ersten Option muss die Registrierung des Anbieters bei jeder Änderung des Fokus aufgehoben und registriert werden. Weitere Informationen zum Aufheben der Registrierung des AutoVervollständigen-Anbieters finden Sie weiter später in diesem Thema.

Es gibt mehrere Schritte bei der Positionierung der AutoVervollständigen-Liste, die zwischen dem AutoVervollständigen-Anbieter (Anwendung) und dem AutoVervollständigen-Client (Eingabebereich) koordiniert werden müssen. Bevor die AutoVervollständigen-Liste angezeigt wird , entweder als Ergebnis eines Aufrufs der [**Show-Methode**](itipautocompleteprovider-show.md) des AutoVervollständigen-Anbieters oder aufgrund der Eingabe von Text über die Tastatur durch den Benutzer, muss der Anbieter den Client darüber informieren, wo die AutoVervollständigen-Liste positioniert werden soll. Der Anbieter sollte die folgenden Schritte ausführen:

-   Verwenden Sie die [**ITipAutocompleteClient::RequestShowUI-Methode**](itipautocompleteclient-requestshowui.md) des AutoVervollständigen-Clients, um zu bestimmen, ob der Eingabebereich bereit ist, die AutoVervollständigen-Liste anzuzeigen. **RequestShowUI** verwendet den *HWND-Parameter,* der das HWND für das AutoVervollständigen-Listenfenster ist, und die Methode gibt **TRUE** oder **FALSE** zurück, um anzugeben, ob es sich um den Zustand handelt, in dem die AutoVervollständigen-Liste angezeigt werden kann. Wenn der Client **FALSE zurückgibt,** sollte der Anbieter nicht versuchen, die AutoVervollständigen-Liste zu zeigen.
-   Rufen [**Sie RequestShowUI**](itipautocompleteclient-requestshowui.md) auf, um das Popuphandl für das AutoVervollständigen-Listenfenster vor dem Aufrufen der [**ITipAutocompleteClient::P referredRects-Methode zu festlegen.**](itipautocompleteclient-preferredrects.md) Wenn Sie dies nicht tun, tritt beim Aufrufen von PreferredRects ein **E \_ INVALIDARG-Fehler** **auf.**
-   Wenn [**RequestShowUI**](itipautocompleteclient-requestshowui.md) **TRUE** zurückgibt, sollte der Anbieter das Standardkoordinatenrechteck der AutoVervollständigen-Liste basierend auf der Position des Texteingabefelds berechnen und dann die [**ITipAutocompleteClient::P referredRects-Methode des AutoVervollständigen-Clients aufrufen.**](itipautocompleteclient-preferredrects.md) Dadurch kann der AutoVervollständigen-Client das Rechteck anpassen, um zu vermeiden, dass sich die AutoVervollständigen-Liste mit dem Eingabebereich überschneiden. Die **PreferredRects-Methode** verwendet vier Parameter:

    -   RECT *rcACList:* Das Standardkoordinatenrechteck der AutoVervollständigen-Liste.
    -   RECT *rcField:* Das Bildschirmkoordinatenrechteck des entsprechenden Texteingabefelds.
    -   RECT *\* prcModifiedACList:* Das angepasste Bildschirmkoordinatenrechteck für die AutoVervollständigen-Funktion
    -   BOOL *\* pfShowAbove:* Dieser Parameter gibt dem Anbieter an, ob das *Rechteck prcModifiedACList* die AutoVervollständigen-Liste über oder unterhalb des Eingabebereichs positioniert. Die Anwendung kann diese Informationen verwenden, um Benutzeroberflächenelemente wie Ziehpunkte und Bildlaufleisten ordnungsgemäß zu zeichnen. Der Anbieter sollte zunächst die Richtung übergeben, in der die AutoVervollständigen-Liste relativ zum Texteingabefeld von *rcACList positioniert wird.* Der Client ändert *pfShowAbove* nicht, wenn *prcModifiedACList* auf *rcACList gesetzt wird.*

    Verwenden Sie die Rückgabewerte der *Argumente prcModifiedACList* und *pfShowAbove* out, um das Listenfenster AutoVervollständigen zu positionieren und anzuzeigen. Wenn der Eingabebereich nicht verwendet wird, [**gibt RequestShowUI**](itipautocompleteclient-requestshowui.md) immer **TRUE** zurück, und *prcModifiedACList* ist immer identisch mit *rcACList.* *pfShowAbove bleibt* ebenfalls unverändert, was dazu führt, dass die Aufrufe keine Auswirkungen auf das Anwendungsverhalten haben. Im folgenden Beispielcode werden diese Vorgehensweisen veranschaulicht.


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



Wenn der Benutzer ein Element in der AutoVervollständigen-Liste auswählt, muss der Anbieter die [**ITipAutocompleteClient::UserSelection-Methode**](itipautocompleteclient-userselection.md) des Clients aufrufen, zusätzlich zum Einfügen des ausgewählten Elementtexts in das Texteingabefeld. Der Eingabebereich verwendet diese Benachrichtigung, um den restlichen Text zu verwerfen, der noch nicht aus dem Eingabebereich eingefügt wurde.

Wenn der Anbieter nicht mehr benötigt wird, sollte die Verknüpfung des Anbieters mit dem AutoVervollständigen-Client aufgehoben werden, indem die [**ITipAutocompleteClient::UnadviseProvider-Methode**](itipautocompleteclient-unadviseprovider.md) des AutoVervollständigen-Clients aufgerufen wird, um die Registrierung des Anbieters zu aufheben. Möglicherweise muss die Registrierung des Anbieters aus zwei Gründen aufgehoben werden: weil das Texteingabefeld, dem der Anbieter zugeordnet ist, zerstört wurde oder weil die Anwendung nur einen AutoVervollständigen-Client anstelle eines Pro-Text-Eingabefelds erstellt. In diesem Fall muss die Registrierung des Anbieters jedes Mal aufgehoben werden, wenn der Fokus aus dem Textfeld entfernt wird.

## <a name="conclusion"></a>Zusammenfassung

Die Integration der automatischen Vervollständigung im Eingabebereich ist ein leistungsstarkes Tool zur Verbesserung der Benutzerfreundlichkeit in Windows-Anwendungen, die AutoVervollständigen-Listen auf Tablet-PCs enthalten. Ohne Integration müssen Benutzer des Eingabebereichs einen mühsamen Prozess durchgehen, bei dem text ein Zeichen nach dem anderen eingefügt und der Eingabebereich neu positioniert wird, um AutoVervollständigen zu verwenden. Bei der Integration werden AutoVervollständigen-Listen an einem geeigneten Ort angezeigt, da Benutzer im Eingabebereich frei geben, was sowohl die Geschwindigkeit als auch die Einfachheit der Texteingabe erhöht. In Anwendungen, die AutoVervollständigen-Funktionen enthalten, die auf shell AutoVervollständigen oder .NET Framework 3.0 AutoVervollständigen aufsetzen, ist die AutoVervollständigen-Integration des Eingabebereichs ein kostenloses und überzeugendes Feature. Darüber hinaus wird ein einfacher Satz von COM-basierten Schnittstellen bereitgestellt, um die gleiche integrierte Benutzeroberfläche für Anwendungen zu ermöglichen, die benutzerdefinierte AutoVervollständigen-Steuerelemente verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 
