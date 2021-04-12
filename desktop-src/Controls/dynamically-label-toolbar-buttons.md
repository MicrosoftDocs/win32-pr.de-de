---
title: Dynamisches bezeichnen von Symbolleisten-Schaltflächen
description: Mithilfe der TB-SetButtonInfo-Meldung können Sie einer vorhandenen Schaltfläche Text zuweisen \_ .
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472428"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="ff678-103">Dynamisches bezeichnen von Symbolleisten-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="ff678-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="ff678-104">Mithilfe der [**TB- \_ SetButtonInfo**](tb-setbuttoninfo.md) -Meldung können Sie einer vorhandenen Schaltfläche Text zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ff678-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff678-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="ff678-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff678-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="ff678-106">Technologies</span></span>

-   [<span data-ttu-id="ff678-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ff678-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ff678-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ff678-108">Prerequisites</span></span>

-   <span data-ttu-id="ff678-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff678-109">C/C++</span></span>
-   <span data-ttu-id="ff678-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ff678-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ff678-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ff678-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="ff678-112">Dynamisches bezeichnen einer Symbolleisten-Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ff678-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="ff678-113">Im folgenden Beispiel wird veranschaulicht, wie Sie den Text der dritten Schaltfläche in den vorherigen Beispielen von " **Speichern** " in " **Speichern** unter" ändern.</span><span class="sxs-lookup"><span data-stu-id="ff678-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="ff678-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff678-114">Remarks</span></span>

<span data-ttu-id="ff678-115">Wenn Sie den Text einer Schaltfläche mithilfe von [**TB \_ SetButtonInfo**](tb-setbuttoninfo.md) ändern, wirkt sich dies nicht auf die Zeichenfolge aus, die dieser Schaltfläche in der internen Zeichen folgen Liste zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ff678-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="ff678-116">Wenn Sie der internen Textliste eine Symbolleisten-Schaltflächen Zeichenfolge hinzufügen, können Sie den Index dieser Zeichenfolge nicht abrufen, indem Sie [TBN \_ getbuttoninfo](tbn-getbuttoninfo.md)aufrufen – Sie müssen stattdessen die [**TB \_ getbutton**](tb-getbutton.md) -Nachricht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff678-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff678-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff678-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff678-118">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="ff678-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="ff678-119">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ff678-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




