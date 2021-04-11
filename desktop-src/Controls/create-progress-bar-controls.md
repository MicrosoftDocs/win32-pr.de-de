---
title: Vorgehensweise beim Verwenden von Statusanzeige-Steuerelementen
description: In diesem Thema wird erläutert, wie Sie eine Statusanzeige verwenden, um den Fortschritt eines langen Datei Verarbeitungsvorgangs anzuzeigen.
ms.assetid: 4CC25F3A-9CAF-4ADC-B29C-3FACDD73D5A0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c71ff33a14f2d2af5fa8735c5197c50acaa948b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949167"
---
# <a name="how-to-use-progress-bar-controls"></a><span data-ttu-id="21a64-103">Vorgehensweise beim Verwenden von Statusanzeige-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="21a64-103">How to Use Progress Bar Controls</span></span>

<span data-ttu-id="21a64-104">In diesem Thema wird erläutert, wie Sie eine Statusanzeige verwenden, um den Fortschritt eines langen Datei Verarbeitungsvorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="21a64-104">This topic explains how to use a progress bar to indicate the progress of a lengthy file-parsing operation.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="21a64-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="21a64-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="21a64-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="21a64-106">Technologies</span></span>

-   [<span data-ttu-id="21a64-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="21a64-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="21a64-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="21a64-108">Prerequisites</span></span>

-   <span data-ttu-id="21a64-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="21a64-109">C/C++</span></span>
-   <span data-ttu-id="21a64-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="21a64-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="21a64-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="21a64-111">Instructions</span></span>

### <a name="create-a-progress-bar-control"></a><span data-ttu-id="21a64-112">Erstellen eines Statusanzeige-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="21a64-112">Create a Progress Bar Control</span></span>

<span data-ttu-id="21a64-113">Der folgende Beispielcode erstellt eine Statusanzeige und positioniert Sie am unteren Rand des Client Bereichs des übergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="21a64-113">The following example code creates a progress bar and positions it along the bottom of the parent window's client area.</span></span> <span data-ttu-id="21a64-114">Die Höhe der Statusanzeige basiert auf der Höhe der in einer Schiebe Leiste verwendeten Pfeil Bitmap.</span><span class="sxs-lookup"><span data-stu-id="21a64-114">The height of the progress bar is based on the height of the arrow bitmap used in a scroll bar.</span></span> <span data-ttu-id="21a64-115">Der Bereich basiert auf der Größe der Datei dividiert durch 2.048, d. h. der Größe jedes "Blocks" der aus der Datei gelesenen Daten.</span><span class="sxs-lookup"><span data-stu-id="21a64-115">The range is based on the size of the file divided by 2,048, which is the size of each "chunk" of data that is read from the file.</span></span> <span data-ttu-id="21a64-116">Im Beispiel wird außerdem ein Inkrement festgelegt, und die aktuelle Position der Statusanzeige wird um das Inkrement erhöht, nachdem die einzelnen Blöcke verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="21a64-116">The example also sets an increment and advances the current position of the progress bar by the increment after parsing each chunk.</span></span>


```C++
// ParseALargeFile - uses a progress bar to indicate the progress of a parsing operation.
//
// Returns TRUE if successful, or FALSE otherwise.
//
// hwndParent - parent window of the progress bar.
//
// lpszFileName - name of the file to parse. 
// 
// Global variable 
//     g_hinst - instance handle.
//

extern HINSTANCE g_hinst; 

BOOL ParseALargeFile(HWND hwndParent, LPTSTR lpszFileName) 
{ 
    RECT rcClient;  // Client area of parent window.
    int cyVScroll;  // Height of scroll bar arrow.
    HWND hwndPB;    // Handle of progress bar.
    HANDLE hFile;   // Handle of file.
    DWORD cb;       // Size of file and count of bytes read.
    LPCH pch;       // Address of data read from file.
    LPCH pchTmp;    // Temporary pointer.

    // Ensure that the common control DLL is loaded, and create a progress bar 
    // along the bottom of the client area of the parent window. 
    //
    // Base the height of the progress bar on the height of a scroll bar arrow.
    
    InitCommonControls(); 
    
    GetClientRect(hwndParent, &rcClient); 
    
    cyVScroll = GetSystemMetrics(SM_CYVSCROLL); 

    hwndPB = CreateWindowEx(0, PROGRESS_CLASS, (LPTSTR) NULL, 
                            WS_CHILD | WS_VISIBLE, rcClient.left, 
                            rcClient.bottom - cyVScroll, 
                            rcClient.right, cyVScroll, 
                            hwndParent, (HMENU) 0, g_hinst, NULL);

    // Open the file for reading, and retrieve the size of the file. 

    hFile = CreateFile(lpszFileName, GENERIC_READ, FILE_SHARE_READ, 
                       (LPSECURITY_ATTRIBUTES) NULL, OPEN_EXISTING, 
                       FILE_ATTRIBUTE_NORMAL, (HANDLE) NULL); 

    if (hFile == (HANDLE) INVALID_HANDLE_VALUE)
        return FALSE; 

    cb = GetFileSize(hFile, (LPDWORD) NULL); 

    // Set the range and increment of the progress bar. 

    SendMessage(hwndPB, PBM_SETRANGE, 0, MAKELPARAM(0, cb / 2048));
    
    SendMessage(hwndPB, PBM_SETSTEP, (WPARAM) 1, 0); 

    // Parse the file. 
    pch = (LPCH) LocalAlloc(LPTR, sizeof(char) * 2048); 
    
    pchTmp = pch; 
    
    do { 
        ReadFile(hFile, pchTmp, sizeof(char) * 2048, &cb, (LPOVERLAPPED) NULL);
        
        // TODO: Write an error handler to check that all the
        // requested data was read.
        //
        // Include here any code that parses the
        // file. 
        //  
        //  
        //  
        // Advance the current position of the progress bar by the increment.
        
        SendMessage(hwndPB, PBM_STEPIT, 0, 0); 
        
    } while (cb); 

    CloseHandle((HANDLE) hFile);
    
    DestroyWindow(hwndPB);

    return TRUE; 
}
```



## <a name="remarks"></a><span data-ttu-id="21a64-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21a64-117">Remarks</span></span>

<span data-ttu-id="21a64-118">Sie müssen sicherstellen, dass die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " ordnungsgemäß verwendet wird, um die Sicherheit Ihrer Anwendung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="21a64-118">You must make sure to use the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function correctly, to ensure the security of your application.</span></span> <span data-ttu-id="21a64-119">Im Beispielcode sollten Sie z. b. überprüfen, ob `ReadFile` alle angeforderten Daten tatsächlich von gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="21a64-119">For instance, in the example code, you should check to make sure that `ReadFile` actually reads all of the requested data.</span></span>

<span data-ttu-id="21a64-120">Beachten Sie auch, [**dass der vierte Parameter von "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)–" (lpsecurity- \_ Attribute)**null**– Standard Sicherheitswerte festlegt.</span><span class="sxs-lookup"><span data-stu-id="21a64-120">Also notice that the fourth parameter of [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)—(LPSECURITY\_ATTRIBUTES)**NULL**—sets default security values.</span></span> <span data-ttu-id="21a64-121">Wenn Sie bestimmte Sicherheitseinstellungen benötigen, müssen Sie die entsprechenden Werte in den Elementen der-Struktur festlegen.</span><span class="sxs-lookup"><span data-stu-id="21a64-121">If you need specific security settings, you must set the appropriate values in the structure's members.</span></span> <span data-ttu-id="21a64-122">Ruft **sizeof** auf, um die korrekte Größe der **lpsecurity- \_ Attribut** Struktur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="21a64-122">Call **sizeof** to set the correct size of the **LPSECURITY\_ATTRIBUTES** structure.</span></span>

<span data-ttu-id="21a64-123">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Microsoft Windows](sec-comctls.md)-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="21a64-123">For more information, see [Security Considerations: Microsoft Windows Controls](sec-comctls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21a64-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21a64-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a64-125">Verwenden von Statusanzeige-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="21a64-125">Using Progress Bar Controls</span></span>](using-progress-bar-controls.md)
</dt> <dt>

[<span data-ttu-id="21a64-126">Überlegungen zur Sicherheit: Microsoft Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="21a64-126">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)
</dt> </dl>

 

 