---
title: CMainWindow
description: Der folgende Beispielcode veranschaulicht dieses Verfahren.
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- CMainWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e9cb538246dfa6931a2f036ba75cab5e962a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341825"
---
# <a name="cmainwindow"></a>CMainWindow

Das Microsoft Windows-Betriebssystem übersetzt die folgenden Benutzeraktionen in Standardfenster Meldungen und sendet Sie an die Haupt Prozedur in der **stoclien** -Anwendung:

-   Der Benutzer klickt auf die linke Maustaste oder auf Tablet-Geräte, um eine Zeilen Zeichnungs Sequenz zu initiieren.
-   Der Benutzer klickt auf die Schaltfläche und bewegt die Schaltfläche und bewegt die Maus, um eine Linie zu zeichnen.
-   Die Sequenz wird beendet, wenn die linke Maustaste losgelassen wird.

Der folgende Beispielcode veranschaulicht dieses Verfahren.

## <a name="cmainwindowwindowproc-stocliencpp"></a>CMainWindow:: WindowProc (stoclien). CPP


```C++
LRESULT CMainWindow::WindowProc(
            UINT uMsg,
            WPARAM wParam,
            LPARAM lParam)
  {
    LRESULT lResult = FALSE;

    switch (uMsg)
    {
      case WM_CREATE:
        break;

      case WM_ACTIVATE:
        // A mouse click reactivates the paint procedure.
        // This is used to paint a new window when a user
        // selects a portion of the STOCLIEN window that is 
        // visible beneath another window. This message is  
        // sent in the WindowProc handle.
        if (WA_CLICKACTIVE == LOWORD(wParam))
          m_pGuiPaper->PaintWin();
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;

      case WM_SIZE:
        // Handle a resize of this window.
        m_wWidth = LOWORD(lParam);
        m_wHeight = HIWORD(lParam);
        // Inform CGuiPaper of the change.
        m_pGuiPaper->Resize(m_wWidth, m_wHeight);
        break;

      case WM_PAINT:
        // This is a message to repaint the window.
        {
          PAINTSTRUCT ps;

          if(BeginPaint(m_hWnd, &ps))
            EndPaint(m_hWnd, &ps);

          m_pGuiPaper->PaintWin();
        }
        break;

      case WM_LBUTTONDOWN:
        // Start sequence of ink drawing to the paper.
        m_pGuiPaper->InkStart(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_MOUSEMOVE:
        // Draw inking sequence data.
        m_pGuiPaper->InkDraw(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_LBUTTONUP:
        // Stop an ink drawing sequence.
        m_pGuiPaper->InkStop(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_COMMAND:
        // Dispatch and handle any Menu command messages received.
        lResult = DoMenu(wParam, lParam);
        break;

      case WM_CHAR:
        if (wParam == 0x1b)
        {
          // Exit this application if user presses the ESC key.
          ::PostMessage(m_hWnd, WM_CLOSE, 0, 0);
        }
        break;

      case WM_CLOSE:
        // The user selected Close on the main window System menu
        // or Exit on the File menu.
        // If there is unsaved ink data, then prompt
        // the user. If the user cancels, do not close the window.
        if (IDCANCEL == m_pGuiPaper->AskSave())
          break;
      case WM_QUIT:
        // When exiting the application, close any associated help
        // windows.
        // ::WinHelp(m_hWnd, m_szHelpFile, HELP_QUIT, 0);
      default:
        // If there are any messages that have not been handled,
        // send them to the default window procedure.
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;
    }

    return(lResult);
  }
```



Eine Zeilen Zeichnungs Sequenz beginnt, wenn die WM- \_ lbuttondown-Nachricht Maus Positionsdaten übermittelt.

CMainWindow weist einen Zeiger auf das cguipaper-Objekt auf und ruft die [**cguipaper:: inkstart**](cguipaper-methods.md) -Methode auf, um die Zeilen Zeichnungs Sequenz zu starten.

Wenn die Maus zu zeichnen bewegt wird, wird eine Sequenz von separaten **WM- \_ MouseMove** -Nachrichten, die Maus Positionsdaten enthalten, für die [cguipaper:: inkdraw](cguipaper-methods.md) -Methode bereitgestellt.

Wenn die linke Maustaste losgelassen wird, wird die **WM \_ lbuttonup** -Meldung empfangen. Die [cguipaper:: inkstopp](cguipaper-methods.md) -Methode beendet die Zeilen Zeichnungs Sequenz.

 

 




