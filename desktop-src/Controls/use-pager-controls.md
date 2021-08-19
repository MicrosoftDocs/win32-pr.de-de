---
title: Verwenden von Pager-Steuerelementen
description: In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b917943f5f86498bb3cbea2c58842049c4618caf64a66a6b8db1cb2ab86a315b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828641"
---
# <a name="how-to-use-pager-controls"></a>Verwenden von Pager-Steuerelementen

In diesem Abschnitt wird beschrieben, wie Sie das Pager-Steuerelement in Ihrer Anwendung implementieren.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="initialize-a-pager-control"></a>Initialisieren eines Pager-Steuerelements

Um das Pager-Steuerelement verwenden zu können, müssen Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen, bei der das FLAG FÜR DIE KLASSE DER KLASSE FÜR DIE KLASSE DER KLASSE FÜR DIE \_ \_ [**INITCOMMONCONTROLSEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) im **dwICC-Member** festgelegt ist.

### <a name="create-a-pager-control"></a>Erstellen eines Pager-Steuerelements

Verwenden Sie [**CreateWindow oder**](/windows/desktop/api/winuser/nf-winuser-createwindowa) die [**CreateWindowEx-API,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) um ein Pager-Steuerelement zu erstellen. Der Klassenname für das Steuerelement ist [**WC \_ PAGESCROLLER,**](common-control-window-classes.md)der in Commctrl.h definiert ist. Der [**PGS \_ HORZ-Stil**](pager-control-styles.md) wird verwendet, um einen horizontalen Pager zu erstellen, und der [**PGS \_ VERT-Stil**](pager-control-styles.md) wird verwendet, um einen vertikalen Pager zu erstellen. Da es sich um ein untergeordnetes Steuerelement handelt, sollte auch [**das WS \_ CHILD-Format**](/windows/desktop/winmsg/window-styles) verwendet werden.

Nachdem das Pager-Steuerelement erstellt wurde, sollten Sie ihm wahrscheinlich ein enthaltenes Fenster zuweisen. Wenn das enthaltene Fenster ein untergeordnetes Fenster ist, sollten Sie das untergeordnete Fenster zu einem untergeordneten Fenster des Pager-Steuerelements machen, damit größe und position richtig berechnet werden. Anschließend weisen Sie das Fenster mit der [**PGM \_ SETCHILD-Meldung**](pgm-setchild.md) dem Pager-Steuerelement zu. Beachten Sie, dass das übergeordnete Fenster des enthaltenen Fensters durch diese Meldung nicht geändert wird. es weist einfach das enthaltene Fenster zu. Wenn das enthaltene Fenster eines der gängigen Steuerelemente ist, muss es über den [**CCS \_ NORESIZE-Stil**](common-control-styles.md) verfügen, um zu verhindern, dass das Steuerelement versucht, sich selbst in die Größe des Pagersteuerelementes zu ändern.

### <a name="process-pager-control-notifications"></a>Verarbeiten von Pager-Steuerelementbenachrichtigungen

Es ist mindestens erforderlich, die [PGN-CALCSIZE-Benachrichtigung \_ zu](pgn-calcsize.md) verarbeiten. Wenn Sie diese Benachrichtigung nicht verarbeiten und einen Wert für die Breite oder Höhe eingeben, werden die Bildlaufpfeile im Pager-Steuerelement nicht angezeigt. Dies liegt daran, dass das Pager-Steuerelement die in der PGN-CALCSIZE-Benachrichtigung angegebene Breite oder Höhe verwendet, um die "ideale" Größe des enthaltenen \_ Fensters zu bestimmen.

Im folgenden Beispiel wird veranschaulicht, wie sie den [PGN \_ CALCSIZE-Benachrichtigungsfall](pgn-calcsize.md) verarbeiten. In diesem Beispiel ist das enthaltene Fenster ein Symbolleisten-Steuerelement, das eine unbekannte Anzahl von Schaltflächen in einer unbekannten Größe enthält. Das Beispiel zeigt, wie die [**TB \_ GETMAXSIZE-Nachricht verwendet**](tb-getmaxsize.md) wird, um die Größe aller Elemente in der Symbolleiste zu bestimmen. Im Beispiel wird dann die Breite aller Elemente in das **iWidth-Member** der [**NMPGCALCSIZE-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) platziert, das an die Benachrichtigung übergeben wird.


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

[Verwenden von Pagersteuerelementen](using-pager-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 