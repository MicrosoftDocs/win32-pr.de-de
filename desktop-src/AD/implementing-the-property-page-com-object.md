---
title: Implementieren des COM-Objekts der Eigenschaften Seite
description: Eine Eigenschaften Blatt Erweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementieren des COM-Objekts der Eigenschaften Seite
- COM-Objekt der Eigenschaften Seite, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55962002ca059ad6e9c137925d1ba21ba9adc513
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858143"
---
# <a name="implementing-the-property-page-com-object"></a>Implementieren des COM-Objekts der Eigenschaften Seite

Eine Eigenschaften Blatt Erweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird. Die Eigenschaften Blatt Erweiterung muss die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -und [**ishellpropsheetext**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstellen implementieren. Eine Eigenschaften Blatt Erweiterung wird instanziiert, wenn der Benutzer das Eigenschaften Blatt für ein Objekt einer Klasse anzeigt, für die die Eigenschaften Blatt Erweiterung im Anzeige Spezifizierer der Klasse registriert wurde.

-   [Implementieren von ishellextinit](#implementing-ishellextinit)
-   [Implementieren von ishellpropsheetext](#implementing-ishellpropsheetext)
-   [Übergeben des Erweiterungs Objekts an die Eigenschaften Seite](#passing-the-extension-object-to-the-property-page)
-   [Arbeiten mit dem Benachrichtigungs Objekt](#working-with-the-notification-object)
-   [Verschiedenes](#miscellaneous)
-   [Eigenschaften Blätter für Mehrfachauswahl](#multiple-selection-property-sheets)
-   [Neu in Windows Server 2003](#new-with-windows-server-2003)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementieren von ishellextinit

Nachdem das COM-Objekt der Eigenschafts Blatt Erweiterung instanziiert wurde, wird die [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode aufgerufen. **Ishellextinit:: Initialize** stellt die Eigenschaften Blatt Erweiterung mit einem [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt bereit, das Daten enthält, die sich auf das Verzeichnis Objekt beziehen, das das Eigenschaften Blatt anwendet.

Das [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält Daten im [**cfstr \_ dsobjectnames**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) -Format. Das Datenformat **cfstr \_ dsobjectnames** ist ein **HGLOBAL** , das eine [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur enthält. Die **dsobjectnames** -Struktur enthält Verzeichnis Objektdaten, auf die die Eigenschaften Blatt Erweiterung angewendet wird.

Das [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält auch Daten im Format der Optionen für die [**cfstr \_ DS- \_ Anzeige \_ Spezifikation \_**](cfstr-ds-display-spec-options.md) . Das Datenformat der **cfstr \_ DS- \_ Anzeige \_ \_ Spezifikation** ist ein **HGLOBAL** , das eine [**dsdisplayspecoptions**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) -Struktur enthält. **Dsdisplayspecoptions** enthält Konfigurationsdaten, die von der Erweiterung verwendet werden können.

Wenn ein anderer Wert als **S \_ OK** von [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)zurückgegeben wird, wird das Eigenschaften Blatt nicht angezeigt.

Die Parameter " *pidlfolder* " und " *hkeyprogid* " der [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode werden nicht verwendet.

Der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger kann durch die Erweiterung gespeichert werden, indem der Verweis Zähler von **IDataObject** erhöht wird. Diese Schnittstelle muss freigegeben werden, wenn Sie nicht mehr benötigt wird.

## <a name="implementing-ishellpropsheetext"></a>Implementieren von ishellpropsheetext

Nachdem [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) zurückgegeben wurde, wird die [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) -Methode aufgerufen. Die Eigenschaften Blatt Erweiterung muss während dieser Methode die Seite oder Seiten hinzufügen. Eine Eigenschaften Seite wird erstellt, indem Sie eine [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur füllt und diese Struktur dann [**an die Funktion**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) "die Funktion" von "| Die Eigenschaften Seite wird dann durch Aufrufen der Rückruffunktion, die an **ishellpropsheetext:: addPages** im *lpfnaddpage* -Parameter übergeben wird, dem Eigenschaften Blatt hinzugefügt.

Wenn ein anderer Wert als **S \_ OK** von [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)zurückgegeben wird, wird das Eigenschaften Blatt nicht angezeigt.

Wenn die Eigenschaften Blatt Erweiterung keine Seiten zum Eigenschaften Blatt hinzufügen muss, sollte Sie nicht die Rückruffunktion aufrufen, die an [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) im *lpfnaddpage* -Parameter übergeben wird.

Die [**ishellpropsheetext:: replacepage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) -Methode wird nicht verwendet.

## <a name="passing-the-extension-object-to-the-property-page"></a>Übergeben des Erweiterungs Objekts an die Eigenschaften Seite

Das Erweiterungs Objekt des Eigenschaften Blatts ist unabhängig von der Eigenschaften Seite. In vielen Fällen ist es wünschenswert, das Erweiterungs Objekt oder ein anderes Objekt auf der Eigenschaften Seite zu verwenden. Legen Sie hierzu den **LPARAM** -Member der [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur auf den Objekt Zeiger fest. Die Eigenschaften Seite kann diesen Wert dann abrufen, wenn die [**WM- \_ InitDialog**](../dlgbox/wm-initdialog.md) -Nachricht verarbeitet wird. Für eine Eigenschaften Seite ist der *LPARAM* -Parameter der **WM- \_ InitDialog** -Nachricht ein Zeiger auf die **PROPSHEETPAGE** -Struktur. Rufen Sie den Objekt Zeiger ab, indem Sie den *LPARAM* der **WM- \_ InitDialog** -Nachricht in einen **PROPSHEETPAGE** -Zeiger umwandeln und dann den **LPARAM** -Member der **PROPSHEETPAGE** -Struktur abrufen.

Im folgenden C++-Codebeispiel wird gezeigt, wie ein-Objekt an eine Eigenschaften Seite übergeben wird.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Beachten Sie, dass das Eigenschaften Blatt nach dem Aufrufen von [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) das Erweiterungs Objekt des Eigenschaften Blatts freigibt und es nie erneut verwendet. Dies bedeutet, dass das Erweiterungs Objekt gelöscht wird, bevor die Eigenschaften Seite angezeigt wird. Wenn die Seite versucht, auf den Objekt Zeiger zuzugreifen, wird der Arbeitsspeicher freigegeben, und der Zeiger ist nicht gültig. Um dies zu korrigieren, erhöhen Sie den Verweis Zähler für das Erweiterungs Objekt, wenn die Seite hinzugefügt wird, und geben Sie dann das Objekt frei, wenn das Dialogfeld der Eigenschaften Seite zerstört wird. Dadurch entsteht ein weiteres Problem, da das Dialogfeld Eigenschaften Seite erst erstellt wird, wenn die Seite zum ersten Mal angezeigt wird. Wenn der Benutzer nie die Erweiterungs Seite auswählt, wird die Seite niemals erstellt und zerstört. Dies führt dazu, dass das Erweiterungs Objekt nie freigegeben wird, sodass ein Speicherfehler auftritt. Um dies zu vermeiden, implementieren Sie eine Eigenschaften Seiten-Rückruffunktion. Fügen Sie zu diesem Zweck dem **dwFlags** -Member der [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur das Flag " **PSP \_ usecallback** " hinzu, und legen Sie den **pfncallback** -Member der **PROPSHEETPAGE** -Struktur auf die Adresse der implementierten [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Funktion fest. Wenn die **PropSheetPageProc** -Funktion die **pspcb- \_ releasebenachrichtigung** empfängt, enthält der *PPSP* -Parameter von **PropSheetPageProc** einen Zeiger auf die **PROPSHEETPAGE** -Struktur. Der **LPARAM** -Member der **PROPSHEETPAGE** -Struktur enthält den Erweiterungs Zeiger, der zum Freigeben des Objekts verwendet werden kann.

Im folgenden C++-Codebeispiel wird gezeigt, wie ein Erweiterungs Objekt freigegeben wird.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Arbeiten mit dem Benachrichtigungs Objekt

Da die Erweiterungs Seiten der Eigenschaften Seite in einem Eigenschaften Blatt angezeigt werden, das von einer für die Erweiterung unbekannten Komponente erstellt wurde, ist es erforderlich, einen "Manager" zu verwenden, um die Datenübertragung zwischen den Erweiterungs Seiten und dem Eigenschaften Blatt zu verarbeiten. Dieser "Manager" wird als Benachrichtigungs Objekt bezeichnet. Das Benachrichtigungs Objekt fungiert als Moderator zwischen den einzelnen Seiten und dem Eigenschaften Blatt.

Wenn das Eigenschafts Blatt-Erweiterungs Objekt initialisiert wird, muss die Erweiterung ein Benachrichtigungs Objekt durch Aufrufen von [**adspropcreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)erstellen, wobei das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt, das von [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) abgerufen wurde, und der Name des Verzeichnis Objekts übergeben wird. Der Verweis Zähler der **IDataObject** -Schnittstelle muss nicht erhöht werden, da das Benachrichtigungs Objekt, das von der **adspropkreatenotifyobj** -Funktion erstellt wird, dies tut. Das von **adspropkreatenotifyobj** bereitgestellte Benachrichtigungs Objekt Handle sollte für die spätere Verwendung gespeichert werden. **Adspropkreatenotifyobj** kann entweder während **ishellextinit:: Initialize** oder [**ishellpropsheetext:: addPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)aufgerufen werden. Wenn die Eigenschaften Blatt Erweiterung heruntergefahren wird, muss Sie eine WM-Benachrichtigung zum [**\_ \_ Benachrichtigen \_**](wm-adsprop-notify-exit.md) der Nachricht an das Benachrichtigungs Objekt senden. Dies bewirkt, dass sich das Benachrichtigungs Objekt selbst zerstört. Dies wird am besten erreicht, wenn die [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) -Funktion die **pspcb- \_ releasebenachrichtigung** empfängt.

Durch Aufrufen von [**adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)kann die Erweiterung des Eigenschaften Blatts zusätzlich zu den vom [**cfstr \_ dsobjectnames**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) -Zwischenablage Format bereitgestellten Daten abrufen. Einer der Vorteile der Verwendung von **adspropgetinitinfo** besteht darin, dass ein [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Objekt bereitgestellt wird, das für die programmgesteuerte Arbeit mit dem Directory-Objekt verwendet wird.

> [!Note]  
> Im Gegensatz zu den meisten com-Methoden und-Funktionen erhöht [**adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) den Verweis Zähler für das [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Objekt nicht. Das **IDirectoryObject** darf nicht freigegeben werden, es sei denn, der Verweis Zähler wird zuerst manuell inkrementiert.

 

Wenn die Eigenschaften Seite erstmalig erstellt wird, muss die Erweiterung die Seite beim Benachrichtigungs Objekt registrieren, indem [**adspropsethwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) mit dem Fenster Handle der Seite aufgerufen wird.

[**Adspropcheckifbeschreib Table**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) ist eine Utility-Funktion, die die Eigenschaften Blatt Erweiterung verwenden kann, um zu bestimmen, ob eine Eigenschaft geschrieben werden kann.

## <a name="miscellaneous"></a>Verschiedenes

Das Handle der Eigenschaften Seite wird an die Dialogfeld Seite der Seite übermittelt. Das Eigenschaften Blatt ist das direkt übergeordnete Element der Eigenschaften Seite, sodass das Handle des Eigenschaften Blatts durch Aufrufen der [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) -Funktion mit dem Eigenschaften Seiten Handle abgerufen werden kann.

Wenn sich der Inhalt der Erweiterungs Seite ändert, sollte in der Erweiterung das [**propsheet \_**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) -Makro geändert verwendet werden, um das Eigenschaften Blatt über Änderungen zu benachrichtigen. Auf dem Eigenschaften Blatt wird dann die Schaltfläche anwenden aktiviert.

## <a name="multiple-selection-property-sheets"></a>Eigenschaften Blätter Multiple-Selection

Mit den Betriebssystemen Windows Server 2003 und höher unterstützen die Active Directory-Verwaltungs-MMC-Snap-Ins Eigenschaften Blatt Erweiterungen für mehrere Verzeichnisobjekte. Diese Eigenschaften Blätter werden angezeigt, wenn die Eigenschaften für mehr als ein Element gleichzeitig angezeigt werden. Der Hauptunterschied zwischen einer Erweiterung für ein Einzel Auswahl-Eigenschafts Blatt und einer Erweiterung für eine Eigenschaften Seite mit mehreren Auswahl besteht darin, dass die [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur, die vom [**cfstr \_ dsobjectnames**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) -Zwischenablage Format in [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) bereitgestellt wird, mehr als eine [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Struktur enthält.

Wenn das Benachrichtigungs Objekt erstellt wird, muss eine Mehrfachauswahl-Eigenschaften Blatt Erweiterung anstelle eines von der Erweiterung erstellten Namens einen eindeutigen Namen übergeben, der vom Snap-in bereitgestellt wird. Um den eindeutigen Namen abzurufen, fordern Sie das [**cfstr \_ DS \_ multiselectproppage**](cfstr-ds-multiselectproppage.md) -Zwischenablage Format aus dem [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) an, das von [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)abgerufen wurde. Diese Daten sind ein **HGLOBAL** , das eine mit NULL endenden Unicode-Zeichenfolge enthält, die der eindeutige Name ist. Dieser eindeutige Name wird dann an die [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) -Funktion übergeben, um das Benachrichtigungs Objekt zu erstellen. Die Beispiel Funktion " **comateadsnotificationobject** " im [Beispiel Code für die Implementierung des Eigenschaften Blatt-com-Objekts](example-code-for-implementation-of-the-property-sheet-com-object.md) veranschaulicht, wie dies ordnungsgemäß funktioniert, und dass mit früheren Versionen des Snap-ins kompatibel ist, die keine Eigenschaften Blätter für Mehrfachauswahl unterstützen.

Bei Mehrfachauswahl-Eigenschaften Blättern wird das System nur an das erste Objekt im [**dsobject**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) -Array gebunden. Aus diesem Grund liefert [**adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) nur das [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Attribut und das Write-able-Attribut für das erste Objekt im Array. Die anderen Objekte im Array sind nicht an gebunden.

Eine Mehrfachauswahl-Eigenschaften Blatt Erweiterung wird unter dem [**adminmultiselectpropertypages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) -Attribut registriert.

## <a name="new-with-windows-server-2003"></a>Neu in Windows Server 2003

Die folgenden Features sind neu in Windows Server 2003.

Wenn auf der Eigenschaften Seite ein Fehler auftritt, kann [**adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) mit den entsprechenden Fehler Daten aufgerufen werden. **Adspropsenderrormessage** speichert alle Fehlermeldungen in einer Warteschlange. Diese Meldungen werden angezeigt, wenn [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) das nächste Mal aufgerufen wird. Wenn **adspropshowerrordialog** zurückgibt, werden die Nachrichten in der Warteschlange gelöscht.

In Windows Server 2003 wird die Funktion " [**adspropabthwndwithtitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) " eingeführt. Diese Funktion ähnelt [**adspropsetup**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), enthält jedoch den Seitentitel. Dadurch kann das von [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) angezeigte Fehler Dialogfeld nützlichere Daten für den Benutzer bereitstellen. Wenn die Eigenschaften Blatt Erweiterung die **adspropshowerrordialog** -Funktion verwendet, sollte die Erweiterung anstelle von **adsproppinthwnd** **adspropabthwndwithtitle** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel Code für die Implementierung des Eigenschaften Blatts-com-Objekts](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 