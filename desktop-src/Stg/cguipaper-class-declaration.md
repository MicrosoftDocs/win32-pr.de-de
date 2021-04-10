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
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="7b94d-103">Cguipaper-Klassen Deklaration</span><span class="sxs-lookup"><span data-stu-id="7b94d-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="7b94d-104">Im folgenden finden Sie die **cguipaper** -Klassen Deklaration aus "guipaper. H".</span><span class="sxs-lookup"><span data-stu-id="7b94d-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="7b94d-105">**Cguipaper** behält die aktuellen GUI-Eigenschaften für das Zeichnungs Papier bei.</span><span class="sxs-lookup"><span data-stu-id="7b94d-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="7b94d-106">Member **m \_ crinkcolor**, **m \_ crinkwidth** und **m \_ winrect** enthalten Werte für die aktuelle frei Hand Farbe, die frei Handbreite und das Zeichnungs Rechteck.</span><span class="sxs-lookup"><span data-stu-id="7b94d-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="7b94d-107">Das **m- \_ HWND** -Element speichert das Handle für das Fenster, in dem das Zeichnen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7b94d-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="7b94d-108">Das eigentliche Zeichnen von Bildern erfolgt mithilfe eines Handles für einen Gerätekontext, der in Mitglied **m \_ hdc** gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7b94d-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="7b94d-109">Ein Handle für den aktuellen Zeichnungs Stift wird im Member **m \_ HPEN** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7b94d-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="7b94d-110">Der Stift wird zerstört und neu erstellt, wenn seine Farbe oder Breite vom Benutzer geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7b94d-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="7b94d-111">Die Member **m \_ pcopapersink** und **m \_ dwtaschen Sink** halten Werte, die für die Verbindung mit copaper erforderlich sind, um eingehende Benachrichtigungen über die [**ipapersink**](ipapersink-methods.md) -Schnittstelle zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="7b94d-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="7b94d-112">Der Member **m \_ bdirty** enthält ein Flag, das angibt, dass der Benutzer die Zeichnung geändert hat und dass die in der Datei gespeicherten Daten nicht mehr wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b94d-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="7b94d-113">Mitglied **m \_ pipaper** enthält den Haupt Schnittstellen Zeiger auf das copaper-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b94d-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="7b94d-114">Der Zugriff auf alle copaper-Funktionen erfolgt über diesen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="7b94d-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="7b94d-115">Der **m \_ nlockkey** -Member wird verwendet, um ein Client Sperr Schema zu unterstützen, das für mehrere Clients verwendet wird, um einem exklusiven Client Zugriff auf ein frei gegebenes copaper-Objekt zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7b94d-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="7b94d-116">Copaper weist während eines [**iPaper**](ipaper-methods.md)::**Lock** -Aufrufs **m \_ nlockkey** zu und wird vom Client in nachfolgenden Aufrufen an copaper als Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7b94d-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="7b94d-117">Copaper führt die Arbeit in diesen Aufrufen nur dann durch, wenn der übergebene Sperr Schlüssel mit dem Schlüssel übereinstimmt, der zuletzt von copaper an einen Client ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7b94d-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="7b94d-118">Mitglied **m \_ ppapfile** enthält einen Zeiger auf ein [**cpapfile**](cpapfile-class-and-methods.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b94d-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="7b94d-119">Dabei handelt es sich um ein C++-Objekt, das Lade-und Speichervorgänge in einer strukturierten Speicher Verbund Datei kapselt.</span><span class="sxs-lookup"><span data-stu-id="7b94d-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="7b94d-120">**Cpapfile** kann mit dem zugrunde liegenden serverbasierten copaper-Objekt verwendet werden, um die copaper-Zeichnungsdaten zu laden und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7b94d-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




