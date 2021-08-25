---
title: Anpassen von Symbolleisten
description: Die Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen komfortablen Zugriff auf die Programmfunktionalität zu ermöglichen.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f098880676fc0404df2a68694dc80b8601c21926d94ff594029321bafb1528a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929545"
---
# <a name="how-to-customize-toolbars"></a>Anpassen von Symbolleisten

Die Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen komfortablen Zugriff auf die Programmfunktionalität zu ermöglichen. Statische Symbolleisten haben jedoch einige Nachteile, z. B. zu wenig Platz, um alle verfügbaren Tools effektiv anzuzeigen. Die Lösung für dieses Problem besteht in der Anpassung der Symbolleisten Ihrer Anwendung an den Benutzer. Benutzer können dann nur die tools anzeigen, die sie benötigen, und sie können sie so organisieren, dass sie ihrem persönlichen Arbeitsstil entspricht.

> [!Note]  
> Symbolleisten in Dialogfeldern können nicht angepasst werden.

 

Um die Anpassung zu aktivieren, fügen Sie beim Erstellen des Symbolleisten-Steuerelements das [**\_ CCS-STYLE-Styleflag**](common-control-styles.md) für allgemeine Steuerelemente ein. Es gibt zwei grundlegende Ansätze für die Anpassung:

-   Das Anpassungsdialogfeld. Dieses vom System bereitgestellte Dialogfeld ist der einfachste Ansatz. Es bietet Benutzern eine grafische Benutzeroberfläche, mit der sie Symbole hinzufügen, löschen oder verschieben können.
-   Ziehen und Ablegen von Tools. Durch die Implementierung von Drag & Drop-Funktionen können Benutzer Tools an einen anderen Speicherort auf der Symbolleiste verschieben oder löschen, indem sie sie von der Symbolleiste ziehen. Es bietet Benutzern eine schnelle und einfache Möglichkeit, ihre Symbolleiste zu organisieren, erlaubt ihnen jedoch nicht das Hinzufügen von Tools.

Abhängig von den Anforderungen der Anwendung können Sie einen oder beide Ansätze implementieren. Keiner dieser beiden Anpassungsansätze bietet einen integrierten Mechanismus, z. B. die Schaltfläche Abbrechen oder Rückgängig, um die Symbolleiste in ihren früheren Zustand zurück zu kehren. Sie müssen explizit die SYMBOLLEISTEN-Steuerelement-API verwenden, um den präcustomization-Zustand der Symbolleiste zu speichern. Bei Bedarf können Sie diese gespeicherten Informationen später verwenden, um den ursprünglichen Zustand der Symbolleiste wiederherzustellen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="customization-dialog-box"></a>Anpassungsdialogfeld

Das Anpassungsdialogfeld wird vom Symbolleisten-Steuerelement bereitgestellt, um Benutzern eine einfache Möglichkeit zum Hinzufügen, Verschieben oder Löschen von Tools zu bieten. Benutzer können sie starten, indem sie auf die Symbolleiste doppelklicken. Anwendungen können das Anpassungsdialogfeld programmgesteuert starten, indem sie dem Symbolleisten-Steuerelement eine [**TB \_ CUSTOMIZE-Meldung**](tb-customize.md) senden.

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld zur Anpassung der Symbolleiste.

![Screenshot eines Fensters mit einer Symbolleiste mit drei Element und einem Dialogfeld mit Listen der verfügbaren und aktuellen Symbolleistenschaltflächen](images/tb-customdlg.png)

Die Tools im Listenfeld auf der rechten Seite befinden sich derzeit auf der Symbolleiste. Zunächst enthält diese Liste die Tools, die Sie beim Erstellen der Symbolleiste angeben. Das Listenfeld auf der linken Seite enthält die Tools, die zur Symbolleiste hinzugefügt werden können. Ihre Anwendung ist für das Auflisten dieser Liste verantwortlich (mit Dem Trennzeichen, das automatisch angezeigt wird).

