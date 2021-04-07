---
title: Anpassen von Symbolleisten
description: Die meisten Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen bequemen Zugriff auf die Programmfunktionalität zu ermöglichen.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104038706"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="2cf40-103">Anpassen von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="2cf40-103">How to Customize Toolbars</span></span>

<span data-ttu-id="2cf40-104">Die meisten Windows-basierten Anwendungen verwenden Symbolleisten-Steuerelemente, um Benutzern einen bequemen Zugriff auf die Programmfunktionalität zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="2cf40-105">Statische Symbolleisten haben jedoch gewisse Mängel – z. b. zu wenig Platz, um alle verfügbaren Tools effektiv anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="2cf40-106">Die Lösung für dieses Problem besteht darin, die Symbolleisten Ihrer Anwendung Benutzer anpassbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="2cf40-107">Anschließend können Benutzer auswählen, nur die Tools anzuzeigen, die Sie benötigen, und Sie können Sie auf eine Weise organisieren, die Ihrem persönlichen Arbeitsstil entspricht.</span><span class="sxs-lookup"><span data-stu-id="2cf40-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="2cf40-108">Symbolleisten in Dialogfeldern können nicht angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="2cf40-109">Um die Anpassung zu aktivieren, schließen Sie beim Erstellen des Toolbar-Steuer Elements das Stil-Flag für die [**CCS \_**](common-control-styles.md) -Anpassung ein.</span><span class="sxs-lookup"><span data-stu-id="2cf40-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="2cf40-110">Es gibt zwei grundlegende Ansätze für die Anpassung:</span><span class="sxs-lookup"><span data-stu-id="2cf40-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="2cf40-111">Das Anpassungs Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="2cf40-111">The customization dialog box.</span></span> <span data-ttu-id="2cf40-112">Dieses vom System bereitgestellte Dialogfeld ist der einfachste Ansatz.</span><span class="sxs-lookup"><span data-stu-id="2cf40-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="2cf40-113">Der Benutzer erhält eine grafische Benutzeroberfläche, die es Ihnen ermöglicht, Symbole hinzuzufügen, zu löschen oder zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="2cf40-114">Drag & Drop-Tools.</span><span class="sxs-lookup"><span data-stu-id="2cf40-114">Dragging and dropping tools.</span></span> <span data-ttu-id="2cf40-115">Durch das Implementieren der Drag & Drop-Funktionalität können Benutzer Tools an einen anderen Speicherort auf der Symbolleiste verschieben oder löschen, indem Sie Sie aus der Symbolleiste ziehen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="2cf40-116">Sie bietet Benutzern eine schnelle und einfache Möglichkeit, Ihre Symbolleiste zu organisieren, Sie ermöglicht Ihnen jedoch nicht das Hinzufügen von Tools.</span><span class="sxs-lookup"><span data-stu-id="2cf40-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="2cf40-117">Sie können je nach den Anforderungen der Anwendung entweder einen Ansatz oder beides implementieren.</span><span class="sxs-lookup"><span data-stu-id="2cf40-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="2cf40-118">Keines dieser beiden Ansätze für die Anpassung bietet einen integrierten Mechanismus, wie z. b. die Schaltfläche Abbrechen oder rückgängig, um die Symbolleiste in den früheren Zustand zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2cf40-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="2cf40-119">Sie müssen explizit die ToolBar-Steuerelement-API verwenden, um den Status der Symbolleiste zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="2cf40-120">Bei Bedarf können Sie diese gespeicherten Informationen später zum Wiederherstellen des ursprünglichen Zustands der Symbolleiste verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2cf40-121">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="2cf40-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2cf40-122">Technologien</span><span class="sxs-lookup"><span data-stu-id="2cf40-122">Technologies</span></span>

