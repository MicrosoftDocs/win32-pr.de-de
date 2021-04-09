---
title: Verwenden eines doppelten Schriftart Duplikats
description: In diesem Abschnitt wird erläutert, wie Sie mit einem Schriftart Duplikat eine Reihe von Änderungen auf einen Textbereich anwenden.
ms.assetid: CF0123E5-313F-4583-872F-6FE954F1C9E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dce0481b59fe9955b93a00b2c0d703c5c695ef
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103948532"
---
# <a name="how-to-use-a-font-duplicate"></a>Verwenden eines doppelten Schriftart Duplikats

In diesem Abschnitt wird erläutert, wie Sie mit einem Schriftart Duplikat eine Reihe von Änderungen auf einen Textbereich anwenden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-font-duplicate"></a>Schriftart Duplikat verwenden

Im folgenden Beispiel wird gezeigt, wie mit einem Schriftart Duplikat eine Reihe von Änderungen auf einen Bereich gleichzeitig angewendet werden können.


```C++
void ChangeFontNameSizeBold(ITextSelection *pSel)
{
    ITextFont *pFontSel      = NULL
    ITextFont *FontDuplicate = NULL;
    
    // Get ITextFont version of non-duplicated font.
    if (FAILED(pSel->GetFont( &pFontSel))
        return;

    // Duplicate the font.
    pFontSel->GetValue(&pFontDuplicate);
    pFontSel->Release();
    
    if(!pFontDuplicate)
        return;

   // Changes here happen only to the underlying data structure, 
   // such as a CHARFORMAT, in the duplicate - NOT to the actual story text.

    BSTR bstrTemp = UnicodeBstrFromAnsi("Times New Roman");   // Font name
    
    pFontDuplicate->SetName(bstrTemp);
    SysFreeString(bstrTemp);
    
    pFontDuplicate->SetBold(tomTrue);                        // Bold
    pFontDuplicate->SetSize(10.5);                           // 10.5 point font.
    pFontDuplicate->SetAnimation(tomBlackMarchingAnts);

    // Apply the change to text as one change: one screen update, one undo. 
    // You can also apply the font object to different ranges before you free it.
    
    pSel->SetFont(pFontDuplicate);
    
    pFontDuplicate->Release();
    
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

 

 




