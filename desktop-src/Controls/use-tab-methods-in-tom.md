---
title: Verwenden von Registerkartenmethoden in TOM
description: Das folgende Beispiel enthält C-Funktionen, die die Verwendung der Registerkartenmethoden im Textobjektmodell (Text Object Model, TOM) veranschaulichen.
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b4a101c2deb3c22993f41b11ee94df6ac738da41963046f02a072f3eaa6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828612"
---
# <a name="how-to-use-tab-methods-in-tom"></a>Verwenden von Registerkartenmethoden in TOM

Das folgende Beispiel enthält C-Funktionen, die die Verwendung der Registerkartenmethoden im Textobjektmodell (Text Object Model, TOM) veranschaulichen. Es wird davon ausgegangen, dass die meisten Anwendungen eine Symbolleiste enthalten, die die aktuelle Position und den Typ der Registerkarten für den aktuell ausgewählten Absatz zeigt.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-a-tab-method"></a>Verwenden einer Tab-Methode

Im folgenden Codebeispiel wird veranschaulicht, wie eine Symbolleiste mit den aktuellen Registerkartendetails aktualisiert wird.


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



### <a name="copy-tab-information"></a>Kopieren von Registerkarteninformationen

Das folgende Beispiel zeigt, wie nur die Registerkarteninformationen von einer [**ITextPara-Schnittstelle**](/windows/desktop/api/Tom/nn-tom-itextpara) in eine andere kopiert werden. Es werden zwei Parameter verwendet: **ITextPara** pParaFrom (der Absatz, aus dem Registerkarten kopiert werden sollen) und \*  **ITextPara** \* *pParaFrom* (der Absatz, in den Registerkarten kopiert werden sollen).


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

[Verwenden des Textobjektmodells](using-the-text-object-model.md)
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




