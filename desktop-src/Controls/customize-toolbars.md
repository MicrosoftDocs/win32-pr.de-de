---
title: Anpassen von Symbolleisten
description: Die meisten Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen bequemen Zugriff auf die Programmfunktionalität zu ermöglichen.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104038706"
---
# <a name="how-to-customize-toolbars"></a>Anpassen von Symbolleisten

Die meisten Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen bequemen Zugriff auf die Programmfunktionalität zu ermöglichen. Statische Symbolleisten haben jedoch gewisse Mängel – z. b. zu wenig Platz, um alle verfügbaren Tools effektiv anzuzeigen. Die Lösung für dieses Problem besteht darin, die Symbolleisten Ihrer Anwendung Benutzer anpassbar zu machen. Anschließend können Benutzer auswählen, nur die Tools anzuzeigen, die Sie benötigen, und Sie können Sie auf eine Weise organisieren, die Ihrem persönlichen Arbeitsstil entspricht.

> [!Note]  
> Symbolleisten in Dialogfeldern können nicht angepasst werden.

 

Um die Anpassung zu aktivieren, schließen Sie beim Erstellen des Toolbar-Steuer Elements das Stil-Flag für die [**CCS \_**](common-control-styles.md) -Anpassung ein. Es gibt zwei grundlegende Ansätze für die Anpassung:

-   Das Anpassungs Dialogfeld. Dieses vom System bereitgestellte Dialogfeld ist der einfachste Ansatz. Der Benutzer erhält eine grafische Benutzeroberfläche, die es Ihnen ermöglicht, Symbole hinzuzufügen, zu löschen oder zu verschieben.
-   Drag & Drop-Tools. Durch das Implementieren der Drag & Drop-Funktionalität können Benutzer Tools an einen anderen Speicherort auf der Symbolleiste verschieben oder löschen, indem Sie Sie aus der Symbolleiste ziehen. Sie bietet Benutzern eine schnelle und einfache Möglichkeit, Ihre Symbolleiste zu organisieren, Sie ermöglicht Ihnen jedoch nicht das Hinzufügen von Tools.

Sie können je nach den Anforderungen der Anwendung entweder einen Ansatz oder beides implementieren. Keines dieser beiden Ansätze für die Anpassung bietet einen integrierten Mechanismus, wie z. b. die Schaltfläche Abbrechen oder rückgängig, um die Symbolleiste in den früheren Zustand zurückzukehren. Sie müssen explizit die ToolBar-Steuerelement-API verwenden, um den Status der Symbolleiste zu speichern. Bei Bedarf können Sie diese gespeicherten Informationen später zum Wiederherstellen des ursprünglichen Zustands der Symbolleiste verwenden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="customization-dialog-box"></a>Dialog Feld "Anpassung"

Das Dialogfeld Anpassung wird vom Symbolleisten-Steuerelement bereitgestellt, um Benutzern eine einfache Möglichkeit zum Hinzufügen, verschieben oder Löschen von Tools zu bieten. Benutzer können Sie starten, indem Sie auf die Symbolleiste doppelklicken. Anwendungen können das Dialogfeld Anpassung Programm gesteuert starten, indem Sie das Symbolleisten-Steuerelement an eine TB-Anpassungs Nachricht senden. [**\_**](tb-customize.md)

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld für die Symbolleisten Anpassung.

![Screenshot eines Fensters mit einer Symbolleiste mit drei Elementen und einem Dialogfeld mit Listen mit den verfügbaren und aktuellen Symbolleisten Schaltflächen](images/tb-customdlg.png)

Die Tools im Listenfeld auf der rechten Seite sind die Tools, die derzeit auf der Symbolleiste angezeigt werden. Zunächst enthält diese Liste die Tools, die Sie beim Erstellen der Symbolleiste angeben. Das Listenfeld Links enthält die Tools, die zur Symbolleiste hinzugefügt werden können. Die Anwendung ist dafür verantwortlich, diese Liste zu füllen (außer mit dem Trennzeichen, das automatisch angezeigt wird).