-   [<span data-ttu-id="2cf40-123">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="2cf40-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2cf40-124">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2cf40-124">Prerequisites</span></span>

-   <span data-ttu-id="2cf40-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="2cf40-125">C/C++</span></span>
-   <span data-ttu-id="2cf40-126">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="2cf40-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2cf40-127">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="2cf40-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="2cf40-128">Dialog Feld "Anpassung"</span><span class="sxs-lookup"><span data-stu-id="2cf40-128">Customization Dialog Box</span></span>

<span data-ttu-id="2cf40-129">Das Dialogfeld Anpassung wird vom Symbolleisten-Steuerelement bereitgestellt, um Benutzern eine einfache Möglichkeit zum Hinzufügen, verschieben oder Löschen von Tools zu bieten.</span><span class="sxs-lookup"><span data-stu-id="2cf40-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="2cf40-130">Benutzer können Sie starten, indem Sie auf die Symbolleiste doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="2cf40-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="2cf40-131">Anwendungen können das Dialogfeld Anpassung Programm gesteuert starten, indem Sie das Symbolleisten-Steuerelement an eine TB-Anpassungs Nachricht senden. [**\_**](tb-customize.md)</span><span class="sxs-lookup"><span data-stu-id="2cf40-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="2cf40-132">Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld für die Symbolleisten Anpassung.</span><span class="sxs-lookup"><span data-stu-id="2cf40-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![Screenshot eines Fensters mit einer Symbolleiste mit drei Elementen und einem Dialogfeld mit Listen mit den verfügbaren und aktuellen Symbolleisten Schaltflächen](images/tb-customdlg.png)

<span data-ttu-id="2cf40-134">Die Tools im Listenfeld auf der rechten Seite sind die Tools, die derzeit auf der Symbolleiste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="2cf40-135">Zunächst enthält diese Liste die Tools, die Sie beim Erstellen der Symbolleiste angeben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="2cf40-136">Das Listenfeld Links enthält die Tools, die zur Symbolleiste hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="2cf40-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="2cf40-137">Die Anwendung ist dafür verantwortlich, diese Liste zu füllen (außer mit dem Trennzeichen, das automatisch angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="2cf40-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="2cf40-138">Das Symbolleisten-Steuerelement benachrichtigt Ihre Anwendung, dass es ein Anpassungs Dialogfeld startet, indem es das übergeordnete Fenster einen [TBN \_ begincustomibenachrichtigungscode](tbn-beginadjust.md) gefolgt von einem [TBN \_ initcustomibenachrichtigungscode](tbn-initcustomize.md) sendet.</span><span class="sxs-lookup"><span data-stu-id="2cf40-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="2cf40-139">In den meisten Fällen ist es nicht erforderlich, dass die Anwendung auf diese Benachrichtigungs Codes antwortet.</span><span class="sxs-lookup"><span data-stu-id="2cf40-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="2cf40-140">Wenn Sie jedoch nicht möchten, dass das Dialogfeld "Symbolleiste anpassen" eine Hilfe Schaltfläche anzeigt, behandeln Sie TBN \_ initcustomize, indem Sie tbnrf \_ hidehelp zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="2cf40-141">Anschließend sammelt das Symbolleisten-Steuerelement die Informationen, die benötigt werden, um das Dialogfeld zu initialisieren, indem drei Reihe von Benachrichtigungs Codes in der folgenden Reihenfolge gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="2cf40-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="2cf40-142">Ein [TBN \_ queryinsert](tbn-queryinsert.md) -Benachrichtigungs Code für jede Schaltfläche auf der Symbolleiste, um zu bestimmen, wo Schaltflächen eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="2cf40-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="2cf40-143">Gibt **false** zurück, um zu verhindern, dass eine Schaltfläche links neben der in der Benachrichtigungs Meldung angegebenen Schaltfläche eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="2cf40-144">Wenn Sie für  alle TBN- \_ queryinsert-Benachrichtigungs Codes false zurückgeben, wird das Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="2cf40-145">Einen [TBN- \_ querydelete](tbn-querydelete.md) -Benachrichtigungs Code für jedes Tool, das sich zurzeit auf der Symbolleiste befindet.</span><span class="sxs-lookup"><span data-stu-id="2cf40-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="2cf40-146">Gibt **true** zurück, wenn ein Tool gelöscht werden kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2cf40-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="2cf40-147">Eine Reihe von [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Benachrichtigungs Codes, um die Liste der verfügbaren Schaltflächen aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="2cf40-148">Um der Liste eine Schaltfläche hinzuzufügen, füllen Sie die [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur aus, die mit dem Benachrichtigungs Code übergebenen wird, und geben Sie **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf40-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="2cf40-149">Wenn keine weiteren Tools hinzugefügt werden können, geben Sie **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf40-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="2cf40-150">Beachten Sie, dass Sie Informationen für Schaltflächen zurückgeben können, die sich bereits auf der Symbolleiste befinden. Diese Schaltflächen werden nicht zur Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="2cf40-151">Daraufhin wird das Dialogfeld angezeigt, und der Benutzer kann damit beginnen, die Symbolleiste anzupassen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="2cf40-152">Wenn das Dialogfeld geöffnet ist, kann Ihre Anwendung abhängig von den Aktionen des Benutzers eine Vielzahl von Benachrichtigungs Codes empfangen:</span><span class="sxs-lookup"><span data-stu-id="2cf40-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="2cf40-153">[TBN \_ Queryinsert](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="2cf40-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="2cf40-154">Der Benutzer hat den Speicherort eines Tools auf der Symbolleiste geändert oder ein Tool hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="2cf40-155">Gibt **false** zurück, um zu verhindern, dass das Tool an dieser Stelle eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="2cf40-156">[TBN \_ Delta Button](tbn-deletingbutton.md).</span><span class="sxs-lookup"><span data-stu-id="2cf40-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="2cf40-157">Der Benutzer ist im Begriff, ein Tool aus der Symbolleiste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="2cf40-158">[TBN \_ "Custhelp](tbn-custhelp.md)".</span><span class="sxs-lookup"><span data-stu-id="2cf40-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="2cf40-159">Der Benutzer hat auf die Schaltfläche "Hilfe" geklickt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="2cf40-160">[TBN \_ Toolbarchange](tbn-toolbarchange.md).</span><span class="sxs-lookup"><span data-stu-id="2cf40-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="2cf40-161">Der Benutzer hat ein Tool hinzugefügt, verschoben oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2cf40-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="2cf40-162">[TBN \_ Zurücksetzen](tbn-reset.md).</span><span class="sxs-lookup"><span data-stu-id="2cf40-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="2cf40-163">Der Benutzer hat auf die Schaltfläche Zurücksetzen geklickt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="2cf40-164">Nachdem das Dialogfeld zerstört wurde, empfängt Ihre Anwendung einen [TBN- \_ endanpassungs](tbn-endadjust.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="2cf40-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="2cf40-165">Das folgende Codebeispiel zeigt eine Möglichkeit zum Implementieren der Symbolleisten Anpassung.</span><span class="sxs-lookup"><span data-stu-id="2cf40-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="2cf40-166">Drag & Drop-Tools</span><span class="sxs-lookup"><span data-stu-id="2cf40-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="2cf40-167">Benutzer können die Schaltflächen auf einer Symbolleiste auch neu anordnen, indem Sie die UMSCHALTTASTE gedrückt halten und die Schaltfläche an eine andere Position ziehen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="2cf40-168">Der Drag & Drop-Prozess wird automatisch vom Symbolleisten-Steuerelement behandelt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="2cf40-169">Sie zeigt ein inaktives Bild der Schaltfläche an, während Sie gezogen wird, und ordnet die Symbolleiste nach dem Ablegen neu an.</span><span class="sxs-lookup"><span data-stu-id="2cf40-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="2cf40-170">Benutzer können auf diese Weise keine Schaltflächen hinzufügen, aber Sie können eine Schaltfläche löschen, indem Sie Sie auf der Symbolleiste ablegen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="2cf40-171">Obwohl das Symbolleisten-Steuerelement diesen Vorgang normalerweise automatisch durchführt, sendet es die Anwendung auch zwei Benachrichtigungs Codes: [TBN \_ querydelete](tbn-querydelete.md) und [TBN \_ queryinsert](tbn-queryinsert.md).</span><span class="sxs-lookup"><span data-stu-id="2cf40-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="2cf40-172">Um den Drag & Drop-Prozess zu steuern, behandeln Sie diese Benachrichtigungs Codes wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2cf40-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="2cf40-173">Der [TBN- \_ querydelete](tbn-querydelete.md) -Benachrichtigungs Code wird gesendet, sobald der Benutzer versucht, die Schaltfläche zu verschieben, bevor die Schaltfläche "Ghost" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="2cf40-174">Gibt **false** zurück, um zu verhindern, dass die Schaltfläche verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="2cf40-175">Wenn Sie " **true**" zurückgeben, kann der Benutzer das Tool entweder verschieben oder löschen, indem es aus der Symbolleiste entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="2cf40-176">Wenn ein Tool verschoben werden kann, kann es gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="2cf40-177">Wenn der Benutzer jedoch ein Tool löscht, sendet das Symbolleisten-Steuerelement ihrer Anwendung einen [TBN- \_ Delta-Schalt](tbn-deletingbutton.md) Flächen-Benachrichtigungs Code. an diesem Punkt können Sie auswählen, dass die Schaltfläche an ihrer ursprünglichen Position wieder eingefügt werden soll, wodurch der Löschvorgang abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="2cf40-178">Der [TBN- \_ queryinsert](tbn-queryinsert.md) -Benachrichtigungs Code wird gesendet, wenn der Benutzer versucht, die Schaltfläche auf der Symbolleiste zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="2cf40-179">Um zu verhindern, dass die Schaltfläche, die verschoben wird, Links von der in der Benachrichtigung angegebenen Schaltfläche abgelegt wird, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="2cf40-180">Dieser Benachrichtigungs Code wird nicht gesendet, wenn der Benutzer das Tool von der Symbolleiste löscht.</span><span class="sxs-lookup"><span data-stu-id="2cf40-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="2cf40-181">Wenn der Benutzer versucht, eine Schaltfläche zu ziehen, ohne auch die UMSCHALTTASTE zu drücken, verarbeitet das Symbolleisten-Steuerelement den Drag & Drop-Vorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="2cf40-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="2cf40-182">Die Anwendung sendet jedoch einen [TBN- \_ BeginDrag](tbn-begindrag.md) -Benachrichtigungs Code, um den Start eines Zieh Vorgangs anzugeben, und einen [TBN- \_ EndDrag](tbn-enddrag.md) -Benachrichtigungs Code, um das Ende anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="2cf40-183">Wenn Sie diese Art von Drag & amp; Drop aktivieren möchten, muss die Anwendung diese Benachrichtigungs Codes verarbeiten, die erforderliche Benutzeroberfläche bereitstellen und die Symbolleiste so ändern, dass Sie Änderungen widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="2cf40-184">Speichern und Wiederherstellen von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="2cf40-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="2cf40-185">Wenn Sie eine Symbolleiste anpassen, muss Ihre Anwendung möglicherweise Informationen speichern, damit Sie den ursprünglichen Zustand der Symbolleiste wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="2cf40-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="2cf40-186">Um das Speichern oder Wiederherstellen eines Symbolleisten Zustands zu initiieren, senden Sie das Symbolleisten-Steuerelement eine [**TB \_ saverestore**](tb-saverestore.md) -Nachricht, bei der *LPARAM* auf **true** festgelegt</span><span class="sxs-lookup"><span data-stu-id="2cf40-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="2cf40-187">Der *LPARAM* -Wert dieser Meldung gibt an, ob Sie einen Speicher-oder Wiederherstellungs Vorgang anfordern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="2cf40-188">Nachdem die Nachricht gesendet wurde, gibt es zwei Möglichkeiten, den Speicher-/Wiederherstellungsvorgang zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="2cf40-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="2cf40-189">Mit den allgemeinen Steuerelementen [Version 4,72](common-control-versions.md) und früher müssen Sie einen [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md) -Handler implementieren.</span><span class="sxs-lookup"><span data-stu-id="2cf40-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="2cf40-190">Das Symbolleisten-Steuerelement sendet diesen Benachrichtigungs Code, um Informationen zu den einzelnen Schaltflächen bei der Wiederherstellung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="2cf40-191">Version 5,80 enthält eine Option zum Speichern/Wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="2cf40-192">Zu Beginn des Prozesses und beim Speichern oder Wiederherstellen der einzelnen Schaltflächen erhält die Anwendung einen [TBN- \_ Save](tbn-save.md) -oder [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="2cf40-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="2cf40-193">Um diese Option verwenden zu können, müssen Sie Benachrichtigungs Handler implementieren, um die Bitmap-und Zustandsinformationen bereitzustellen, die zum erfolgreichen speichern oder Wiederherstellen des Symbolleisten Zustands benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="2cf40-194">Symbolleisten Zustände werden in einem Datenstrom gespeichert, der aus Blöcken von shelldefinierten Daten besteht, die sich mit Blöcken von Anwendungs definierten Daten abwechseln.</span><span class="sxs-lookup"><span data-stu-id="2cf40-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="2cf40-195">Ein Datenblock jedes Typs wird für jede Schaltfläche gespeichert, zusammen mit einem optionalen Block globaler Daten, die Anwendungen am Anfang des Streams platzieren können.</span><span class="sxs-lookup"><span data-stu-id="2cf40-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="2cf40-196">Während des Speicher Vorgangs fügt der [TBN- \_ Speicher](tbn-save.md) Handler die Anwendungs definierten Blöcke zum Datenstrom hinzu.</span><span class="sxs-lookup"><span data-stu-id="2cf40-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="2cf40-197">Während des Wiederherstellungs Vorgangs liest der [TBN- \_ Wiederherstellungs](tbn-restore.md) Handler jeden Block und übergibt der Shell die Informationen, die er zum Rekonstruieren der Symbolleiste benötigt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="2cf40-198">Behandeln einer TBN- \_ Speicher Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2cf40-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="2cf40-199">Der erste [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code wird zu Beginn des Speicher Vorgangs gesendet.</span><span class="sxs-lookup"><span data-stu-id="2cf40-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="2cf40-200">Bevor alle Schaltflächen gespeichert werden, werden die Elemente der [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) -Struktur wie in der folgenden Tabelle dargestellt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="2cf40-201">Member</span><span class="sxs-lookup"><span data-stu-id="2cf40-201">Member</span></span>       | <span data-ttu-id="2cf40-202">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2cf40-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf40-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="2cf40-203">**iItem**</span></span>    | <span data-ttu-id="2cf40-204">–1</span><span class="sxs-lookup"><span data-stu-id="2cf40-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2cf40-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="2cf40-205">**cbData**</span></span>   | <span data-ttu-id="2cf40-206">Die Menge an Arbeitsspeicher, die für shelldefinierte Daten benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2cf40-207">**cbuttons**</span><span class="sxs-lookup"><span data-stu-id="2cf40-207">**cButtons**</span></span> | <span data-ttu-id="2cf40-208">Die Anzahl der Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2cf40-209">**pData**</span><span class="sxs-lookup"><span data-stu-id="2cf40-209">**pData**</span></span>    | <span data-ttu-id="2cf40-210">Die berechnete Speichermenge, die für Anwendungs definierte Daten benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="2cf40-211">Normalerweise fügen Sie einige globale Daten und Daten für jede Schaltfläche ein.</span><span class="sxs-lookup"><span data-stu-id="2cf40-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="2cf40-212">Fügen Sie diesen Wert zu **cbData** hinzu, und weisen Sie **pData** ausreichend Arbeitsspeicher zu, um die Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="2cf40-213">**pcurrent**</span><span class="sxs-lookup"><span data-stu-id="2cf40-213">**pCurrent**</span></span> | <span data-ttu-id="2cf40-214">Das erste nicht verwendete Byte im Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="2cf40-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="2cf40-215">Wenn Sie keine globalen Symbolleisten Informationen benötigen, legen Sie **pcurrent**  =  **pData** so fest, dass Sie auf den Anfang des Datenstroms zeigt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="2cf40-216">Wenn Sie globale Symbolleisten Informationen benötigen, speichern Sie diese bei **pData**, und legen Sie dann **pcurrent** auf den Anfang des nicht verwendeten Teils des Datenstroms fest, bevor Sie zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="2cf40-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="2cf40-217">Wenn Sie einige globale Symbolleisten Informationen hinzufügen möchten, platzieren Sie Sie am Anfang des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="2cf40-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="2cf40-218">Setzen Sie **pcurrent** am Ende der globalen Daten, sodass es auf den Anfang des nicht verwendeten Teils des Datenstroms zeigt, und geben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf40-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="2cf40-219">Nachdem Sie zurückgegeben haben, beginnt die Shell, Schaltflächen Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="2cf40-220">Sie fügt die shelldefinierten Daten für die erste Schaltfläche bei **pcurrent** hinzu und **verschiebt dann pcurrent** auf den Anfang des nicht verwendeten Teils.</span><span class="sxs-lookup"><span data-stu-id="2cf40-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="2cf40-221">Nachdem jede Schaltfläche gespeichert wurde, wird ein [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code gesendet, und [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) wird zurückgegeben, wobei diese Member wie folgt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="2cf40-222">Member</span><span class="sxs-lookup"><span data-stu-id="2cf40-222">Member</span></span>                       | <span data-ttu-id="2cf40-223">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2cf40-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf40-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="2cf40-224">**iItem**</span></span>                    | <span data-ttu-id="2cf40-225">Der null basierte Index der Schaltflächen Nummer.</span><span class="sxs-lookup"><span data-stu-id="2cf40-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="2cf40-226">**pcurrent**</span><span class="sxs-lookup"><span data-stu-id="2cf40-226">**pCurrent**</span></span>                 | <span data-ttu-id="2cf40-227">Ein Zeiger auf das erste nicht verwendete Byte im Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="2cf40-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="2cf40-228">Wenn Sie zusätzliche Informationen über die Schaltfläche speichern möchten, speichern Sie Sie an dem Speicherort, auf den **pcurrent** verweist, und aktualisieren Sie **pcurrent** , um auf den ersten nicht verwendeten Teil des Datenstroms zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="2cf40-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2cf40-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="2cf40-230">Eine [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur, die die Schaltfläche beschreibt, die gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="2cf40-231">Beim Empfang des Benachrichtigungs Codes sollten Sie alle von Ihnen benötigten Schaltflächen spezifischen Informationen aus [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2cf40-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="2cf40-232">Beachten Sie, dass Sie beim Hinzufügen einer Schaltfläche den **dwdata** -Member von **TBBUTTON** verwenden können, um anwendungsspezifische Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2cf40-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="2cf40-233">Laden Sie die Daten in den Datenstrom bei **pcurrent**.</span><span class="sxs-lookup"><span data-stu-id="2cf40-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="2cf40-234">**Pcurrent** wird an das Ende der Daten zurückgegeben, wobei wiederum auf den Anfang des nicht verwendeten Teils des Streams verwiesen wird und zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2cf40-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="2cf40-235">Die Shell wechselt dann zur Schaltfläche "weiter", fügt die Informationen zu **pData** hinzu, **verschiebt "pcurrent**", lädt " [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)" und sendet einen weiteren [TBN- \_ Speicher](tbn-save.md) Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="2cf40-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="2cf40-236">Dieser Prozess wird fortgesetzt, bis alle Schaltflächen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="2cf40-237">Wiederherstellen gespeicherter Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="2cf40-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="2cf40-238">Der Wiederherstellungs Vorgang kehrt im Grunde den Speicher Prozess um.</span><span class="sxs-lookup"><span data-stu-id="2cf40-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="2cf40-239">Zu Beginn empfängt Ihre Anwendung einen [TBN- \_ Wiederherstellungs](tbn-restore.md) Benachrichtigungs Code mit dem **iItem** -Member der [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) -Struktur, die auf – 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2cf40-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="2cf40-240">Der **cbData** -Member wird auf die Größe von **pData** festgelegt, und die **cbuttons** werden auf die Anzahl der Schaltflächen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="2cf40-241">Der Benachrichtigungs Handler sollte die globalen Informationen, die beim Speichern am Anfang von **pData** platziert wurden, extrahieren und die **pcurrent** -Funktion bis zum Anfang des ersten Blocks von shelldefinierten Daten voranbringen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="2cf40-242">Legen Sie **cbytesperrecord** auf die Größe der Datenblöcke fest, die Sie zum Speichern der Schaltflächen Daten verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2cf40-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="2cf40-243">Legen Sie **cbuttons** auf die Anzahl der Schaltflächen fest, und geben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf40-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="2cf40-244">Der nächste [**nmtbrestore**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) ist für die erste Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="2cf40-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="2cf40-245">Der **pcurrent** -Member zeigt auf den Anfang des ersten Blocks von Schaltflächen Daten, und **iItem** wird auf den Schaltflächen Index festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="2cf40-246">Extrahieren Sie diese Daten und **pcurrent**.</span><span class="sxs-lookup"><span data-stu-id="2cf40-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="2cf40-247">Laden Sie die Daten in [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), und geben Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf40-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="2cf40-248">Um eine Schaltfläche auf der wiederhergestellten Symbolleiste auszulassen, legen Sie den **idcommand** -Member von **TBBUTTON** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="2cf40-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="2cf40-249">Die Shell wiederholt den Vorgang für die verbleibenden Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="2cf40-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="2cf40-250">Zusätzlich zu den Nachrichten [**nmtbsave**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) und **nmtbrestore** können Sie auch Nachrichten wie z. [b. TBN \_ Reset](tbn-reset.md) zum Speichern und Wiederherstellen einer Symbolleiste verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cf40-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="2cf40-251">Im folgenden Codebeispiel wird eine Symbolleiste vor der Anpassung gespeichert und wieder hergestellt, wenn die Anwendung eine [TBN \_ ](tbn-reset.md) -Zurücksetzungs Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="2cf40-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="2cf40-252">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cf40-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cf40-253">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="2cf40-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="2cf40-254">**Bild-/Indexwerte der Symbolleiste Standard**</span><span class="sxs-lookup"><span data-stu-id="2cf40-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="2cf40-255">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="2cf40-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




