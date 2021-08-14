---
title: Implementieren des COM-Objekts der Eigenschaftenseite
description: Eine Eigenschaftenblatterweiterung ist ein COM-Objekt, das als Prozessserver implementiert wird.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementieren des COM-Objekts der Eigenschaftenseite
- COM-Objekt der Eigenschaftenseite, Implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504c27bcf4703bb49a3e8620c287c30ae9017ab6e65345d003f2acb6c9b544e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187611"
---
# <a name="implementing-the-property-page-com-object"></a>Implementieren des COM-Objekts der Eigenschaftenseite

Eine Eigenschaftenblatterweiterung ist ein COM-Objekt, das als Prozessserver implementiert wird. Die Eigenschaftenblatterweiterung muss die Schnittstellen [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) implementieren. Eine Eigenschaftenblatterweiterung wird instanziiert, wenn der Benutzer das Eigenschaftenblatt für ein Objekt einer Klasse anzeigt, für das die Eigenschaftenblatterweiterung im Anzeigespezifizierer der Klasse registriert wurde.

-   [Implementieren von IShellExtInit](#implementing-ishellextinit)
-   [Implementieren von IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Übergeben des Erweiterungsobjekts an die Eigenschaftenseite](#passing-the-extension-object-to-the-property-page)
-   [Arbeiten mit dem Benachrichtigungsobjekt](#working-with-the-notification-object)
-   [Verschiedenes](#miscellaneous)
-   [Eigenschaftenblätter mit mehrfacher Auswahl](#multiple-selection-property-sheets)
-   [Neu mit Windows Server 2003](#new-with-windows-server-2003)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementieren von IShellExtInit

Nachdem das COM-Objekt der Eigenschaftenblatterweiterung instanziiert wurde, wird die [**IShellExtInit::Initialize-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) aufgerufen. **IShellExtInit::Initialize** stellt die Eigenschaftenblatterweiterung mit einem [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) bereit, das Daten enthält, die sich auf das Verzeichnisobjekt beziehen, das vom Eigenschaftenblatt angewendet wird.

Das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält Daten im [**CFSTR \_ DSOBJECTNAMES-Format.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) Das **CFSTR \_ DSOBJECTNAMES-Datenformat** ist ein **HGLOBAL-Objekt,** das eine [**DSOBJECTNAMES-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) enthält. Die **DSOBJECTNAMES-Struktur** enthält Verzeichnisobjektdaten, die von der Eigenschaftenblatterweiterung angewendet werden.

Das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält auch Daten im [**FORMAT CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) Das **CFSTR \_ DS \_ DISPLAY SPEC \_ \_ OPTIONS-Datenformat** ist ein **HGLOBAL-Format,** das eine [**DSDISPLAYSPECOPTIONS-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) enthält. **DSDISPLAYSPECOPTIONS** enthält Konfigurationsdaten für die Verwendung durch die Erweiterung.

Wenn ein anderer Wert als **S \_ OK** von [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)zurückgegeben wird, wird das Eigenschaftenblatt nicht angezeigt.

Die Parameter *pidlFolder* und *hkeyProgID* der [**IShellExtInit::Initialize-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) werden nicht verwendet.

Der [**IDataObject-Zeiger**](/windows/win32/api/objidl/nn-objidl-idataobject) kann von der Erweiterung gespeichert werden, indem der Verweiszähler des **IDataObject** erhöht wird. Diese Schnittstelle muss freigegeben werden, wenn sie nicht mehr benötigt wird.

## <a name="implementing-ishellpropsheetext"></a>Implementieren von IShellPropSheetExt

Nachdem [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) zurückgegeben wurde, wird die [**IShellPropSheetExt::AddPages-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) aufgerufen. Die Eigenschaftenblatterweiterung muss die Seite oder Seiten während dieser Methode hinzufügen. Eine Eigenschaftenseite wird erstellt, indem eine [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) ausgefüllt und diese Struktur dann an die [**CreatePropertySheetPage-Funktion**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) übergeben wird. Die Eigenschaftenseite wird dann dem Eigenschaftenblatt hinzugefügt, indem die Rückruffunktion aufgerufen wird, die an **IShellPropSheetExt::AddPages** im *lpfnAddPage-Parameter* übergeben wird.

Wenn von [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)ein anderer Wert als **S \_ OK** zurückgegeben wird, wird das Eigenschaftenblatt nicht angezeigt.

Wenn die Eigenschaftenblatterweiterung keine Seiten zum Eigenschaftenblatt hinzufügen muss, sollte sie nicht die Rückruffunktion aufrufen, die an [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) im *lpfnAddPage-Parameter* übergeben wird.

Die [**IShellPropSheetExt::ReplacePage-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) wird nicht verwendet.

## <a name="passing-the-extension-object-to-the-property-page"></a>Übergeben des Erweiterungsobjekts an die Eigenschaftenseite

Das Eigenschaftenblatterweiterungsobjekt ist von der Eigenschaftenseite unabhängig. In vielen Fällen ist es wünschenswert, das Erweiterungsobjekt oder ein anderes Objekt auf der Eigenschaftenseite verwenden zu können. Legen Sie hierzu den **lParam-Member** der [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) auf den Objektzeiger fest. Die Eigenschaftenseite kann diesen Wert dann abrufen, wenn sie die [**WM \_ INITDIALOG-Nachricht**](../dlgbox/wm-initdialog.md) verarbeitet. Für eine Eigenschaftenseite ist der *lParam-Parameter* der **WM \_ INITDIALOG-Nachricht** ein Zeiger auf die **PROPSHEETPAGE-Struktur.** Rufen Sie den Objektzeiger ab, indem Sie die *lParam* der **WM \_ INITDIALOG-Nachricht in** einen **PROPSHEETPAGE-Zeiger** umwandeln und dann den **lParam-Member** der **PROPSHEETPAGE-Struktur** abrufen.

Das folgende C++-Codebeispiel zeigt, wie ein Objekt an eine Eigenschaftenseite übergeben wird.


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



Beachten Sie, dass nach dem Aufruf von [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) das Eigenschaftenblatt das Eigenschaftenblatterweiterungsobjekt freigibt und es nie wieder verwendet. Dies bedeutet, dass das Erweiterungsobjekt gelöscht wird, bevor die Eigenschaftenseite angezeigt wird. Wenn die Seite versucht, auf den Objektzeiger zuzugreifen, wurde der Arbeitsspeicher freigegeben, und der Zeiger ist ungültig. Um dies zu korrigieren, erhöhen Sie den Verweiszähler für das Erweiterungsobjekt, wenn die Seite hinzugefügt wird, und geben Sie dann das Objekt frei, wenn das Dialogfeld der Eigenschaftenseite zerstört wird. Dies führt zu einem weiteren Problem, da das Dialogfeld "Eigenschaftenseite" erst erstellt wird, wenn die Seite zum ersten Mal angezeigt wird. Wenn der Benutzer die Erweiterungsseite nie auswählt, wird die Seite nie erstellt und zerstört. Dies führt dazu, dass das Erweiterungsobjekt nie freigegeben wird, sodass ein Speicherverlust auftritt. Um dies zu vermeiden, implementieren Sie eine Rückruffunktion für Eigenschaftenseiten. Fügen Sie hierzu dem **dwFlags-Member** der [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) das **PSP \_ USECALLBACK-Flag** hinzu, und legen Sie den **pfnCallback-Member** der **PROPSHEETPAGE-Struktur** auf die Adresse der [**implementierten PropSheetPageProc-Funktion**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) fest. Wenn die **PropSheetPageProc-Funktion** die **PSPCB \_ RELEASE-Benachrichtigung** empfängt, enthält der *ppsp-Parameter* von **PropSheetPageProc** einen Zeiger auf die **PROPSHEETPAGE-Struktur.** Der **lParam-Member** der **PROPSHEETPAGE-Struktur** enthält den Erweiterungszeiger, der zum Freigeben des Objekts verwendet werden kann.

Das folgende C++-Codebeispiel zeigt, wie ein Erweiterungsobjekt veröffentlicht wird.


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



## <a name="working-with-the-notification-object"></a>Arbeiten mit dem Benachrichtigungsobjekt

Da die Eigenschaftenblatterweiterungsseiten in einem Eigenschaftenblatt angezeigt werden, das von einer Komponente erstellt wird, die der Erweiterung unbekannt ist, ist es erforderlich, einen "Manager" zu verwenden, um die Datenübertragung zwischen den Erweiterungsseiten und dem Eigenschaftenblatt zu verarbeiten. Dieser "Manager" wird als Benachrichtigungsobjekt bezeichnet. Das Benachrichtigungsobjekt fungiert als Moderator zwischen den einzelnen Seiten und dem Eigenschaftenblatt.

Wenn das Eigenschaftenblatterweiterungsobjekt initialisiert wird, muss die Erweiterung ein Benachrichtigungsobjekt erstellen, indem [**sie ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)aufruft und das von [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) abgerufene [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) und den Verzeichnisobjektnamen übergibt. Es ist nicht erforderlich, den Verweiszähler der **IDataObject-Schnittstelle** zu erhöhen, da das von der **ADsPropCreateNotifyObj-Funktion** erstellte Benachrichtigungsobjekt dies tut. Das von **ADsPropCreateNotifyObj** bereitgestellte Benachrichtigungsobjekthandle sollte zur späteren Verwendung gespeichert werden. **ADsPropCreateNotifyObj** kann entweder während **IShellExtInit::Initialize** oder [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)aufgerufen werden. Wenn die Eigenschaftenblatterweiterung heruntergefahren wird, muss sie eine [**WM \_ ADSPROP \_ NOTIFY \_ EXIT-Meldung**](wm-adsprop-notify-exit.md) an das Benachrichtigungsobjekt senden. Dies bewirkt, dass sich das Benachrichtigungsobjekt selbst zerstört. Dies geschieht am besten, wenn die [**PropSheetPageProc-Funktion**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) die **PSPCB \_ RELEASE-Benachrichtigung** empfängt.

Die Eigenschaftenblatterweiterung kann Daten zusätzlich zu den Daten abrufen, die vom [**CFSTR \_ DSOBJECTNAMES-Zwischenablageformat**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) bereitgestellt werden, indem [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)aufgerufen wird. Einer der Vorteile der Verwendung von **ADsPropGetInitInfo** besteht darin, dass es ein [**IDirectoryObject-Objekt**](/windows/desktop/api/iads/nn-iads-idirectoryobject) bereitstellt, das für die programmgesteuerte Arbeit mit dem Verzeichnisobjekt verwendet wird.

> [!Note]  
> Im Gegensatz zu den meisten COM-Methoden und -Funktionen erhöht [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) den Verweiszähler für das [**IDirectoryObject-Objekt**](/windows/desktop/api/iads/nn-iads-idirectoryobject) nicht. **Das IDirectoryObject** darf nur freigegeben werden, wenn der Verweiszähler zuerst manuell erhöht wird.

 

Wenn die Eigenschaftenseite zum ersten Mal erstellt wird, sollte die Erweiterung die Seite mit dem Benachrichtigungsobjekt registrieren, indem [**sie ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) mit dem Fensterhandle der Seite aufruft.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) ist eine Hilfsprogrammfunktion, mit der die Eigenschaftenblatterweiterung bestimmen kann, ob eine Eigenschaft geschrieben werden kann.

## <a name="miscellaneous"></a>verschiedene gefährliche Stoffe

Das Handle der Eigenschaftenseite wird an die Seitendialogfeldprozedur übergeben. Das Eigenschaftenblatt ist das direkte übergeordnete Element der Eigenschaftenseite, sodass das Handle des Eigenschaftenblatts durch Aufrufen der [**GetParent-Funktion**](/windows/win32/api/winuser/nf-winuser-getparent) mit dem Eigenschaftenseitenhandle abgerufen werden kann.

Wenn sich der Inhalt der Erweiterungsseite ändert, sollte die Erweiterung das [**PropSheet \_ Changed-Makro**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) verwenden, um das Eigenschaftenblatt über Änderungen zu benachrichtigen. Das Eigenschaftenblatt aktiviert dann die Schaltfläche Anwenden.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection Eigenschaftenblätter

Mit Windows Server 2003 und höher unterstützen die MMC-Snap-Ins für die Active Directory-Verwaltung Eigenschaftenblatterweiterungen für mehrere Verzeichnisobjekte. Diese Eigenschaftenblätter werden angezeigt, wenn die Eigenschaften für mehrere Elemente gleichzeitig angezeigt werden. Der Hauptunterschied zwischen einer Einfachauswahl-Eigenschaftenblatterweiterung und einer Erweiterung für Einauswahleigenschaftenblätter besteht darin, dass die [**DSOBJECTNAMES-Struktur,**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) die vom [**CFSTR \_ DSOBJECTNAMES-Zwischenablageformat**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) in [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) bereitgestellt wird, mehr als eine [**DSOBJECT-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) enthält.

Wenn das Benachrichtigungsobjekt erstellt wird, muss eine Eigenschaftenblatterweiterung mit mehrfacher Auswahl einen eindeutigen Namen übergeben, der vom Snap-In bereitgestellt wird, anstatt einen von der Erweiterung erstellten Namen. Um den eindeutigen Namen abzurufen, fordern Sie das [**CFSTR \_ DS \_ MULTISELECTPROPPAGE-Zwischenablageformat**](cfstr-ds-multiselectproppage.md) aus dem [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) an, das von [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)abgerufen wurde. Bei diesen Daten handelt es sich um eine **HGLOBAL-Datei,** die eine mit NULL endende Unicode-Zeichenfolge enthält, die den eindeutigen Namen enthält. Dieser eindeutige Name wird dann an die [**Funktion ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) übergeben, um das Benachrichtigungsobjekt zu erstellen. Die **CreateADsNotificationObject-Beispielfunktion** in [Beispielcode für die Implementierung des COM-Objekts für Eigenschaftenblätter](example-code-for-implementation-of-the-property-sheet-com-object.md) veranschaulicht, wie dies ordnungsgemäß funktioniert und mit früheren Versionen des Snap-Ins kompatibel ist, die keine Eigenschaftenblätter mit mehrfacher Auswahl unterstützen.

Bei Eigenschaftenblättern mit mehrfacher Auswahl wird das System nur an das erste Objekt im [**DSOBJECT-Array**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) gebunden. Aus diesem Grund stellt [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) nur die [**Attribute IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) und write-fähig für das erste Objekt im Array zur Verfügung. Die anderen Objekte im Array sind nicht an gebunden.

Eine Eigenschaftenblatterweiterung mit mehrfacher Auswahl wird unter dem [**AdminMultiselectPropertyPages-Attribut**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) registriert.

## <a name="new-with-windows-server-2003"></a>Neu mit Windows Server 2003

Die folgenden Features sind mit Windows Server 2003 neu.

Wenn auf der Eigenschaftenseite ein Fehler auftritt, kann [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) mit den entsprechenden Fehlerdaten aufgerufen werden. **ADsPropSendErrorMessage** speichert alle Fehlermeldungen in einer Warteschlange. Diese Meldungen werden beim nächsten Aufruf von [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) angezeigt. Wenn **ADsPropShowErrorDialog** zurückgegeben wird, werden die Nachrichten in der Warteschlange gelöscht.

Windows Server 2003 führt die [**ADsPropSetHwndWithTitle-Funktion**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) ein. Diese Funktion ähnelt [**ADsPropSetHwnd,**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)enthält jedoch den Seitentitel. Dadurch wird das von [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) angezeigte Fehlerdialogfeld aktiviert, um dem Benutzer nützliche daten bereitzustellen. Wenn die Eigenschaftenblatterweiterung die **ADsPropShowErrorDialog-Funktion** verwendet, sollte die Erweiterung **ADsPropSetHwndWithTitle** anstelle von **ADsPropSetHwnd** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispielcode für die Implementierung des COM-Objekts des Eigenschaftenblatts](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 