Das Symbolleisten-Steuerelement benachrichtigt Ihre Anwendung, dass ein Anpassungsdialogfeld gestartet wird, indem es dem übergeordneten Fenster einen [TBN \_ BEGINADJUST-Benachrichtigungscode](tbn-beginadjust.md) gefolgt von einem [TBN \_ INITCUSTOMIZE-Benachrichtigungscode](tbn-initcustomize.md) sendet. In den meisten Fällen muss die Anwendung nicht auf diese Benachrichtigungscodes reagieren. Wenn sie jedoch nicht möchten, dass im Dialogfeld Symbolleiste anpassen eine Hilfeschaltfläche angezeigt wird, behandeln Sie TBN \_ INITCUSTOMIZE, indem Sie TBNRF \_ HIDEHELP zurückgeben.

Das Symbolleisten-Steuerelement sammelt dann die Informationen, die es zum Initialisieren des Dialogfelds benötigt, indem es drei Benachrichtigungscodes in der folgenden Reihenfolge sendet:

-   Ein [TBN \_ QUERYINSERT-Benachrichtigungscode](tbn-queryinsert.md) für jede Schaltfläche auf der Symbolleiste, um zu bestimmen, wo Schaltflächen eingefügt werden können. Geben **Sie FALSE** zurück, um zu verhindern, dass eine Schaltfläche links neben der in der Benachrichtigungsmeldung angegebenen Schaltfläche eingefügt wird. Wenn Sie **FALSE an** alle TBN \_ QUERYINSERT-Benachrichtigungscodes zurückgeben, wird das Dialogfeld nicht angezeigt.
-   Ein [TBN \_ QUERYDELETE-Benachrichtigungscode](tbn-querydelete.md) für jedes Tool, das sich derzeit auf der Symbolleiste befindet. Gibt **TRUE** zurück, wenn ein Tool gelöscht werden kann, oder **FALSE,** wenn dies nicht der Fall ist.
-   Eine Reihe von [TBN \_ GETBUTTONINFO-Benachrichtigungscodes](tbn-getbuttoninfo.md) zum Auffüllen der Liste der verfügbaren Schaltflächen. Um der Liste eine Schaltfläche hinzuzufügen, füllen Sie die [**NMTOOLBAR-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) aus, die mit dem Benachrichtigungscode übergeben wird, und geben **SIE TRUE zurück.** Wenn Sie keine Tools mehr hinzufügen müssen, geben Sie **FALSE zurück.** Beachten Sie, dass Sie Informationen für Schaltflächen zurückgeben können, die sich bereits auf der Symbolleiste befinden. diese Schaltflächen werden der Liste nicht hinzugefügt.

Das Dialogfeld wird dann angezeigt, und der Benutzer kann damit beginnen, die Symbolleiste anzupassen.

Wenn das Dialogfeld geöffnet ist, kann Ihre Anwendung abhängig von den Aktionen des Benutzers eine Vielzahl von Benachrichtigungscodes empfangen:

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). Der Benutzer hat den Speicherort eines Tools auf der Symbolleiste geändert oder ein Tool hinzugefügt. Geben **Sie FALSE** zurück, um zu verhindern, dass das Tool an dieser Position eingefügt wird.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). Der Benutzer wird ein Tool von der Symbolleiste entfernen.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). Der Benutzer hat auf die Schaltfläche Hilfe geklickt.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). Der Benutzer hat ein Tool hinzugefügt, verschoben oder gelöscht.
-   [TBN \_ SETZEN SIE ZURÜCK.](tbn-reset.md) Der Benutzer hat auf die Schaltfläche Zurücksetzen geklickt.

Nachdem das Dialogfeld zerstört wurde, erhält Ihre Anwendung einen [ \_ TBN-ENDADJUST-Benachrichtigungscode.](tbn-endadjust.md)

Das folgende Codebeispiel zeigt eine Möglichkeit, die Anpassung der Symbolleiste zu implementieren.


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



### <a name="dragging-and-dropping-tools"></a>Tools zum Ziehen und Löschen

