---
title: Cguipaper-Klassen Deklaration
description: Cguipaper-Klassen Deklaration
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036493"
---
# <a name="cguipaper-class-declaration"></a>Cguipaper-Klassen Deklaration

Im folgenden finden Sie die **cguipaper** -Klassen Deklaration aus "guipaper. H".


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



**Cguipaper** behält die aktuellen GUI-Eigenschaften für das Zeichnungs Papier bei. Member **m \_ crinkcolor**, **m \_ crinkwidth** und **m \_ winrect** enthalten Werte für die aktuelle frei Hand Farbe, die frei Handbreite und das Zeichnungs Rechteck. Das **m- \_ HWND** -Element speichert das Handle für das Fenster, in dem das Zeichnen erfolgt.

Das eigentliche Zeichnen von Bildern erfolgt mithilfe eines Handles für einen Gerätekontext, der in Mitglied **m \_ hdc** gespeichert ist. Ein Handle für den aktuellen Zeichnungs Stift wird im Member **m \_ HPEN** beibehalten. Der Stift wird zerstört und neu erstellt, wenn seine Farbe oder Breite vom Benutzer geändert wird.

Die Member **m \_ pcopapersink** und **m \_ dwtaschen Sink** halten Werte, die für die Verbindung mit copaper erforderlich sind, um eingehende Benachrichtigungen über die [**ipapersink**](ipapersink-methods.md) -Schnittstelle zu empfangen. Der Member **m \_ bdirty** enthält ein Flag, das angibt, dass der Benutzer die Zeichnung geändert hat und dass die in der Datei gespeicherten Daten nicht mehr wiedergegeben werden.

Mitglied **m \_ pipaper** enthält den Haupt Schnittstellen Zeiger auf das copaper-Objekt. Der Zugriff auf alle copaper-Funktionen erfolgt über diesen Zeiger.

Der **m \_ nlockkey** -Member wird verwendet, um ein Client Sperr Schema zu unterstützen, das für mehrere Clients verwendet wird, um einem exklusiven Client Zugriff auf ein frei gegebenes copaper-Objekt zu ermöglichen. Copaper weist während eines [**iPaper**](ipaper-methods.md)::**Lock** -Aufrufs **m \_ nlockkey** zu und wird vom Client in nachfolgenden Aufrufen an copaper als Parameter übergeben. Copaper führt die Arbeit in diesen Aufrufen nur dann durch, wenn der übergebene Sperr Schlüssel mit dem Schlüssel übereinstimmt, der zuletzt von copaper an einen Client ausgegeben wurde.

Mitglied **m \_ ppapfile** enthält einen Zeiger auf ein [**cpapfile**](cpapfile-class-and-methods.md) -Objekt. Dabei handelt es sich um ein C++-Objekt, das Lade-und Speichervorgänge in einer strukturierten Speicher Verbund Datei kapselt. **Cpapfile** kann mit dem zugrunde liegenden serverbasierten copaper-Objekt verwendet werden, um die copaper-Zeichnungsdaten zu laden und zu speichern.

 

 