Das Symbolleisten-Steuerelement benachrichtigt Ihre Anwendung, dass es ein Anpassungs Dialogfeld startet, indem es das übergeordnete Fenster einen [TBN \_ begincustomibenachrichtigungscode](tbn-beginadjust.md) gefolgt von einem [TBN \_ initcustomibenachrichtigungscode](tbn-initcustomize.md) sendet. In den meisten Fällen ist es nicht erforderlich, dass die Anwendung auf diese Benachrichtigungs Codes antwortet. Wenn Sie jedoch nicht möchten, dass das Dialogfeld "Symbolleiste anpassen" eine Hilfe Schaltfläche anzeigt, behandeln Sie TBN \_ initcustomize, indem Sie tbnrf \_ hidehelp zurückgeben.

Anschließend sammelt das Symbolleisten-Steuerelement die Informationen, die benötigt werden, um das Dialogfeld zu initialisieren, indem drei Reihe von Benachrichtigungs Codes in der folgenden Reihenfolge gesendet werden:

-   Ein [TBN \_ queryinsert](tbn-queryinsert.md) -Benachrichtigungs Code für jede Schaltfläche auf der Symbolleiste, um zu bestimmen, wo Schaltflächen eingefügt werden können. Gibt **false** zurück, um zu verhindern, dass eine Schaltfläche links neben der in der Benachrichtigungs Meldung angegebenen Schaltfläche eingefügt wird. Wenn Sie für  alle TBN- \_ queryinsert-Benachrichtigungs Codes false zurückgeben, wird das Dialogfeld nicht angezeigt.
-   Einen [TBN- \_ querydelete](tbn-querydelete.md) -Benachrichtigungs Code für jedes Tool, das sich zurzeit auf der Symbolleiste befindet. Gibt **true** zurück, wenn ein Tool gelöscht werden kann, andernfalls **false** .
-   Eine Reihe von [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Benachrichtigungs Codes, um die Liste der verfügbaren Schaltflächen aufzufüllen. Um der Liste eine Schaltfläche hinzuzufügen, füllen Sie die [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur aus, die mit dem Benachrichtigungs Code übergebenen wird, und geben Sie **true** zurück. Wenn keine weiteren Tools hinzugefügt werden können, geben Sie **false** zurück. Beachten Sie, dass Sie Informationen für Schaltflächen zurückgeben können, die sich bereits auf der Symbolleiste befinden. Diese Schaltflächen werden nicht zur Liste hinzugefügt.

Daraufhin wird das Dialogfeld angezeigt, und der Benutzer kann damit beginnen, die Symbolleiste anzupassen.

Wenn das Dialogfeld geöffnet ist, kann Ihre Anwendung abhängig von den Aktionen des Benutzers eine Vielzahl von Benachrichtigungs Codes empfangen:

-   [TBN \_ Queryinsert](tbn-queryinsert.md). Der Benutzer hat den Speicherort eines Tools auf der Symbolleiste geändert oder ein Tool hinzugefügt. Gibt **false** zurück, um zu verhindern, dass das Tool an dieser Stelle eingefügt wird.
-   [TBN \_ Delta Button](tbn-deletingbutton.md). Der Benutzer ist im Begriff, ein Tool aus der Symbolleiste zu entfernen.
-   [TBN \_ "Custhelp](tbn-custhelp.md)". Der Benutzer hat auf die Schaltfläche "Hilfe" geklickt.
-   [TBN \_ Toolbarchange](tbn-toolbarchange.md). Der Benutzer hat ein Tool hinzugefügt, verschoben oder gelöscht.
-   [TBN \_ Zurücksetzen](tbn-reset.md). Der Benutzer hat auf die Schaltfläche Zurücksetzen geklickt.

Nachdem das Dialogfeld zerstört wurde, empfängt Ihre Anwendung einen [TBN- \_ endanpassungs](tbn-endadjust.md) -Benachrichtigungs Code.

Das folgende Codebeispiel zeigt eine Möglichkeit zum Implementieren der Symbolleisten Anpassung.


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>Drag & Drop-Tools

Benutzer können die Schaltflächen auf einer Symbolleiste auch neu anordnen, indem Sie die UMSCHALTTASTE gedrückt halten und die Schaltfläche an eine andere Position ziehen. Der Drag & Drop-Prozess wird automatisch vom Symbolleisten-Steuerelement behandelt. Sie zeigt ein inaktives Bild der Schaltfläche an, während Sie gezogen wird, und ordnet die Symbolleiste nach dem Ablegen neu an. Benutzer können auf diese Weise keine Schaltflächen hinzufügen, aber Sie können eine Schaltfläche löschen, indem Sie Sie auf der Symbolleiste ablegen.

Obwohl das Symbolleisten-Steuerelement diesen Vorgang normalerweise automatisch durchführt, sendet es die Anwendung auch zwei Benachrichtigungs Codes: [TBN \_ querydelete](tbn-querydelete.md) und [TBN \_ queryinsert](tbn-queryinsert.md). Um den Drag & Drop-Prozess zu steuern, behandeln Sie diese Benachrichtigungs Codes wie folgt:

-   Der [TBN- \_ querydelete](tbn-querydelete.md) -Benachrichtigungs Code wird gesendet, sobald der Benutzer versucht, die Schaltfläche zu verschieben, bevor die Schaltfläche "Ghost" angezeigt wird. Gibt **false** zurück, um zu verhindern, dass die Schaltfläche verschoben wird. Wenn Sie " **true**" zurückgeben, kann der Benutzer das Tool entweder verschieben oder löschen, indem es aus der Symbolleiste entfernt wird. Wenn ein Tool verschoben werden kann, kann es gelöscht werden. Wenn der Benutzer jedoch ein Tool löscht, sendet das Symbolleisten-Steuerelement ihrer Anwendung einen [TBN- \_ Delta-Schalt](tbn-deletingbutton.md) Flächen-Benachrichtigungs Code. an diesem Punkt können Sie auswählen, dass die Schaltfläche an ihrer ursprünglichen Position wieder eingefügt werden soll, wodurch der Löschvorgang abgebrochen wird.
-   Der [TBN- \_ queryinsert](tbn-queryinsert.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer versucht, die Schaltfläche auf der Symbolleiste zu löschen. Um zu verhindern, dass die Schaltfläche, die verschoben wird, Links von der in der Benachrichtigung angegebenen Schaltfläche abgelegt wird, wird **false** zurückgegeben. Dieser Benachrichtigungs Code wird nicht gesendet, wenn der Benutzer das Tool von der Symbolleiste löscht.

Wenn der Benutzer versucht, eine Schaltfläche zu ziehen, ohne auch die UMSCHALTTASTE zu drücken, verarbeitet das Symbolleisten-Steuerelement den Drag & Drop-Vorgang nicht. Die Anwendung sendet jedoch einen [TBN- \_ BeginDrag](tbn-begindrag.md) -Benachrichtigungs Code, um den Start eines Zieh Vorgangs anzugeben, und einen [TBN- \_ EndDrag](tbn-enddrag.md) -Benachrichtigungs Code, um das Ende anzugeben. Wenn Sie diese Art von Drag & amp; Drop aktivieren möchten, muss die Anwendung diese Benachrichtigungs Codes verarbeiten, die erforderliche Benutzeroberfläche bereitstellen und die Symbolleiste so ändern, dass Sie Änderungen widerspiegelt.

### <a name="saving-and-restoring-toolbars"></a>Speichern und Wiederherstellen von Symbolleisten

Wenn Sie eine Symbolleiste anpassen, muss Ihre Anwendung möglicherweise Informationen speichern, damit Sie den ursprünglichen Zustand der Symbolleiste wiederherstellen können. Um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren, senden Sie das Symbolleisten-Steuerelement eine [**TB \_ saverestore**](tb-saverestore.md) -Nachricht, bei der *LPARAM* auf **true** festgelegt Der *LPARAM* -Wert dieser Meldung gibt an, ob Sie einen Speicher-oder Wiederherstellungs Vorgang anfordern. Nachdem die Nachricht gesendet wurde, gibt es zwei Möglichkeiten, den Speicher-/Wiederherstellungsvorgang zu behandeln:

-   Mit den allgemeinen Steuerelementen [Version 4,72](common-control-versions.md) und früher müssen Sie einen [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Handler implementieren. Das Symbolleisten-Steuerelement sendet diesen Benachrichtigungs Code, um Informationen zu den einzelnen Schaltflächen bei der Wiederherstellung anzufordern.
-   Version 5,80 enthält eine Option zum Speichern/Wiederherstellen. Zu Beginn des Prozesses und beim Speichern oder Wiederherstellen der einzelnen Schaltflächen erhält die Anwendung einen [TBN- \_ Save](tbn-save.md) -oder [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigungs Code. Um diese Option verwenden zu können, müssen Sie Benachrichtigungs Handler implementieren, um die Bitmap-und Zustandsinformationen bereitzustellen, die zum erfolgreichen speichern oder Wiederherstellen des Symbolleisten Zustands benötigt werden.

Symbolleisten Zustände werden in einem Datenstrom gespeichert, der aus Blöcken von shelldefinierten Daten besteht, die sich mit Blöcken von Anwendungs definierten Daten abwechseln. Ein Datenblock jedes Typs wird für jede Schaltfläche gespeichert, zusammen mit einem optionalen Block globaler Daten, die Anwendungen am Anfang des Streams platzieren können. Während des Speicher Vorgangs fügt der [TBN- \_ Speicher](tbn-save.md) Handler die Anwendungs definierten Blöcke zum Datenstrom hinzu. Während des Wiederherstellungs Vorgangs liest der [TBN- \_ Wiederherstellungs](tbn-restore.md) Handler jeden Block und übergibt der Shell die Informationen, die er zum Rekonstruieren der Symbolleiste benötigt.

### <a name="how-to-handle-a-tbn_save-notification"></a>Behandeln einer TBN- \_ Speicher Benachrichtigung

Der erste [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code wird zu Beginn des Speicher Vorgangs gesendet. Bevor alle Schaltflächen gespeichert werden, werden die Elemente der [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) -Struktur wie in der folgenden Tabelle dargestellt festgelegt.



| Member       | Einstellung                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Die Menge an Arbeitsspeicher, die für shelldefinierte Daten benötigt wird.                                                                                                                                                                                                                                                                                                |
| **cbuttons** | Die Anzahl der Schaltflächen.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Die berechnete Speichermenge, die für Anwendungs definierte Daten benötigt wird. Normalerweise fügen Sie einige globale Daten und Daten für jede Schaltfläche ein. Fügen Sie diesen Wert zu **cbData** hinzu, und weisen Sie **pData** ausreichend Arbeitsspeicher zu, um die Daten zu speichern.                                                                                                                      |
| **pcurrent** | Das erste nicht verwendete Byte im Datenstrom. Wenn Sie keine globalen Symbolleisten Informationen benötigen, legen Sie **pcurrent**  =  **pData** so fest, dass Sie auf den Anfang des Datenstroms zeigt. Wenn Sie globale Symbolleisten Informationen benötigen, speichern Sie diese bei **pData**, und legen Sie dann **pcurrent** auf den Anfang des nicht verwendeten Teils des Datenstroms fest, bevor Sie zurückkehren. |



 

Wenn Sie einige globale Symbolleisten Informationen hinzufügen möchten, platzieren Sie Sie am Anfang des Datenstroms. Setzen Sie **pcurrent** am Ende der globalen Daten, sodass es auf den Anfang des nicht verwendeten Teils des Datenstroms zeigt, und geben Sie zurück.

Nachdem Sie zurückgegeben haben, beginnt die Shell, Schaltflächen Informationen zu speichern. Sie fügt die shelldefinierten Daten für die erste Schaltfläche bei **pcurrent** hinzu und **verschiebt dann pcurrent** auf den Anfang des nicht verwendeten Teils.

Nachdem jede Schaltfläche gespeichert wurde, wird ein [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code gesendet, und [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) wird zurückgegeben, wobei diese Member wie folgt festgelegt werden.



| Member                       | Einstellung                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Der null basierte Index der Schaltflächen Nummer.                                                                                                                                                                                                                           |
| **pcurrent**                 | Ein Zeiger auf das erste nicht verwendete Byte im Datenstrom. Wenn Sie zusätzliche Informationen über die Schaltfläche speichern möchten, speichern Sie Sie an dem Speicherort, auf den **pcurrent** verweist, und aktualisieren Sie **pcurrent** , um auf den ersten nicht verwendeten Teil des Datenstroms zu verweisen. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Eine [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur, die die Schaltfläche beschreibt, die gespeichert wird.                                                                                                                                                                              |



 

Beim Empfang des Benachrichtigungs Codes sollten Sie alle von Ihnen benötigten Schaltflächen spezifischen Informationen aus [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)extrahieren. Beachten Sie, dass Sie beim Hinzufügen einer Schaltfläche den **dwdata** -Member von **TBBUTTON** verwenden können, um anwendungsspezifische Daten zu speichern. Laden Sie die Daten in den Datenstrom bei **pcurrent**. **Pcurrent** wird an das Ende der Daten zurückgegeben, wobei wiederum auf den Anfang des nicht verwendeten Teils des Streams verwiesen wird und zurückgegeben wird.

Die Shell wechselt dann zur Schaltfläche "weiter", fügt die Informationen zu **pData** hinzu, **verschiebt "pcurrent**", lädt " [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)" und sendet einen weiteren [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code. Dieser Prozess wird fortgesetzt, bis alle Schaltflächen gespeichert wurden.

### <a name="restoring-saved-toolbars"></a>Wiederherstellen gespeicherter Symbolleisten

Der Wiederherstellungs Vorgang kehrt im Grunde den Speicher Prozess um. Zu Beginn empfängt Ihre Anwendung einen [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigungs Code mit dem **iItem** -Member der [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) -Struktur, die auf – 1 festgelegt ist. Der **cbData** -Member wird auf die Größe von **pData** festgelegt, und die **cbuttons** werden auf die Anzahl der Schaltflächen festgelegt.

Der Benachrichtigungs Handler sollte die globalen Informationen, die beim Speichern am Anfang von **pData** platziert wurden, extrahieren und die **pcurrent** -Funktion bis zum Anfang des ersten Blocks von shelldefinierten Daten voranbringen. Legen Sie **cbytesperrecord** auf die Größe der Datenblöcke fest, die Sie zum Speichern der Schaltflächen Daten verwendet haben. Legen Sie **cbuttons** auf die Anzahl der Schaltflächen fest, und geben Sie zurück.

Der nächste [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) ist für die erste Schaltfläche. Der **pcurrent** -Member zeigt auf den Anfang des ersten Blocks von Schaltflächen Daten, und **iItem** wird auf den Schaltflächen Index festgelegt. Extrahieren Sie diese Daten und **pcurrent**. Laden Sie die Daten in [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), und geben Sie zurück. Um eine Schaltfläche auf der wiederhergestellten Symbolleiste auszulassen, legen Sie den **idcommand** -Member von **TBBUTTON** auf NULL fest. Die Shell wiederholt den Vorgang für die verbleibenden Schaltflächen. Zusätzlich zu den Nachrichten [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) und **nmtbrestore** können Sie auch Nachrichten wie z. [b. TBN \_ Reset](tbn-reset.md) zum Speichern und Wiederherstellen einer Symbolleiste verwenden.

Im folgenden Codebeispiel wird eine Symbolleiste vor der Anpassung gespeichert und wieder hergestellt, wenn die Anwendung eine [TBN \_ ](tbn-reset.md) -Zurücksetzungs Nachricht empfängt.


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[**Bild-/Indexwerte der Symbolleiste Standard**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