Benutzer können die Schaltflächen auf einer Symbolleiste auch neu anordnen, indem sie die UMSCHALTTASTE drücken und die Schaltfläche an eine andere Position ziehen. Der Drag & Drop-Prozess wird automatisch vom Symbolleisten-Steuerelement verarbeitet. Sie zeigt ein ingesenkte Bild der Schaltfläche an, während sie gezogen wird, und ordnet die Symbolleiste neu an, nachdem sie gelöscht wurde. Benutzer können auf diese Weise keine Schaltflächen hinzufügen, aber sie können eine Schaltfläche löschen, indem sie sie auf der Symbolleiste ablegen.

Obwohl das Symbolleisten-Steuerelement diesen Vorgang normalerweise automatisch abfragt, sendet es ihrer Anwendung auch zwei Benachrichtigungscodes: [TBN \_ QUERYDELETE](tbn-querydelete.md) und [TBN \_ QUERYINSERT](tbn-queryinsert.md). Um den Drag & Drop-Prozess zu steuern, behandeln Sie diese Benachrichtigungscodes wie folgt:

-   Der [TBN \_ QUERYDELETE-Benachrichtigungscode](tbn-querydelete.md) wird gesendet, sobald der Benutzer versucht, die Schaltfläche zu verschieben, bevor die in ghost-Schaltfläche angezeigt wird. Geben Sie **FALSE** zurück, um zu verhindern, dass die Schaltfläche verschoben wird. Wenn Sie **TRUE zurückgeben,** kann der Benutzer das Tool entweder verschieben oder löschen, indem er es aus der Symbolleiste löscht. Wenn ein Tool verschoben werden kann, kann es gelöscht werden. Wenn der Benutzer jedoch ein Tool löscht, sendet das Symbolleisten-Steuerelement ihrer Anwendung einen [TBN DELETINGBUTTON-Benachrichtigungscode. \_ ](tbn-deletingbutton.md) An diesem Punkt können Sie die Schaltfläche am ursprünglichen Speicherort erneut setzen und dadurch den Löschvorgang abbrechen.
-   Der [TBN \_ QUERYINSERT-Benachrichtigungscode](tbn-queryinsert.md) wird gesendet, wenn der Benutzer versucht, die Schaltfläche auf der Symbolleiste zu löschen. Um zu verhindern, dass die schaltfläche, die verschoben wird, links neben der in der Benachrichtigung angegebenen Schaltfläche gelöscht wird, geben Sie **FALSE zurück.** Dieser Benachrichtigungscode wird nicht gesendet, wenn der Benutzer das Tool von der Symbolleiste löscht.

Wenn der Benutzer versucht, eine Schaltfläche zu ziehen, ohne auch die UMSCHALTTASTE zu drücken, verarbeitet das Symbolleisten-Steuerelement den Drag & Drop-Vorgang nicht. Sie sendet Ihrer Anwendung jedoch einen [TBN BEGINDRAG-Benachrichtigungscode, \_ ](tbn-begindrag.md) um den Beginn eines Ziehvorgang anzugeben, und einen [TBN ENDDRAG-Benachrichtigungscode, \_ ](tbn-enddrag.md) um das Ende anzugeben. Wenn Sie diese Form von Drag & Drop aktivieren möchten, muss Ihre Anwendung diese Benachrichtigungscodes verarbeiten, die erforderliche Benutzeroberfläche bereitstellen und die Symbolleiste so ändern, dass alle Änderungen widergestrichen werden.

### <a name="saving-and-restoring-toolbars"></a>Speichern und Wiederherstellen von Symbolleisten

Beim Anpassen einer Symbolleiste muss Ihre Anwendung möglicherweise Informationen speichern, damit Sie den ursprünglichen Zustand der Symbolleiste wiederherstellen können. Um das Speichern oder Wiederherstellen eines Symbolleistenzustands zu initiieren, senden Sie dem Symbolleisten-Steuerelement eine [**\_ SAVERESTORE-Tb-Nachricht,**](tb-saverestore.md) bei der *lParam* auf **TRUE festgelegt ist.** Der *lParam-Wert* dieser Meldung gibt an, ob Sie einen Speicher- oder Wiederherstellungsvorgang anfordern. Nachdem die Nachricht gesendet wurde, gibt es zwei Möglichkeiten, den Speicher-/Wiederherstellungsvorgang zu verarbeiten:

