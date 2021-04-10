---
title: So erstellen Sie ein Multiple-Selection Listenfeld
description: In diesem Thema wird veranschaulicht, wie Sie den Inhalt eines Verzeichnisses in einem Listenfeld Mehrfachauswahl anzeigen und darauf zugreifen können.
ms.assetid: 5192E171-8CEF-4921-9378-A7C3A52A9024
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd47b1d582d53a66bc77284927aef4230043e92
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039857"
---
# <a name="how-to-create-a-multiple-selection-list-box"></a><span data-ttu-id="a5b80-103">So erstellen Sie ein Multiple-Selection Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a5b80-103">How to Create a Multiple-Selection List Box</span></span>

<span data-ttu-id="a5b80-104">In diesem Thema wird veranschaulicht, wie Sie den Inhalt eines Verzeichnisses in einem Listenfeld Mehrfachauswahl anzeigen und darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a5b80-104">This topic demonstrates how to display and access the contents of a directory in a multiple-selection list box.</span></span> <span data-ttu-id="a5b80-105">Im Listenfeld Mehrfachauswahl kann der Benutzer mehrere Elemente gleichzeitig auswählen.</span><span class="sxs-lookup"><span data-stu-id="a5b80-105">In a multiple-selection list box, the user can select more than one item at a time.</span></span>

<span data-ttu-id="a5b80-106">Mit dem C++-Codebeispiel in diesem Thema kann ein Benutzer eine Liste der Dateien im aktuellen Verzeichnis anzeigen, eine Gruppe von Dateien aus der Liste auswählen und diese löschen.</span><span class="sxs-lookup"><span data-stu-id="a5b80-106">The C++ code example in this topic enables a user to view a list of files in the current directory, select a group of files from the list, and delete them.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a5b80-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a5b80-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a5b80-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="a5b80-108">Technologies</span></span>

-   [<span data-ttu-id="a5b80-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a5b80-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a5b80-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a5b80-110">Prerequisites</span></span>

-   <span data-ttu-id="a5b80-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a5b80-111">C/C++</span></span>
-   <span data-ttu-id="a5b80-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="a5b80-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a5b80-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a5b80-113">Instructions</span></span>


<span data-ttu-id="a5b80-114">Die Verzeichnis Auflistungs Anwendung muss die folgenden Aufgaben im Listenfeld – Verwandte Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="a5b80-114">The directory listing application must perform the following list box–related tasks:</span></span>

-   <span data-ttu-id="a5b80-115">Initialisieren Sie das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="a5b80-115">Initialize the list box.</span></span>
-   <span data-ttu-id="a5b80-116">Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="a5b80-116">Retrieve the user's selections from the list box.</span></span>
-   <span data-ttu-id="a5b80-117">Entfernen Sie die Dateinamen aus dem Listenfeld, nachdem die ausgewählten Dateien gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="a5b80-117">Remove the file names from the list box after the selected files have been deleted.</span></span>

<span data-ttu-id="a5b80-118">Im folgenden C++-Codebeispiel initialisiert die Dialogfeld Prozedur das Listenfeld Mehrfachauswahl (IDC \_ FileList) mithilfe der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion, um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="a5b80-118">In the following C++ code example, the dialog box procedure initializes the multiple-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span>

<span data-ttu-id="a5b80-119">Wenn der Benutzer eine Gruppe von Dateien auswählt und auf die Schaltfläche **Löschen** klickt, sendet die Dialogfeld Prozedur die [**lb- \_ getselcount**](lb-getselcount.md) -Nachricht, um die Anzahl ausgewählter Dateien abzurufen, und die [**lb \_ getselitems**](lb-getselitems.md) -Nachricht, um ein Array ausgewählter Listenfeld Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5b80-119">When the user selects a group of files and chooses the **Delete** button, the dialog box procedure sends the [**LB\_GETSELCOUNT**](lb-getselcount.md) message, to retrieve the number of files selected, and the [**LB\_GETSELITEMS**](lb-getselitems.md) message, to retrieve an array of selected list box items.</span></span> <span data-ttu-id="a5b80-120">Nach dem Löschen einer Datei entfernt die Dialogfeld Prozedur das entsprechende Element aus dem Listenfeld, indem die [**lb- \_ deletestring**](lb-deletestring.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5b80-120">After deleting a file, the dialog procedure removes the corresponding item from the list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



```C++
#define BIGBUFF 8192 
 
INT_PTR CALLBACK DlgDelFilesProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int cSelItems; 
    int cSelItemsInBuffer; 
    TCHAR achBuffer[MAX_PATH]; 
    int aSelItems[BIGBUFF]; 
    int i; 
    BOOL fResult; 
    HWND hListBox;
    int iRet;
 
    switch (message) { 
 
        case WM_INITDIALOG: 
 
            // Initialize the list box by filling it with files from 
            // the current directory. 
            pszCurDir = achBuffer; 
            GetCurrentDirectory(MAX_PATH, pszCurDir);
            DlgDirList(hDlg, pszCurDir, IDC_FILELIST, IDS_PATHTOFILL, 0); 
            SetFocus(GetDlgItem(hDlg, IDC_FILELIST)); 
 
            return FALSE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
 
                    // When the user presses the DEL (IDOK) button, 
                    // first retrieve the list of selected files. 
                    pszFileToDelete = achBuffer; 
                    hListBox = GetDlgItem(hDlg, IDC_FILELIST); 
                    cSelItems = SendMessage(hListBox, 
                            LB_GETSELCOUNT, 0, 0); 
 
                    cSelItemsInBuffer = SendMessage(hListBox, 
                            LB_GETSELITEMS, 512, (LPARAM) aSelItems); 
 
                    if (cSelItems > cSelItemsInBuffer) 
                    { 
                        MessageBox(hDlg, L"Too many items selected.", 
                                NULL, MB_OK); 
                    } 
                    else 
                    { 

                        // Make sure the user really wants to delete the files.
                        iRet = MessageBox(hDlg, 
                            L"Are you sure you want to delete these files?", 
                            L"Deleting Files", MB_YESNO | MB_ICONEXCLAMATION);
                        if (iRet == IDNO)
                            return TRUE;

                        // Go through the list backward because after deleting
                        // an item the indices change for every subsequent 
                        // item. By going backward, the indices are never 
                        // invalidated. 
                        for (i = cSelItemsInBuffer - 1; i >= 0; i--) 
                        { 
                            SendMessage(hListBox, LB_GETTEXT, 
                                        aSelItems[i], 
                                        (LPARAM) pszFileToDelete); 
 
                            fResult = DeleteFile(pszFileToDelete); 
                            if (!fResult) 
                            {                     
                                MessageBox(hDlg, L"Could not delete file.", 
                                    NULL, MB_OK);     
                            } 
                            else 
                            { 
                                SendMessage(hListBox, LB_DELETESTRING, 
                                        aSelItems[i], 0); 
                            } 
                        } 
                        SendMessage(hListBox, LB_SETCARETINDEX, 0, 0); 
                    } 
                    return TRUE; 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    return FALSE; 
            } 
 
        default: 
                return FALSE; 
    } 
} 
```



## <a name="related-topics"></a><span data-ttu-id="a5b80-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5b80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b80-122">Listenfeld-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="a5b80-122">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a5b80-123">Informationen zu Listenfeldern</span><span class="sxs-lookup"><span data-stu-id="a5b80-123">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="a5b80-124">Verwenden von Listenfeldern</span><span class="sxs-lookup"><span data-stu-id="a5b80-124">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




