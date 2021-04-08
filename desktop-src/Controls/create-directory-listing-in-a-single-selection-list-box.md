---
title: Erstellen einer Verzeichnisliste in einem Listenfeld
description: In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einfacher Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zuzugreifen.
ms.assetid: 11C0DB10-59BA-47C4-8687-101A2A85D660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03829990605271574a2030486ac5aba428867ec3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949224"
---
# <a name="how-to-create-a-directory-listing-in-a-single-selection-listbox"></a><span data-ttu-id="54a94-103">Erstellen einer Verzeichnisliste in einem Listenfeld mit einfacher Auswahl</span><span class="sxs-lookup"><span data-stu-id="54a94-103">How to create a directory listing in a single-selection ListBox</span></span>

<span data-ttu-id="54a94-104">In diesem Thema wird veranschaulicht, wie Sie ein Listenfeld mit einfacher Auswahl verwenden, um den Inhalt eines Verzeichnisses anzuzeigen und darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="54a94-104">This topic demonstrates how to use a single-selection list box to display and access the contents of a directory.</span></span> <span data-ttu-id="54a94-105">Das Listenfeld für die einfache Auswahl ist der Standard Listen Feldtyp.</span><span class="sxs-lookup"><span data-stu-id="54a94-105">The single-selection list box is the default list box type.</span></span> <span data-ttu-id="54a94-106">Ein Benutzer kann jeweils nur ein Element in einem Listenfeld mit einer einzelnen Auswahl auswählen.</span><span class="sxs-lookup"><span data-stu-id="54a94-106">A user can only select one item at a time from a single-selection list box.</span></span>

<span data-ttu-id="54a94-107">Mit dem C++-Codebeispiel in diesem Thema kann ein Benutzer eine Liste der Dateien im aktuellen Verzeichnis anzeigen, eine Datei aus der Liste auswählen und diese löschen.</span><span class="sxs-lookup"><span data-stu-id="54a94-107">The C++ code example in this topic enables a user to view a list of files in the current directory, select a file from the list, and delete it.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="54a94-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="54a94-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="54a94-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="54a94-109">Technologies</span></span>

-   [<span data-ttu-id="54a94-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="54a94-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="54a94-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="54a94-111">Prerequisites</span></span>

-   <span data-ttu-id="54a94-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="54a94-112">C/C++</span></span>
-   <span data-ttu-id="54a94-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="54a94-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="54a94-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="54a94-114">Instructions</span></span>


<span data-ttu-id="54a94-115">Die Verzeichnis Auflistungs Anwendung muss die folgenden Aufgaben im Zusammenhang mit dem Listenfeld ausführen:</span><span class="sxs-lookup"><span data-stu-id="54a94-115">The directory listing application must perform the following list box related tasks:</span></span>

-   <span data-ttu-id="54a94-116">Initialisieren Sie das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="54a94-116">Initialize the list box.</span></span>
-   <span data-ttu-id="54a94-117">Rufen Sie die Auswahl des Benutzers aus dem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="54a94-117">Retrieve the user's selection from the list box.</span></span>
-   <span data-ttu-id="54a94-118">Entfernen Sie den Dateinamen aus dem Listenfeld, nachdem die ausgewählte Datei gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="54a94-118">Remove the file name from the list box after the selected file has been deleted.</span></span>

<span data-ttu-id="54a94-119">Im folgenden C++-Codebeispiel initialisiert die Dialogfeld Prozedur das Listenfeld für die einfache Auswahl (IDC \_ FileList) mithilfe der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion, um das Listenfeld mit den Namen aller Dateien im aktuellen Verzeichnis auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="54a94-119">In the following C++ code example, the dialog box procedure initializes the single-selection list box (IDC\_FILELIST) by using the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function to fill the list box with the names of all the files in the current directory.</span></span> <span data-ttu-id="54a94-120">Wenn der Benutzer eine Datei auswählt und auf die Schaltfläche **Löschen** klickt, ruft die [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) -Funktion den Namen der ausgewählten Datei ab.</span><span class="sxs-lookup"><span data-stu-id="54a94-120">When the user selects a file and chooses the **Delete** button, the [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) function retrieves the name of the selected file.</span></span> <span data-ttu-id="54a94-121">Der Code löscht die Datei mit der [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) -Funktion und aktualisiert das Listenfeld Verzeichnis durch Senden der [**lb- \_ deletestring**](lb-deletestring.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="54a94-121">The code deletes the file by using the [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) function and updates the directory list box by sending the [**LB\_DELETESTRING**](lb-deletestring.md) message.</span></span>



```C++
INT_PTR CALLBACK DlgDelFileProc(HWND hDlg, UINT message, 
        UINT wParam, LONG lParam) 
{ 
    PTSTR pszCurDir; 
    PTSTR pszFileToDelete; 
    int iLBItem; 
    int cStringsRemaining; 
    int iRet; 
    TCHAR achBuffer[MAX_PATH]; 
    TCHAR achTemp[MAX_PATH]; 
    BOOL fResult;     
 
    switch (message) 
    { 
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
                    // first retrieve the selected file. 
                    pszFileToDelete = achBuffer; 
                    DlgDirSelectEx(hDlg, pszFileToDelete, MAX_PATH, 
                        IDC_FILELIST); 

                    // Make sure the user really wants to delete the file.
                    achTemp[MAX_PATH];
                    StringCbPrintf (achTemp, ARRAYSIZE(achTemp),  
                            TEXT("Are you sure you want to delete %s?"), 
                            pszFileToDelete);
                    iRet = MessageBox(hDlg, achTemp, L"Deleting Files", 
                        MB_YESNO | MB_ICONEXCLAMATION);
                    if (iRet == IDNO)
                        return TRUE;;

                    // Delete the file.
                    fResult = DeleteFile(pszFileToDelete); 
                    if (!fResult) 
                    { 
                        MessageBox(hDlg, L"Could not delete file.", 
                            NULL, MB_OK); 
                    } 
                    else // Remove the filename from the list box.
                    { 
                        // Get the selected item.
                        iLBItem = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_GETCURSEL, 0, 0); 
 
                        // Delete the selected item.
                        cStringsRemaining = SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                            LB_DELETESTRING, iLBItem, 0); 
 
                        // If this is not the last item, set the selection to 
                        // the item immediately following the one just deleted.
                        // Otherwise, set the selection to the last item.
                         if (cStringsRemaining > iLBItem) 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, iLBItem, 0); 
                        } 
                        else 
                        { 
                            SendMessage(GetDlgItem(hDlg, IDC_FILELIST), 
                                LB_SETCURSEL, cStringsRemaining, 0); 
                        } 
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



## <a name="related-topics"></a><span data-ttu-id="54a94-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54a94-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a94-123">Listenfeld-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="54a94-123">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="54a94-124">Informationen zu Listenfeldern</span><span class="sxs-lookup"><span data-stu-id="54a94-124">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="54a94-125">Verwenden von Listenfeldern</span><span class="sxs-lookup"><span data-stu-id="54a94-125">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 