-   Mit allgemeinen [Steuerelementen, Version 4.72](common-control-versions.md) und früher, müssen Sie einen [TBN \_ GETBUTTONINFO-Handler](tbn-getbuttoninfo.md) implementieren. Das Symbolleisten-Steuerelement sendet diesen Benachrichtigungscode, um Während der Wiederherstellung Informationen zu den einzelnen Schaltflächen an fordern zu können.
-   Version 5.80 enthält eine Option zum Speichern/Wiederherstellen. Zu Beginn des Prozesses und beim Speichern oder Wiederherstellen jeder Schaltfläche erhält Ihre Anwendung den TBN-Benachrichtigungscode [ \_ SAVE](tbn-save.md) oder [TBN \_ RESTORE.](tbn-restore.md) Um diese Option verwenden zu können, müssen Sie Benachrichtigungshandler implementieren, um die Bitmap- und Zustandsinformationen bereitstellen zu können, die zum erfolgreichen Speichern oder Wiederherstellen des Symbolleistenzustands erforderlich sind.

Symbolleistenzustände werden in einem Datenstrom gespeichert, der aus Blöcken von shelldefinierten Daten besteht, die sich mit Blöcken anwendungsdefinierter Daten abwechseln. Ein Datenblock jedes Typs wird für jede Schaltfläche gespeichert, zusammen mit einem optionalen Block globaler Daten, die Anwendungen am Anfang des Streams platzieren können. Während des Speichervorgangs fügt Der [TBN \_ SAVE-Handler](tbn-save.md) dem Datenstrom die anwendungsdefinierten Blöcke hinzu. Während des Wiederherstellungsprozesses liest der [TBN \_ RESTORE-Handler](tbn-restore.md) jeden Block und gibt der Shell die Informationen, die sie zum Rekonstruieren der Symbolleiste benötigt.

### <a name="how-to-handle-a-tbn_save-notification"></a>Behandeln einer \_ TBN-SAVE-Benachrichtigung

Der erste [TBN SAVE-Benachrichtigungscode \_ ](tbn-save.md) wird zu Beginn des Speichervorgangs gesendet. Bevor Schaltflächen gespeichert werden, werden die Member der [**NMTBSAVE-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) wie in der folgenden Tabelle gezeigt festgelegt.



| Member       | Einstellung                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Die Menge an Arbeitsspeicher, die für shelldefinierte Daten benötigt wird.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Die Anzahl der Schaltflächen.                                                                                                                                                                                                                                                                                                                             |
| **Pdata**    | Die berechnete Menge an Arbeitsspeicher, die für anwendungsdefinierte Daten benötigt wird. In der Regel fügen Sie einige globale Daten sowie Daten für jede Schaltfläche ein. Fügen Sie diesen Wert **cbData** hinzu, und weisen Sie **pData** genügend Arbeitsspeicher zu, um alles zu speichern.                                                                                                                      |
| **pCurrent** | Das erste nicht verwendete Byte im Datenstrom. Wenn Sie keine globalen Symbolleisteninformationen benötigen, legen Sie **pCurrent**  =  **pData** so fest, dass es auf den Anfang des Datenstroms zeigt. Wenn Sie globale Symbolleisteninformationen benötigen, speichern Sie sie unter **pData,** und legen Sie **pCurrent** vor der Rückgabe auf den Anfang des nicht verwendeten Teils des Datenstroms fest. |



 

Wenn Sie einige globale Symbolleisteninformationen hinzufügen möchten, fügen Sie sie am Anfang des Datenstroms ein. Stellen **Sie pCurrent** an das Ende der globalen Daten, sodass sie auf den Anfang des nicht verwendeten Teils des Datenstroms zeigt, und geben Sie zurück.

Nachdem Sie zurückgegeben haben, beginnt die Shell mit dem Speichern von Schaltflächeninformationen. Sie fügt die shelldefinierten Daten für die erste Schaltfläche bei **pCurrent** hinzu und setzt **pCurrent** dann auf den Anfang des nicht verwendeten Teils.

Nachdem jede Schaltfläche gespeichert wurde, wird ein [TBN \_ SAVE-Benachrichtigungscode](tbn-save.md) gesendet, und [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) wird zurückgegeben, wobei diese Member wie folgt festgelegt sind.



