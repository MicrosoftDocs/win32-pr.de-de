---
description: 'Weitere Informationen: Verwenden von Hooks'
ms.assetid: f0ca9e41-a9f7-435f-a601-f0959adcb514
title: Verwenden von Hooks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d65d457b4549601aa89c3dae5b6e05c1fe0afed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867995"
---
# <a name="using-hooks"></a><span data-ttu-id="26161-103">Verwenden von Hooks</span><span class="sxs-lookup"><span data-stu-id="26161-103">Using Hooks</span></span>

<span data-ttu-id="26161-104">Die folgenden Codebeispiele veranschaulichen, wie die folgenden mit Hooks verknüpften Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="26161-104">The following code examples demonstrate how to perform the following tasks associated with hooks:</span></span>

-   [<span data-ttu-id="26161-105">Installieren und Freigeben von Hook-Verfahren</span><span class="sxs-lookup"><span data-stu-id="26161-105">Installing and Releasing Hook Procedures</span></span>](#installing-and-releasing-hook-procedures)
-   [<span data-ttu-id="26161-106">Überwachen von System Ereignissen</span><span class="sxs-lookup"><span data-stu-id="26161-106">Monitoring System Events</span></span>](#monitoring-system-events)

## <a name="installing-and-releasing-hook-procedures"></a><span data-ttu-id="26161-107">Installieren und Freigeben von Hook-Verfahren</span><span class="sxs-lookup"><span data-stu-id="26161-107">Installing and Releasing Hook Procedures</span></span>

<span data-ttu-id="26161-108">Sie können eine Hook-Prozedur installieren, indem Sie die Funktion [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) aufrufen und den Typ des Hooks angeben, der die Prozedur aufruft, ob die Prozedur allen Threads im gleichen Desktop wie der aufrufende Thread oder einem bestimmten Thread zugeordnet werden soll, und ein Zeiger auf den Einstiegspunkt der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="26161-108">You can install a hook procedure by calling the [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) function and specifying the type of hook calling the procedure, whether the procedure should be associated with all threads in the same desktop as the calling thread or with a particular thread, and a pointer to the procedure entry point.</span></span>

<span data-ttu-id="26161-109">Sie müssen eine globale Hook-Prozedur in einer DLL getrennt von der Anwendung platzieren, die die Hook-Prozedur installiert.</span><span class="sxs-lookup"><span data-stu-id="26161-109">You must place a global hook procedure in a DLL separate from the application installing the hook procedure.</span></span> <span data-ttu-id="26161-110">Die Installationsanwendung muss über das Handle für das dll-Modul verfügen, bevor die Hook-Prozedur installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="26161-110">The installing application must have the handle to the DLL module before it can install the hook procedure.</span></span> <span data-ttu-id="26161-111">Rufen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion mit dem Namen der dll auf, um ein Handle für das dll-Modul abzurufen.</span><span class="sxs-lookup"><span data-stu-id="26161-111">To retrieve a handle to the DLL module, call the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function with the name of the DLL.</span></span> <span data-ttu-id="26161-112">Nachdem Sie das Handle abgerufen haben, können Sie die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen, um einen Zeiger auf die Hook-Prozedur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="26161-112">After you have obtained the handle, you can call the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve a pointer to the hook procedure.</span></span> <span data-ttu-id="26161-113">Verwenden Sie abschließend [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) , um die Hook-Prozedur Adresse in der entsprechenden Hook-Kette zu installieren.</span><span class="sxs-lookup"><span data-stu-id="26161-113">Finally, use [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) to install the hook procedure address in the appropriate hook chain.</span></span> <span data-ttu-id="26161-114">**SetWindowsHookEx** übergibt das Modul handle, einen Zeiger auf den Einstiegspunkt für die Hook-Prozedur und 0 für den Thread Bezeichner, um anzugeben, dass die Hook-Prozedur allen Threads im gleichen Desktop wie der aufrufende Thread zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26161-114">**SetWindowsHookEx** passes the module handle, a pointer to the hook-procedure entry point, and 0 for the thread identifier, indicating that the hook procedure should be associated with all threads in the same desktop as the calling thread.</span></span> <span data-ttu-id="26161-115">Diese Sequenz wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="26161-115">This sequence is shown in the following example.</span></span>

``` syntax
HOOKPROC hkprcSysMsg;
static HINSTANCE hinstDLL; 
static HHOOK hhookSysMsg; 
 
hinstDLL = LoadLibrary(TEXT("c:\\myapp\\sysmsg.dll")); 
hkprcSysMsg = (HOOKPROC)GetProcAddress(hinstDLL, "SysMessageProc"); 

hhookSysMsg = SetWindowsHookEx( 
                    WH_SYSMSGFILTER,
                    hkprcSysMsg,
                    hinstDLL,
                    0); 
```

<span data-ttu-id="26161-116">Sie können eine Thread spezifische Hook-Prozedur freigeben (entfernen Sie die Adresse aus der Hookkette), indem Sie die [**unhookwindowshookex**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) -Funktion aufrufen und das Handle für die frei zugebende Hook-Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="26161-116">You can release a thread-specific hook procedure (remove its address from the hook chain) by calling the [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) function, specifying the handle to the hook procedure to release.</span></span> <span data-ttu-id="26161-117">Geben Sie eine Hook-Prozedur frei, sobald Sie von Ihrer Anwendung nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="26161-117">Release a hook procedure as soon as your application no longer needs it.</span></span>

<span data-ttu-id="26161-118">Sie können eine globale Hook-Prozedur mithilfe von [**unhookwindowshookex**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)freigeben, aber diese Funktion gibt die dll, die die Hook-Prozedur enthält, nicht frei.</span><span class="sxs-lookup"><span data-stu-id="26161-118">You can release a global hook procedure by using [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex), but this function does not free the DLL containing the hook procedure.</span></span> <span data-ttu-id="26161-119">Dies liegt daran, dass globale Hook-Prozeduren im Prozess Kontext jeder Anwendung auf dem Desktop aufgerufen werden. Dies führt zu einem impliziten Aufruf der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion für alle diese Prozesse.</span><span class="sxs-lookup"><span data-stu-id="26161-119">This is because global hook procedures are called in the process context of every application in the desktop, causing an implicit call to the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function for all of those processes.</span></span> <span data-ttu-id="26161-120">Da für einen anderen Prozess kein Aufrufe der [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion durchgeführt werden kann, gibt es keine Möglichkeit, die dll freizugeben.</span><span class="sxs-lookup"><span data-stu-id="26161-120">Because a call to the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function cannot be made for another process, there is then no way to free the DLL.</span></span> <span data-ttu-id="26161-121">Das System gibt die dll schließlich frei, nachdem alle Prozesse, die explizit mit der DLL verknüpft sind, entweder beendet oder als **FreeLibrary** bezeichnet wurden und alle Prozesse, die die Hook-Prozedur aufgerufen haben, die Verarbeitung außerhalb der dll fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="26161-121">The system eventually frees the DLL after all processes explicitly linked to the DLL have either terminated or called **FreeLibrary** and all processes that called the hook procedure have resumed processing outside the DLL.</span></span>

<span data-ttu-id="26161-122">Eine alternative Methode zum Installieren einer globalen Hook-Prozedur ist das Bereitstellen einer Installationsfunktion in der dll zusammen mit der Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="26161-122">An alternative method for installing a global hook procedure is to provide an installation function in the DLL, along with the hook procedure.</span></span> <span data-ttu-id="26161-123">Bei dieser Methode benötigt die installierte Anwendung das Handle für das dll-Modul nicht.</span><span class="sxs-lookup"><span data-stu-id="26161-123">With this method, the installing application does not need the handle to the DLL module.</span></span> <span data-ttu-id="26161-124">Durch die Verknüpfung mit der DLL erhält die Anwendung Zugriff auf die-Installationsfunktion.</span><span class="sxs-lookup"><span data-stu-id="26161-124">By linking with the DLL, the application gains access to the installation function.</span></span> <span data-ttu-id="26161-125">Die Installationsfunktion kann das dll-Modul Handle und andere Details im Aufrufen von [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="26161-125">The installation function can supply the DLL module handle and other details in the call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).</span></span> <span data-ttu-id="26161-126">Die dll kann auch eine Funktion enthalten, die die globale Hook-Prozedur freigibt. die Anwendung kann diese Funktion zur Hook-Freigabe beim Beenden von aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="26161-126">The DLL can also contain a function that releases the global hook procedure; the application can call this hook-releasing function when terminating.</span></span>

## <a name="monitoring-system-events"></a><span data-ttu-id="26161-127">Überwachen von System Ereignissen</span><span class="sxs-lookup"><span data-stu-id="26161-127">Monitoring System Events</span></span>

<span data-ttu-id="26161-128">Im folgenden Beispiel werden verschiedene Thread spezifische Hook-Prozeduren verwendet, um das System auf Ereignisse zu überwachen, die sich auf einen Thread auswirken.</span><span class="sxs-lookup"><span data-stu-id="26161-128">The following example uses a variety of thread-specific hook procedures to monitor the system for events affecting a thread.</span></span> <span data-ttu-id="26161-129">Es wird veranschaulicht, wie Ereignisse für die folgenden Arten von Hook-Prozeduren verarbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="26161-129">It demonstrates how to process events for the following types of hook procedures:</span></span>

-   <span data-ttu-id="26161-130">**WH \_ callwndproc**</span><span class="sxs-lookup"><span data-stu-id="26161-130">**WH\_CALLWNDPROC**</span></span>
-   <span data-ttu-id="26161-131">**WH \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="26161-131">**WH\_CBT**</span></span>
-   <span data-ttu-id="26161-132">**WH- \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="26161-132">**WH\_DEBUG**</span></span>
-   <span data-ttu-id="26161-133">**WH \_ GetMessage**</span><span class="sxs-lookup"><span data-stu-id="26161-133">**WH\_GETMESSAGE**</span></span>
-   <span data-ttu-id="26161-134">**WH- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="26161-134">**WH\_KEYBOARD**</span></span>
-   <span data-ttu-id="26161-135">**WH- \_ Maus**</span><span class="sxs-lookup"><span data-stu-id="26161-135">**WH\_MOUSE**</span></span>
-   <span data-ttu-id="26161-136">**WH \_ msgfilter**</span><span class="sxs-lookup"><span data-stu-id="26161-136">**WH\_MSGFILTER**</span></span>

<span data-ttu-id="26161-137">Der Benutzer kann eine Hook-Prozedur mithilfe des Menüs installieren und entfernen.</span><span class="sxs-lookup"><span data-stu-id="26161-137">The user can install and remove a hook procedure by using the menu.</span></span> <span data-ttu-id="26161-138">Wenn eine Hook-Prozedur installiert wird und ein Ereignis auftritt, das von der Prozedur überwacht wird, schreibt die Prozedur Informationen über das Ereignis in den Client Bereich des Hauptfensters der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="26161-138">When a hook procedure is installed and an event that is monitored by the procedure occurs, the procedure writes information about the event to the client area of the application's main window.</span></span>


```
#include <windows.h>
#include <strsafe.h>
#include "app.h"

#pragma comment( lib, "user32.lib") 
#pragma comment( lib, "gdi32.lib")

#define NUMHOOKS 7 
 
// Global variables 
 
typedef struct _MYHOOKDATA 
{ 
    int nType; 
    HOOKPROC hkprc; 
    HHOOK hhook; 
} MYHOOKDATA; 
 
MYHOOKDATA myhookdata[NUMHOOKS]; 

HWND gh_hwndMain;

// Hook procedures

LRESULT WINAPI CallWndProc(int, WPARAM, LPARAM);
LRESULT WINAPI CBTProc(int, WPARAM, LPARAM);
LRESULT WINAPI DebugProc(int, WPARAM, LPARAM);
LRESULT WINAPI GetMsgProc(int, WPARAM, LPARAM);
LRESULT WINAPI KeyboardProc(int, WPARAM, LPARAM);
LRESULT WINAPI MouseProc(int, WPARAM, LPARAM);
LRESULT WINAPI MessageProc(int, WPARAM, LPARAM);

void LookUpTheMessage(PMSG, LPTSTR);
 
LRESULT WINAPI MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    static BOOL afHooks[NUMHOOKS]; 
    int index; 
    static HMENU hmenu; 
 
    gh_hwndMain = hwndMain;
    
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Save the menu handle
 
            hmenu = GetMenu(hwndMain); 
 
            // Initialize structures with hook data. The menu-item identifiers are 
            // defined as 0 through 6 in the header file app.h. They can be used to 
            // identify array elements both here and during the WM_COMMAND message. 
 
            myhookdata[IDM_CALLWNDPROC].nType = WH_CALLWNDPROC; 
            myhookdata[IDM_CALLWNDPROC].hkprc = CallWndProc; 
            myhookdata[IDM_CBT].nType = WH_CBT; 
            myhookdata[IDM_CBT].hkprc = CBTProc; 
            myhookdata[IDM_DEBUG].nType = WH_DEBUG; 
            myhookdata[IDM_DEBUG].hkprc = DebugProc; 
            myhookdata[IDM_GETMESSAGE].nType = WH_GETMESSAGE; 
            myhookdata[IDM_GETMESSAGE].hkprc = GetMsgProc; 
            myhookdata[IDM_KEYBOARD].nType = WH_KEYBOARD; 
            myhookdata[IDM_KEYBOARD].hkprc = KeyboardProc; 
            myhookdata[IDM_MOUSE].nType = WH_MOUSE; 
            myhookdata[IDM_MOUSE].hkprc = MouseProc; 
            myhookdata[IDM_MSGFILTER].nType = WH_MSGFILTER; 
            myhookdata[IDM_MSGFILTER].hkprc = MessageProc; 
 
            // Initialize all flags in the array to FALSE. 
 
            memset(afHooks, FALSE, sizeof(afHooks)); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                 // The user selected a hook command from the menu. 
 
                case IDM_CALLWNDPROC: 
                case IDM_CBT: 
                case IDM_DEBUG: 
                case IDM_GETMESSAGE: 
                case IDM_KEYBOARD: 
                case IDM_MOUSE: 
                case IDM_MSGFILTER: 
 
                    // Use the menu-item identifier as an index 
                    // into the array of structures with hook data. 
 
                    index = LOWORD(wParam); 
 
                    // If the selected type of hook procedure isn't 
                    // installed yet, install it and check the 
                    // associated menu item. 
 
                    if (!afHooks[index]) 
                    { 
                        myhookdata[index].hhook = SetWindowsHookEx( 
                            myhookdata[index].nType, 
                            myhookdata[index].hkprc, 
                            (HINSTANCE) NULL, GetCurrentThreadId()); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_CHECKED); 
                        afHooks[index] = TRUE; 
                    } 
 
                    // If the selected type of hook procedure is 
                    // already installed, remove it and remove the 
                    // check mark from the associated menu item. 
 
                    else 
                    { 
                        UnhookWindowsHookEx(myhookdata[index].hhook); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_UNCHECKED); 
                        afHooks[index] = FALSE; 
                    } 
 
                default: 
                    return (DefWindowProc(hwndMain, uMsg, wParam, 
                        lParam)); 
            } 
            break; 
 
            //
            // Process other messages. 
            //
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
/**************************************************************** 
  WH_CALLWNDPROC hook procedure 
 ****************************************************************/ 
 
LRESULT WINAPI CallWndProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szCWPBuf[256]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch;
    HRESULT hResult; 
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szCWPBuf, 256/sizeof(TCHAR),  
               "CALLWNDPROC - tsk: %ld, msg: %s, %d times   ", 
                wParam, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: writer error handler
            }
            hResult = StringCchLength(szCWPBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 15, szCWPBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_GETMESSAGE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK GetMsgProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szMSGBuf[256]; 
    CHAR szRem[16]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0) // do not process message 
        return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case HC_ACTION: 
            switch (wParam) 
            { 
                case PM_REMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_REMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                case PM_NOREMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_NOREMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                default:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
            } 
 
            // Call an application-defined function that converts a 
            // message constant to a string and copies it to a 
            // buffer. 
 
            LookUpTheMessage((PMSG) lParam, szMsg); 
 
            hdc = GetDC(gh_hwndMain);
            hResult = StringCchPrintf(szMSGBuf, 256/sizeof(TCHAR), 
                "GETMESSAGE - wParam: %s, msg: %s, %d times   ", 
                szRem, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szMSGBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 35, szMSGBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_DEBUG hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK DebugProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),   
                "DEBUG - nCode: %d, tsk: %ld, %d times   ", 
                nCode,wParam, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 55, szBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_CBT hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK CBTProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szCode[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, 
            lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HCBT_ACTIVATE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_ACTIVATE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CLICKSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CLICKSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CREATEWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CREATEWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_DESTROYWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_DESTROYWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_KEYSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_KEYSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MINMAX:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MINMAX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MOVESIZE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MOVESIZE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_QS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_QS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SETFOCUS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SETFOCUS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SYSCOMMAND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SYSCOMMAND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
    } 
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "CBT -  nCode: %s, tsk: %ld, %d times   ",
        szCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 75, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MOUSE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MouseProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process the message 
        return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, 
            wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), 
        "MOUSE - nCode: %d, msg: %s, x: %d, y: %d, %d times   ", 
        nCode, szMsg, LOWORD(lParam), HIWORD(lParam), c++); 
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    TextOut(hdc, 2, 95, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_KEYBOARD hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK KeyboardProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "KEYBOARD - nCode: %d, vk: %d, %d times ", nCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 115, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MSGFILTER hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MessageProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    CHAR szCode[32]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case MSGF_DIALOGBOX:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_DIALOGBOX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_MENU:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_MENU");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_SCROLLBAR:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_SCROLLBAR");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchPrintf(szCode, 128/sizeof(TCHAR), "Unknown: %d", nCode);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
            break; 
    } 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),  
        "MSGFILTER  nCode: %s, msg: %s, %d times    ", 
        szCode, szMsg, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 135, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, wParam, lParam); 
}
```



 

 
