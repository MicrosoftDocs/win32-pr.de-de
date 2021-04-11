---
description: In Windows Vista integriert der Tablet PC-Eingabebereich neue Auto Vervollständigen-Funktionen, die es ermöglichen, dass die Auto Vervollständigen-Liste einer Anwendung in Echtzeit aktualisiert wird, da die frei Hand Eingabe eines Benutzers im Eingabebereich erkannt wird.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Verwenden des Auto Vervollständigen-Eingabe Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e7f108631eb2723b71bf8ed919c17a0eabff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128993"
---
# <a name="using-input-panel-autocomplete"></a>Verwenden des Auto Vervollständigen-Eingabe Bereichs

In Windows Vista integriert der Tablet PC-Eingabebereich neue Auto Vervollständigen-Funktionen, die es ermöglichen, dass die Auto Vervollständigen-Liste einer Anwendung in Echtzeit aktualisiert wird, da die frei Hand Eingabe eines Benutzers im Eingabebereich erkannt wird. Außerdem ist die Auto Vervollständigen-Liste der Anwendung an einem geeigneten Speicherort für Benutzer des Eingabe Bereichs positioniert. Ohne die automatische Vervollständigung des Eingabe Bereichs ist die Verwendung von Auto Vervollständigen-Funktionen mit dem Eingabebereich ein schwieriger Prozess, bei dem Benutzer jeweils ein Zeichen einfügen und den Eingabebereich verschieben müssen, um auf Auto Vervollständigen-Vorschläge zuzugreifen. Mit der-Integration ist AutoComplete ein leistungsfähiges Tool für Tablet PC-Benutzer, das beschleunigt und die einfache Eingabe von Text mit dem Eingabebereich erhöht.

