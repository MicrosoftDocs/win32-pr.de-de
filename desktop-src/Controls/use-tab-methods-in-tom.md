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
# <a name="how-to-use-tab-methods-in-tom"></a>Verwenden von Registerkarten Methoden in Tom

Im folgenden Beispiel werden C-Funktionen bereitstellt, die die Verwendung der Registerkarten Methoden im Text Objektmodell (Tom) veranschaulichen. Es wird davon ausgegangen, dass die meisten Anwendungen eine Symbolleiste enthalten, auf der die aktuelle Position und der Typ der Registerkarten für den aktuell ausgewählten Absatz angezeigt werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-tab-method"></a>Verwenden einer Registerkarten Methode

Im folgenden Codebeispiel wird veranschaulicht, wie eine Symbolleiste mit den aktuellen Registerkarten Details aktualisiert wird.


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



### <a name="copy-tab-information"></a>Registerkarten Informationen kopieren

Im folgenden Beispiel wird gezeigt, wie nur die Registerkarten Informationen von einer [**itextpara**](/windows/desktop/api/Tom/nn-tom-itextpara) -Schnittstelle in eine andere kopiert werden. Es werden zwei Parameter benötigt: **itextpara** \* *pparameafrom* (der Absatz, von dem Tabstopps kopiert werden sollen) und **itextpara** \* *pparameafrom* (der Absatz, in den Registerkarten kopiert werden sollen).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Text Objektmodells](using-the-text-object-model.md)
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




