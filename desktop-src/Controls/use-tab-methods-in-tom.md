---
title: Verwenden von Registerkarten Methoden in Tom
description: Im folgenden Beispiel werden C-Funktionen bereitstellt, die die Verwendung der Registerkarten Methoden im Text Objektmodell (Tom) veranschaulichen.
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858106"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="d5945-103">Verwenden von Registerkarten Methoden in Tom</span><span class="sxs-lookup"><span data-stu-id="d5945-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="d5945-104">Im folgenden Beispiel werden C-Funktionen bereitstellt, die die Verwendung der Registerkarten Methoden im Text Objektmodell (Tom) veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="d5945-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="d5945-105">Es wird davon ausgegangen, dass die meisten Anwendungen eine Symbolleiste enthalten, auf der die aktuelle Position und der Typ der Registerkarten für den aktuell ausgewählten Absatz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d5945-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d5945-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d5945-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d5945-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="d5945-107">Technologies</span></span>

-   [<span data-ttu-id="d5945-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d5945-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d5945-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d5945-109">Prerequisites</span></span>

-   <span data-ttu-id="d5945-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="d5945-110">C/C++</span></span>
-   <span data-ttu-id="d5945-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d5945-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d5945-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d5945-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="d5945-113">Verwenden einer Registerkarten Methode</span><span class="sxs-lookup"><span data-stu-id="d5945-113">Use a Tab Method</span></span>

<span data-ttu-id="d5945-114">Im folgenden Codebeispiel wird veranschaulicht, wie eine Symbolleiste mit den aktuellen Registerkarten Details aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5945-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="d5945-115">Registerkarten Informationen kopieren</span><span class="sxs-lookup"><span data-stu-id="d5945-115">Copy Tab Information</span></span>

<span data-ttu-id="d5945-116">Im folgenden Beispiel wird gezeigt, wie nur die Registerkarten Informationen von einer [**itextpara**](/windows/desktop/api/Tom/nn-tom-itextpara) -Schnittstelle in eine andere kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5945-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="d5945-117">Es werden zwei Parameter benötigt: **itextpara** \* *pparameafrom* (der Absatz, von dem Tabstopps kopiert werden sollen) und **itextpara** \* *pparameafrom* (der Absatz, in den Registerkarten kopiert werden sollen).</span><span class="sxs-lookup"><span data-stu-id="d5945-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="d5945-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5945-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5945-119">Verwenden des Text Objektmodells</span><span class="sxs-lookup"><span data-stu-id="d5945-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="d5945-120">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d5945-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d5945-121">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d5945-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