![Eingabebereich mit Internet Explorer-Liste "Auto Vervollständigen"](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Es gibt drei Möglichkeiten, wie eine Anwendung die Auto Vervollständigen-Integration in den Eingabebereich nutzen kann. Anwendungen, die eine Auto Vervollständigen-Funktionalität enthalten, die mithilfe von Shell AutoComplete (über die [**iautocomplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) -Schnittstelle) oder .NET Framework Auto vervollständigen (über die [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) -Enumeration) erstellt wurde, erhalten die automatische Vervollständigung im Eingabebereich ohne Codeänderungen. Anwendungen, die benutzerdefinierte AutoComplete-Textfelder enthalten, können den Eingabebereich der AutoComplete-API verwenden, um die gleiche Funktionalität zu erhalten.

In allen Fällen können Sie diese Änderungen an der Auto Vervollständigen-Liste der Anwendung vornehmen, ohne die Benutzeroberfläche oder Vorhersage Logik zu duplizieren oder zu ändern, die von einer Anwendung verwendet wird, um eine Auto Vervollständigen-Liste zu generieren. Die Auto Vervollständigen-Liste wird von der Anwendung weiterhin als Besitzer gezeichnet, und die Inhalte der Auto Vervollständigen-Liste sind identisch, wenn der Text direkt in das Bearbeitungsfeld eingegeben wurde.

Die Auto Vervollständigen-Integration im Eingabebereich wird unter dem Betriebssystem Windows Vista oder höheren Versionen unterstützt. Die Auto Vervollständigen-Integration in den Eingabebereich ist ab Windows Vista in Shell AutoComplete integriert, und in Windows Forms Entwicklung ab .NET Framework, Version 3,0. Während sowohl [**iautocomplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) als auch [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) unter früheren Versionen von Windows ausgeführt werden, wird die automatische vollständige Integration des Eingabe Bereichs in Microsoft Windows XP Tablet PC Edition oder früheren Betriebssystemen nicht unterstützt. Wenn Sie in früheren Versionen von Tablet PC den Eingabebereich Auto Vervollständigen ausführen, werden die Anwendungen auf das Verhalten vor der Integration zurückgesetzt.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Gründe für das Integrieren von AutoComplete-Anwendungs Listen in den Eingabebereich

Durch die Integration der Auto Vervollständigen-Liste einer Anwendung können Benutzer, die Text in ein Textfeld eingeben, das eine Auto Vervollständigen-Funktionalität einschließt, die maximale Benutzerfreundlichkeit und Geschwindigkeit der Eingabe ermöglichen. Darüber hinaus wird eine Anwendung, die die Auto Vervollständigen-Integration in den Eingabebereich einschließt, sofort so angezeigt, als ob Sie mit dem Tablet PC entwickelt wurde, sodass die Anwendung für Tablet PC-Benutzer ansprechender wird.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Interagieren der Eingabe Panel-und Auto Vervollständigen-Liste ohne Integration

Verwenden des Eingabe Bereichs zum Eingeben von Text in ein Textfeld, das eine Auto Vervollständigen-Liste enthält, jedoch nicht in den Eingabebereich integriert ist:

1.  Der Benutzer legt den Fokus in das Textfeld und öffnet den Eingabebereich.
2.  Der Benutzer schreibt ein oder zwei Zeichen.
3.  Der Benutzer tippt auf **Insert**. Der Eingabebereich gibt den Text in das Textfeld der Anwendung ein. Die Auto Vervollständigen-Liste der Anwendung wird angezeigt und ist im Eingabebereich wahrscheinlich teilweise oder vollständig verdeckt.
4.  Der Benutzer zieht den Eingabebereich ein, um die Auto Vervollständigen-Liste der Anwendung zu erkennen.
5.  Wenn Sie davon ausgehen, dass der richtige Eintrag in der Liste Auto Vervollständigen enthalten ist, kann der Benutzer jetzt diesen Eintrag auswählen. Andernfalls muss der Benutzer die Schritte 2 und 3 wiederholen.

Dies ist eindeutig ein mühsamer Prozess. Die Erwartungen der Benutzer, wie eine Auto Vervollständigen-Liste funktionieren sollte, sind gestrichelt, und ihre Fähigkeit zum Ausführen von Aufgaben ist beeinträchtigt.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Verbesserung der Eingabe Panel-und Auto Vervollständigen-Listen Interaktion durch Integration

Verwenden des Eingabe Bereichs zum Eingeben von Text in ein Textfeld, das eine Auto Vervollständigen-Liste enthält, die in den Eingabebereich integriert ist:

1.  Der Benutzer legt den Fokus in das Textfeld und öffnet den Eingabebereich.
2.  Der Benutzer schreibt ein oder zwei Zeichen. Die Auto Vervollständigen-Liste der Anwendung wird direkt oberhalb oder direkt unterhalb des Eingabe Panels angezeigt, wenn der Benutzer Text schreibt.
3.  Der Benutzer wählt den Eintrag aus der Auto Vervollständigen-Liste aus. der Eintrag wird direkt in das Textfeld der Anwendung eingefügt, oder der Benutzer wiederholt Schritt 2, bis der richtige Eintrag angezeigt wird.

Aufgrund der Integration wird die Auto Vervollständigen-Liste angezeigt und aktualisiert, während der Benutzer im Eingabebereich schreibt. Außerdem ist die Liste so positioniert, dass Sie für den Benutzer praktisch ist, während Sie schreiben und nicht durch Eingabebereich verdeckt werden. Wenn der Benutzer schließlich ein Element aus einer Auto Vervollständigen-Liste auswählt, wird das Element direkt in das Texteingabefeld der Anwendung eingefügt, sodass der Benutzer den Schritt des Fügens von Text aus dem Eingabebereich umgehen kann.

![Eingabebereich mit Outlook Express Auto Vervollständigen-Liste](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Standard mäßige Auto Vervollständigen-Komponenten, die die automatische Vervollständigung im Eingabebereich einschließen

Sowohl [**iautocomplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) als auch [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) enthalten integrierte Integration des Eingabe Bereichs Auto vervollständigen. Anwendungen, die eine dieser standardmäßigen Auto Vervollständigen-Komponenten verwenden, können die Funktion "Auto Vervollständigen" für den Eingabebereich nutzen, ohne dass zusätzliche Arbeit erforderlich ist. Während der Eingabebereich Auto Vervollständigen nur unter Windows Vista oder neuen Versionen des Windows-Betriebssystems unterstützt wird, erhalten Anwendungen, die vor der Veröffentlichung von Windows Vista mithilfe von **iautocomplete** erstellt wurden, bei Ausführung unter Windows Vista automatisch die automatische Vervollständigung des Eingabe Bereichs. Die folgenden Abschnitte enthalten weitere Informationen zu den spezifischen **iautocomplete** -und AutoCompleteMode-Elementen, die die Auto Vervollständigen-Integration im Eingabebereich einschließen.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Shell Auto Vervollständigen mit Eingabebereich Auto Vervollständigen-Integration

Anwendungen, die [**iautocomplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) verwenden, erhalten die Auto Vervollständigen-Integration für den Eingabebereich kostenlos. Obwohl die Auto Vervollständigen-APIs für die Shell in Windows 2000 weiter integriert sind, wird die Auto Vervollständigen-Integration im Eingabebereich nur unter Windows Vista und neueren Versionen unterstützt. Anwendungen, die vor der Veröffentlichung von Windows Vista erstellt wurden und die **iautocomplete** verwenden, erhalten bei Ausführung unter Windows Vista automatisch die automatische Vervollständigung im Eingabebereich.

Um die Auto Vervollständigen-Funktion auf diese Weise nutzen zu können, müssen Sie das Auto Vervollständigen-Objekt (**CLSID \_ Auto Vervollständigen**) verwenden. Wenn Sie die automatische Vervollständigung für URLs oder Dateinamen bereitstellen möchten, verwenden Sie die Funktion " [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) ", um das Objekt "Auto Vervollständigen" zu erstellen.

Zusätzlich zu [**iautocomplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)können Sie [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) oder [**iautocompletedropdown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)s direkt implementieren und die Auto Vervollständigen-Integration automatisch im Eingabebereich erhalten.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Eingabebereich der Auto Vervollständigen-Integration in .NET Framework Anwendungen

Ab .NET Framework 3,0 enthalten Windows Forms Textfelder autocomplete. Windows Forms Textfeld Auto Vervollständigen basiert auf Shell autocomplete. Dies bedeutet, dass auch die automatische Vervollständigung in den Eingabebereich integriert ist. .NET Framework 3,0 wird bei Windows-Editionen vor Windows Vista unterstützt. Da jedoch die Auto Vervollständigen-Integration im Eingabebereich nur unter Windows Vista oder höheren Versionen unterstützt wird, funktioniert die automatische Vervollständigung im Eingabebereich nur in einer .NET Framework 3,0-Anwendung, wenn Sie unter Windows Vista oder höheren Versionen installiert wird.

Anwendungen, die die Auto Vervollständigen-Integration im Eingabebereich in .NET Framework 3,0 nutzen möchten, müssen ein Windows Forms [Textfeld](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) mit aktivierter [AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) -Eigenschaft verwenden. Sie müssen keine weiteren Schritte durchführen, um die automatische Vervollständigung von Windows Forms Auto Vervollständigen zu nutzen.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Direktes Verwenden von AutoComplete-APIs für den Eingabebereich

Entwickler benutzerdefinierter Auto Vervollständigen-Textfelder müssen direkt mit dem Eingabebereich der AutoComplete-APIs arbeiten, um die verbesserte Texteingabe zu erhalten, die durch die automatische Vervollständigung durch den Eingabebereich in Ihren Anwendungen ermöglicht wird. Die Auto Vervollständigen-APIs für den Eingabebereich sind als Teil des Windows Vista-Betriebssystems und als Teil des Tablet Platform SDK, Version 1,9 oder höher, enthalten. Die Auto Vervollständigen-Schnittstellen für den Eingabebereich sind COM-basierte Schnittstellen.

Im folgenden Abschnitt wird beschrieben, wie Sie diese Schnittstellen im Detail für eine C++-Anwendung arbeiten. Diese COM-Schnittstellen können jedoch in den meisten Sprachen (einschließlich C) \# durch die Verwendung von COM-Interop implementiert werden.

Um die automatische Vervollständigung im Eingabebereich in ein benutzerdefiniertes Textfeld für die automatische Vervollständigung zu implementieren, sind die beiden erforderlichen Schnittstellen die [**itipaudecompleteprovider-Schnittstelle**](itipautocompleteprovider.md) und die [**itipaudecompleteclient-Schnittstelle**](itipautocompleteclient.md). Die Definitionen für diese Schnittstellen finden Sie unter tipaudecomplete. h und tipaudecomplete \_ i.c.

Zuerst muss eine Anwendung eine Auto Vervollständigen-Anbieter Klasse definieren und instanziieren, die [**itipaudecompleteprovider**](itipautocompleteprovider.md) für jedes Texteingabefeld implementiert, das eine Auto Vervollständigen-Liste enthält. Diese Klasse verwaltet die Anwendungsseite der AutoComplete-Integration. Alle Auto Vervollständigen-Anforderungen aus dem Eingabebereich werden vom Auto Vervollständigen-Client an die Anwendung über den Auto Vervollständigen-Anbieter der Anwendung gestellt. Der AutoComplete-Anbieter der Anwendung muss sowohl auf das HWND für die Auto Vervollständigen-Liste der Anwendung als auch auf den hwind für das zugehörige Texteingabefeld zugreifen können. Außerdem müssen die folgenden Methoden von **itipaudecompleteprovider** implementiert werden:

-   [**Itipaudecompleteprovider:: updatependingtext-Methode**](itipautocompleteprovider-updatependingtext.md): Diese Methode wird vom AutoComplete-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich geschrieben hat. Beim Empfang dieser Benachrichtigung ist der Anbieter dafür verantwortlich, eine Auto Vervollständigen-Liste zu generieren, als ob der Text in das Texteingabefeld der Anwendung eingegeben wurde. Die Zeichenfolge, die an den AutoComplete-Anbieter über die **itipaudecompleteprovider:: updatependingtext-Methode** übergeben wird, enthält nur den Text, der sich derzeit im Eingabebereich befindet. Wenn also zusätzlicher Text im Feld Texteingabe vorhanden ist, liegt es in der Verantwortung des Anbieters, ihn ordnungsgemäß an den vom Client gesendeten Text anzufügen. Die String Pass by **itipautocompleteprovider:: updatependingtext-Methode** sollte als Ersatz für die aktuelle Auswahl im Feld behandelt werden. Wenn keine aktuelle Auswahl vorhanden ist, sollte diese an der Position der aktuellen Einfügemarke platziert werden. Nachdem die Auto Vervollständigen-Liste generiert wurde, sollte der Anbieter die [**itipaudecompleteprovider:: Show-Methode**](itipautocompleteprovider-show.md) aufrufen **, um die** Auto Vervollständigen-Liste anzuzeigen. Die Anwendung sollte keine Aufrufe von **updatependingtext** Zwischenspeichern, sondern jeden zusätzlichen Aufruf von **updatependingtext** als Abbruch des vorherigen Aufrufs behandeln, um zu vermeiden, dass eine veraltete Auto Vervollständigen-Listen Benutzeroberfläche blinkt. Der folgende Beispielcode veranschaulicht diese Vorgehensweisen.

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

    

-   [**Itipaudecompleteprovider:: Show-Methode**](itipautocompleteprovider-show.md): Diese Methode wird von [**updatependingtext**](itipautocompleteprovider-updatependingtext.md)aufgerufen, kann aber auch jederzeit vom AutoComplete-Client aufgerufen werden. Nach Erhalt dieses Aufrufes muss der Auto Vervollständigen-Anbieter den Auto Vervollständigen-Anbieter wie durch den-Parameter angegeben ausblenden oder anzeigen. Vor der Anzeige der Auto Vervollständigen-Liste wird vom Auto Vervollständigen-Anbieter erwartet, dass er den AutoComplete-Client über die Position der Auto Vervollständigen-Liste abschließt. Weitere Informationen zum Positionieren der Auto Vervollständigen-Liste finden Sie weiter unten in diesem Artikel.

Als nächstes sollte die Anwendung die Active Template Library (ATL)- [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwenden, um eine Instanz der [**itipautocompleteclient-Schnittstelle**](itipautocompleteclient.md) mit der Klassen-ID **CLSID \_ tipautocompleteclient** als Prozess interner Server zu entwickeln und den Anbieter dann beim Client zu registrieren. Die Methode "AutoComplete Client [**itipaudecompleteclient:: adviseprovider**](itipautocompleteclient-adviseprovider.md) " registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann. Wenn tiptsf.dll im System nicht vorhanden ist, schlägt die **cokreateinzustance** -Funktion fehl und gibt **RegDB \_ E \_ classnotreg** zurück. An diesem Punkt kann die Anwendung das [**itipaubucompleteprovider**](itipautocompleteprovider.md) -Objekt verwerfen und fortfahren, als ob der Eingabebereich nicht vorhanden ist, da es nicht auf einem solchen System vorhanden ist.

Die Anwendung kann eine Instanz von [**itipaudecompleteclient**](itipautocompleteclient.md) oder eine Instanz pro Textfeld erstellen. Die erste Option erfordert, dass der Anbieter bei jeder Änderung des Fokus nicht registriert und registriert wird. Weitere Informationen zum Aufheben der Registrierung des Auto Vervollständigen-Anbieters finden Sie weiter unten in diesem Thema.

Bei der Positionierung der Auto Vervollständigen-Liste, die zwischen dem AutoComplete-Anbieter (Anwendung) und dem AutoComplete-Client (Eingabebereich) koordiniert werden muss, sind mehrere Schritte erforderlich. Bevor die Auto Vervollständigen-Liste angezeigt wird, entweder aufgrund eines Aufrufes der [**Show**](itipautocompleteprovider-show.md) -Methode des Auto Vervollständigen-Anbieters oder aufgrund der Eingabe von Text über die Tastatur durch den Benutzer, muss der Anbieter den Client über die Position der Auto Vervollständigen-Liste informieren. Der Anbieter sollte die folgenden Schritte ausführen:

-   Verwenden Sie die [**itipautocompleteclient:: requestshowui-Methode**](itipautocompleteclient-requestshowui.md) des AutoComplete-Clients, um zu bestimmen, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste zu sehen. **Requestshowui** übernimmt den *HWND* -Parameter, der das HWND für das Auto Vervollständigen-Listenfenster ist, und die Methode gibt **true** oder **false** zurück, um anzugeben, ob es sich um den Zustand handelt, in dem die Auto Vervollständigen-Liste angezeigt werden kann. Wenn der Client **false** zurückgibt, sollte der Anbieter nicht versuchen, die Auto Vervollständigen-Liste anzuzeigen.
-   Aufrufen von [**requestshowui**](itipautocompleteclient-requestshowui.md) , um das Popup Fenster Handle für die automatische Vervollständigung festzulegen, bevor Sie die [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)aufrufen. Wenn dies nicht der Fall ist, wird beim Aufrufen von " **preferredrects**" ein **E \_ invalidArg** -Fehler ausgelöst.
-   Wenn [**requestshowui**](itipautocompleteclient-requestshowui.md) **true** zurückgibt, sollte der Anbieter das standardmäßige Bildschirm Koordinaten Rechteck der Auto Vervollständigen-Liste basierend auf dem Speicherort des Texteingabe Felds berechnen und dann die [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)des AutoComplete-Clients aufrufen. Dies ermöglicht dem AutoComplete-Client das Anpassen des Rechtecks, um die Auto Vervollständigen-Liste mit dem Eingabebereich zu vermeiden. Die **preferredrects** -Methode benötigt vier Parameter:

    -   Rect *rcaclist*: das standardmäßige Bildschirm Koordinaten Rechteck der Auto Vervollständigen-Liste.
    -   Rect *rcfield*: das Bildschirm Koordinaten Rechteck des entsprechenden Texteingabe Felds.
    -   Rect *\* prcmodifiedaclist*: das angepasste Bildschirm Koordinaten Rechteck für den Auto Vervollständigen
    -   Bool *\* pfshowover*: dieser Parameter gibt dem Anbieter an, ob das Rechteck *prcmodifiedaclist* die Auto Vervollständigen-Liste oberhalb oder unterhalb des Eingabe Bereichs positioniert. Die Anwendung kann diese Informationen verwenden, um Benutzeroberflächen Elemente, wie z. b. Zieh Punkte und Bild Lauf leisten, ordnungsgemäß zu zeichnen Der Anbieter sollte anfänglich in der Richtung übergeben werden, dass die Auto Vervollständigen-Liste in Bezug auf das Texteingabefeld von *rcaclist* positioniert wird. " *Pfshowon* " wird vom Client nicht geändert, wenn " *prcmodifiedaclist* " auf " *rcaclist*" festgelegt ist.

    Verwenden Sie die Rückgabewerte der Argumente *prcmodifiedaclist* und *pfshowover* Out, um das Fenster Auto Vervollständigen-Liste zu positionieren und anzuzeigen. Wenn der Eingabebereich nicht verwendet wird, gibt [**requestshowui**](itipautocompleteclient-requestshowui.md) immer **true** zurück, und *prcmodifiedaclist* ist immer identisch mit *rcaclist*. *pfshowon* ist ebenfalls unverändert. das Ergebnis ist, dass die Aufrufe keine Auswirkung auf das Verhalten der Anwendung haben. Der folgende Beispielcode veranschaulicht diese Vorgehensweisen.


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



Wenn der Benutzer ein Element in der Liste AutoComplete auswählt, muss der Anbieter die [**itipaudecompleteclient:: userselection-Methode**](itipautocompleteclient-userselection.md) des Clients zusätzlich zum Einfügen des ausgewählten Element Texts in das Texteingabefeld aufzurufen. Der Eingabebereich verwendet diese Benachrichtigung, um den verbleibenden Text zu verwerfen, der noch nicht aus dem Eingabebereich eingefügt wurde.

Wenn der Anbieter nicht mehr benötigt wird, sollte die Verknüpfung des Anbieters mit dem Auto Vervollständigen-Client aufgehoben werden, indem die [**itipautocompleteclient:: unadviseprovider-Methode**](itipautocompleteclient-unadviseprovider.md) des AutoComplete-Clients aufgerufen wird, um die Registrierung des Anbieters aufzuheben. Die Registrierung des Anbieters muss aus zwei Gründen aufgehoben werden: da das Texteingabefeld, mit dem der Anbieter verknüpft ist, zerstört wurde, oder weil die Anwendung nur einen Auto Vervollständigen-Client anstelle eines pro-Texteingabe Felds erstellt. In dieser Instanz muss die Registrierung des Anbieters jedes Mal aufgehoben werden, wenn der Fokus aus dem Textfeld gewechselt wird.

## <a name="conclusion"></a>Zusammenfassung

Die Auto Vervollständigen-Integration im Eingabebereich ist ein leistungsfähiges Tool zur Verbesserung der Benutzer Leistung in Windows-Anwendungen, die Auto Vervollständigen-Listen auf Tablet PCs enthalten. Ohne Integration müssen Benutzer im Eingabebereich ein mühsames Verfahren zum Einfügen von Text ein Zeichen nacheinander durchlaufen und den Eingabebereich neu positionieren, um AutoComplete zu verwenden. Mit der-Integration werden AutoComplete-Listen an einem geeigneten Speicherort angezeigt, wenn Benutzer im Eingabebereich frei Hand Eingaben haben, wodurch die Geschwindigkeit und die einfache Texteingabe erhöht werden. In Anwendungen, die eine Auto Vervollständigen-Funktionalität enthalten, die auf der Shell Auto vervollständigen oder .NET Framework 3,0 AutoComplete basiert, ist die automatische Vervollständigung im Eingabebereich eine kostenlose und überzeugende Funktion. Außerdem wird ein einfacher Satz von COM-basierten Schnittstellen bereitgestellt, um die gleiche integrierte Benutzeroberfläche für Anwendungen zu ermöglichen, die benutzerdefinierte AutoComplete-Steuerelemente verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 