| Member                       | Einstellung                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Der nullbasierte Index der Schaltflächennummer.                                                                                                                                                                                                                           |
| **pCurrent**                 | Ein Zeiger auf das erste nicht verwendete Byte im Datenstrom. Wenn Sie zusätzliche Informationen über die Schaltfläche speichern möchten, speichern Sie sie an der Position, auf die **pCurrent** zeigt, und aktualisieren **Sie pCurrent** so, dass sie auf den ersten nicht verwendeten Teil des Datenstroms danach zeigt. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Eine [**TBBUTTON-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) die die zu speichernde Schaltfläche beschreibt.                                                                                                                                                                              |



 

Wenn Sie den Benachrichtigungscode erhalten, sollten Sie alle benötigten schaltflächenspezifischen Informationen aus [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)extrahieren. Denken Sie daran, dass Sie beim Hinzufügen einer Schaltfläche den **dwData-Member** von **TBBUTTON** verwenden können, um anwendungsspezifische Daten zu speichern. Laden Sie Ihre Daten unter **pCurrent** in den Datenstrom. Setzen **Sie pCurrent** an das Ende Ihrer Daten, zeigen Sie erneut auf den Anfang des nicht verwendeten Teils des Streams, und geben Sie zurück.

Die Shell wechselt dann zur nächsten Schaltfläche, fügt ihre Informationen **zu pData** hinzu, erhöht **pCurrent,** lädt [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)und sendet einen weiteren [TBN SAVE-Benachrichtigungscode. \_](tbn-save.md) Dieser Vorgang wird fortgesetzt, bis alle Schaltflächen gespeichert sind.

### <a name="restoring-saved-toolbars"></a>Wiederherstellen gespeicherter Symbolleisten

Der Wiederherstellungsprozess kehrt den Speichervorgang im Grunde um. Am Anfang erhält Ihre Anwendung einen [TBN \_ RESTORE-Benachrichtigungscode,](tbn-restore.md) wobei der **iItem-Member** der [**NMTBRESTORE-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) auf –1 festgelegt ist. Der **cbData-Member** wird auf die Größe von **pData** festgelegt, und **cButtons** wird auf die Anzahl der Schaltflächen festgelegt.

Der Benachrichtigungshandler sollte die globalen Informationen extrahieren, die während des Speicherns am Anfang von **pData** platziert wurden, und **pCurrent** an den Anfang des ersten Blocks von shelldefinierten Daten setzen. Legen Sie **cBytesPerRecord** auf die Größe der Datenblöcke fest, die Sie zum Speichern der Schaltflächendaten verwendet haben. Legen Sie **cButtons** auf die Anzahl der Schaltflächen fest, und geben Sie zurück.

Der nächste [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) ist für die erste Schaltfläche vorgesehen. Der **pCurrent-Member** zeigt auf den Anfang Ihres ersten Blockes von Schaltflächendaten, und **iItem** wird auf den Schaltflächenindex festgelegt. Extrahieren Sie diese Daten, und bringen **Sie pCurrent voran.** Laden Sie die Daten in [**TBBUTTON,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)und geben Sie zurück. Um eine Schaltfläche aus der wiederhergestellten Symbolleiste auszulassen, legen Sie das **idCommand-Element** von **TBBUTTON** auf 0 (null) fest. Die Shell wiederholt den Vorgang für die verbleibenden Schaltflächen. Zusätzlich zu den [**NMTBSAVE-**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) und **NMTBRESTORE-Nachrichten** können Sie auch Nachrichten wie [TBN \_ RESET](tbn-reset.md) verwenden, um eine Symbolleiste zu speichern und wiederherzustellen.

Im folgenden Codebeispiel wird eine Symbolleiste vor der Anpassung gespeichert und wiederhergestellt, wenn die Anwendung eine [ \_ TBN-ZURÜCKSETZUNGsmeldung](tbn-reset.md) empfängt.


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

[Verwenden von Symbolleistensteuerelementen](using-toolbar-controls.md)
</dt> <dt>

[**Symbolleiste Standardschaltfläche – Bildindexwerte**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




