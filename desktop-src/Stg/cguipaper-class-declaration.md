---
title: CGuiPaper-Klassendeklaration
description: CGuiPaper-Klassendeklaration
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d684618eea78247b94ed03223cfce45d2cc713f5507b1e290731d3451212b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663520"
---
# <a name="cguipaper-class-declaration"></a>CGuiPaper-Klassendeklaration

Im Folgenden finden Sie die **CGuiPaper-Klassendeklaration** von GUIPAPER.H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**CGuiPaper verwaltet** die aktuellen GUI-Eigenschaften für das Zeichnungsdokument. Die **Member m \_ crInkColor,** **m \_ crInkWidth** und **m \_ WinRect** enthalten Werte für die aktuelle Ink-Farbe, Die Breite der Ink-Farbe und das Zeichenrechteck. Das **m \_ hWnd-Member** speichert das Handle im Fenster, in dem das Malen erfolgt.

Das eigentliche Malen von Bildern erfolgt mithilfe eines Handles für einen Gerätekontext, der im **Member m \_ hDC gespeichert ist.** Ein Handle für den aktuellen Zeichnungsstift wird im Member **m \_ hPen beibehalten.** Der Stift wird zerstört und neu erstellt, wenn seine Farbe oder Breite vom Benutzer geändert wird.

Die **Member \_ m pCOPaperSink** und **m \_ dwPaperSink** enthalten Werte, die zum Herstellen einer Verbindung mit COPaper erforderlich sind, um eingehende Benachrichtigungen über die [**IPaperSink-Schnittstelle zu**](ipapersink-methods.md) empfangen. Member **m \_ bDirty enthält** ein Flag, das angibt, dass der Benutzer die Zeichnung geändert hat und die in der Datei gespeicherten Daten nicht mehr wiedergibt.

Member **m \_ pIPaper enthält** den Hauptschnittstellenzeiger auf das COPaper-Objekt. Auf alle COPaper-Funktionen wird über diesen Zeiger zugegriffen.

Das **m \_ nLockKey-Member** wird verwendet, um ein Clientsperrschema zu unterstützen, das mit mehreren Clients verwendet wird, um einem Client exklusiven Zugriff auf ein freigegebenes COPaper-Objekt zu ermöglichen. COPaper weist **m \_ nLockKey** während eines [**IPaper**](ipaper-methods.md)**::** Lock-Aufrufs zu und wird vom Client in nachfolgenden Aufrufen an COPaper als Parameter übergeben. COPaper führt die Arbeit in diesen Aufrufen nur aus, wenn der übergebene Sperresschlüssel mit dem Schlüssel stimmt, der zuletzt von COPaper an einen Client übergeben wurde.

Member **m \_ pPapFile** enthält einen Zeiger auf ein [**CPapFile-Objekt.**](cpapfile-class-and-methods.md) Es handelt sich um ein C++-Objekt, das Lade- und Speichervorgänge für eine strukturierte Speicherverbunddatei kapselt. **CPapFile arbeitet** mit dem zugrunde liegenden serverbasierten COPaper-Objekt zusammen, um die COPaper-Zeichnungsdaten zu laden und zu speichern.

 

 




