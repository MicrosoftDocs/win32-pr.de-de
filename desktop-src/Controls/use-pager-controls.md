---
title: Verwenden von Pager-Steuerelementen
description: In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039690"
---
# <a name="how-to-use-pager-controls"></a>Verwenden von Pager-Steuerelementen

In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="initialize-a-pager-control"></a>Pager-Steuerelement initialisieren

Um das Pager-Steuerelement zu verwenden, müssen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion mit dem \_ \_ im **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur festgelegten Flag für die-Klasse "pagescroller Class" aufzurufen.

### <a name="create-a-pager-control"></a>Erstellen eines Pager-Steuer Elements

Verwenden Sie die API " [**kreatewindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", um ein Pager-Steuerelement zu erstellen. Der Klassenname für das Steuerelement ist " [**WC \_ pagescroller**](common-control-window-classes.md)", das in "kommctrl. h" definiert ist. Der [**PGS- \_ Horz**](pager-control-styles.md) -Stil wird zum Erstellen eines horizontalen Pager verwendet, und der PGS-Format " [**\_ Vert**](pager-control-styles.md) " wird zum Erstellen eines vertikalen Pager verwendet. Da es sich hierbei um ein untergeordnetes Steuerelement handelt, sollte auch der untergeordnete [**WS \_**](/windows/desktop/winmsg/window-styles) -Stil verwendet werden.

Nachdem das Pager-Steuerelement erstellt wurde, möchten Sie wahrscheinlich ein enthaltenes Fenster zuweisen. Wenn das enthaltene Fenster ein untergeordnetes Fenster ist, sollten Sie das untergeordnete Fenster als untergeordnetes Element des Pager-Steuer Elements festlegen, sodass Größe und Position ordnungsgemäß berechnet werden. Anschließend weisen Sie das Fenster dem Pager-Steuerelement mit der [**PGM- \_ setchild**](pgm-setchild.md) -Nachricht zu. Beachten Sie, dass diese Meldung das übergeordnete Fenster des enthaltenen Fensters nicht tatsächlich ändert. Er weist lediglich das enthaltene Fenster zu. Wenn das enthaltene Fenster eines der allgemeinen Steuerelemente ist, muss es den [**CCS \_ NORESIZE**](common-control-styles.md) -Stil aufweisen, um zu verhindern, dass das Steuerelement versucht, die Größe der Größe des Pager-Steuer Elements zu ändern.

### <a name="process-pager-control-notifications"></a>Pager-Steuerelement Benachrichtigungen verarbeiten

Es ist mindestens erforderlich, dass die [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung verarbeitet wird. Wenn Sie diese Benachrichtigung nicht verarbeiten und einen Wert für die Breite oder Höhe eingeben, werden die Bild Lauf Pfeile im Pager-Steuerelement nicht angezeigt. Dies liegt daran, dass das Pager-Steuerelement die Breite oder Höhe verwendet, die in der PGN \_ calcsize-Benachrichtigung angegeben ist, um die "ideale" Größe des enthaltenen Fensters zu ermitteln.

Im folgenden Beispiel wird veranschaulicht, wie die [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigungs Fälle verarbeitet werden. In diesem Beispiel ist das enthaltene Fenster ein Symbolleisten-Steuerelement, das eine unbekannte Anzahl von Schaltflächen mit einer unbekannten Größe enthält. Im Beispiel wird gezeigt, wie die [**TB \_ getmaxsize**](tb-getmaxsize.md) -Nachricht verwendet wird, um die Größe aller Elemente in der Symbolleiste zu ermitteln. Im Beispiel wird dann die Breite aller Elemente in den **iWidth** -Member der [**nmpgcalcsize**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) -Struktur eingefügt, die an die Benachrichtigung übergeben wird.


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Pager-Steuerelementen](using-pager-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 