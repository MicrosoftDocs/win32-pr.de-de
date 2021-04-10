---
title: Verwenden von Streams
description: Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Ein Stream wird durch eine editstream-Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt.
ms.assetid: A7ED47F1-968C-4E41-B1E2-4449072D2FC4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89a9cc2a8caa157f9c65220fc5cead7564bc555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104101383"
---
# <a name="how-to-use-streams"></a><span data-ttu-id="a538b-104">Verwenden von Streams</span><span class="sxs-lookup"><span data-stu-id="a538b-104">How to Use Streams</span></span>

<span data-ttu-id="a538b-105">Sie können Datenströme verwenden, um Daten in ein oder aus einem Rich-Edit-Steuerelement zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="a538b-105">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="a538b-106">Ein Stream wird durch eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur definiert, die einen Puffer und eine Anwendungs definierte Rückruffunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="a538b-106">A stream is defined by an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure, which specifies a buffer and an application-defined callback function.</span></span>

<span data-ttu-id="a538b-107">Verwenden Sie zum Lesen von Daten in ein Rich-Edit-Steuerelement (d. h. Stream in den Daten) die [**EM- \_ StreamIn**](em-streamin.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a538b-107">To read data into a rich edit control (that is, stream in the data), use the [**EM\_STREAMIN**](em-streamin.md) message.</span></span> <span data-ttu-id="a538b-108">Das-Steuerelement ruft die Rückruffunktion der Anwendung wiederholt auf, die jedes Mal einen Teil der Daten in den Puffer überträgt.</span><span class="sxs-lookup"><span data-stu-id="a538b-108">The control repeatedly calls the application's callback function, which transfers a portion of the data into the buffer each time.</span></span>

<span data-ttu-id="a538b-109">Um den Inhalt eines Rich-Edit-Steuer Elements (d. h. das Streamen der Daten) zu speichern, können Sie die [**EM- \_ StreamOut**](em-streamout.md) -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a538b-109">To save the contents of a rich edit control (that is, stream out the data), you can use the [**EM\_STREAMOUT**](em-streamout.md) message.</span></span> <span data-ttu-id="a538b-110">Das-Steuerelement schreibt wiederholt in den Puffer und ruft dann die Rückruffunktion der Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="a538b-110">The control repeatedly writes to the buffer and then calls the application's callback function.</span></span> <span data-ttu-id="a538b-111">Für jeden-Befehl speichert die Rückruffunktion den Inhalt des Puffers.</span><span class="sxs-lookup"><span data-stu-id="a538b-111">For each call, the callback function saves the contents of the buffer.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a538b-112">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a538b-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a538b-113">Technologien</span><span class="sxs-lookup"><span data-stu-id="a538b-113">Technologies</span></span>

-   [<span data-ttu-id="a538b-114">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a538b-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a538b-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a538b-115">Prerequisites</span></span>

-   <span data-ttu-id="a538b-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="a538b-116">C/C++</span></span>
-   <span data-ttu-id="a538b-117">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="a538b-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a538b-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a538b-118">Instructions</span></span>

### <a name="use-a-stream"></a><span data-ttu-id="a538b-119">Verwenden eines Streams</span><span class="sxs-lookup"><span data-stu-id="a538b-119">Use a Stream</span></span>

<span data-ttu-id="a538b-120">Im folgenden Codebeispiel wird gezeigt, wie eine RTF-Datei in ein Rich-Edit-Steuerelement gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="a538b-120">The following code example shows how to read an .rtf file into a rich edit control.</span></span> <span data-ttu-id="a538b-121">Das Datei Handle wird über den **dwCookie** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur an die Rückruffunktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a538b-121">The file handle is passed to the callback function through the **dwCookie** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span>


```C++
DWORD CALLBACK EditStreamCallback(DWORD_PTR dwCookie, 
                                  LPBYTE lpBuff,
                                  LONG cb, 
                                  PLONG pcb)
{
    HANDLE hFile = (HANDLE)dwCookie;
    
    if (ReadFile(hFile, lpBuff, cb, (DWORD *)pcb, NULL)) 
    {
        return 0;
    }
    
    return -1;
}

BOOL FillRichEditFromFile(HWND hwnd, LPCTSTR pszFile)
{
    BOOL fSuccess = FALSE;
    
    HANDLE hFile = CreateFile(pszFile, GENERIC_READ, 
                              FILE_SHARE_READ, 0, OPEN_EXISTING,
                              FILE_FLAG_SEQUENTIAL_SCAN, NULL);
        
    if (hFile != INVALID_HANDLE_VALUE) 
    {
        EDITSTREAM es = { 0 };
        
        es.pfnCallback = EditStreamCallback;
        es.dwCookie    = (DWORD_PTR)hFile;
        
        if (SendMessage(hwnd, EM_STREAMIN, SF_RTF, (LPARAM)&es) && es.dwError == 0) 
        {
                fSuccess = TRUE;
        }
        
        CloseHandle(hFile);
    }
    
    return fSuccess;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="a538b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a538b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a538b-123">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="a538b-123">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="a538b-124">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="a538b-124">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




