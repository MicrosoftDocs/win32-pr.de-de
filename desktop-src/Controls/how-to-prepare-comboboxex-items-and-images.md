---
title: Vorbereiten von ComboBoxEx-Elementen und -Bildern
description: In diesem Thema wird veranschaulicht, wie Einem ComboBoxEx-Steuerelement Elemente hinzugefügt werden.
ms.assetid: 2603DFBE-9E7A-4B2F-BE33-418997D323B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ea0b6defc7e99bd98c3dac551346280f0650da9e58a948e77ccc98aec81cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958699"
---
# <a name="how-to-prepare-comboboxex-items-and-images"></a>Vorbereiten von ComboBoxEx-Elementen und -Bildern

In diesem Thema wird veranschaulicht, wie Einem ComboBoxEx-Steuerelement Elemente hinzugefügt werden.

Um einem ComboBoxEx-Steuerelement ein Element hinzuzufügen, definieren Sie zunächst eine [**COMBOBOXEXITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Legen Sie dann den Masken **member** der -Struktur fest, um anzugeben, welche Member das Steuerelement verwenden soll. Legen Sie abschließend die angegebenen Member der -Struktur auf die gewünschten Werte fest, und senden Sie die [**CBEM \_ INSERTITEM-Nachricht,**](cbem-insertitem.md) um das Element dem Steuerelement hinzuzufügen.

Die folgende anwendungsdefinierte Funktion fügt einem vorhandenen ComboBoxEx-Steuerelement 15 Elemente hinzu.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Um einem ComboBoxEx-Steuerelement ein Element hinzuzufügen, definieren Sie zunächst eine [**COMBOBOXEXITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)


```C++
COMBOBOXEXITEM cbei;
int iCnt;


typedef struct {
    int iImage;
    int iSelectedImage;
    int iIndent;
    LPTSTR pszText;
} ITEMINFO, *PITEMINFO;

ITEMINFO IInf[ ] = {
    { 0, 3,  0, L"first"}, 
    { 1, 4,  1, L"second"},
    { 2, 5,  2, L"third"},
    { 0, 3,  0, L"fourth"},
    { 1, 4,  1, L"fifth"},
    { 2, 5,  2, L"sixth"},
    { 0, 3,  0, L"seventh"},
    { 1, 4,  1, L"eighth"},
    { 2, 5,  2, L"ninth"},
    { 0, 3,  0, L"tenth"},
    { 1, 4,  1, L"eleventh"},
    { 2, 5,  2, L"twelfth"},
    { 0, 3,  0, L"thirteenth"},
    { 1, 4,  1, L"fourteenth"},
    { 2, 5,  2, L"fifteenth"}
};
```



### <a name="step-2"></a>Schritt 2:

Legen Sie das **Maskenmitglied** der -Struktur fest, um anzugeben, welche Elemente das Steuerelement verwenden soll. Beachten Sie, **dass das Maskenelement** der [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Flagwerte enthält, die das Steuerelement anleiten, Bilder für jedes Element anzuzeigen.


```C++
// Set the mask common to all items.
cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
            CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;
```



### <a name="step-3"></a>Schritt 3:

Legen Sie die angegebenen Member der -Struktur auf die werte fest, die Sie wünschen, und senden Sie dann die [**CBEM \_ INSERTITEM-Nachricht,**](cbem-insertitem.md) um das Element dem Steuerelement hinzuzufügen.


```C++
for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
    // Initialize the COMBOBOXEXITEM struct.
    cbei.iItem          = iCnt;
    cbei.pszText        = IInf[iCnt].pszText;
    cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
    cbei.iImage         = IInf[iCnt].iImage;
    cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
    cbei.iIndent        = IInf[iCnt].iIndent;

    
    // Tell the ComboBoxEx to add the item. Return FALSE if 
    // this fails.
    if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
        return FALSE;
```



### <a name="step-4"></a>Schritt 4:

Weisen Sie die vorhandene Bildliste dem ComboBoxEx-Steuerelement zu, und legen Sie die Größe des Steuerelements fest.


```C++
// Assign the existing image list to the ComboBoxEx control 
// and return TRUE. 
// g_himl is the handle to the existing image list
SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

// Set size of control to make sure it's displayed correctly now
// that the image list is set.
SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

return TRUE; 
```



## <a name="complete-example"></a>Vollständiges Beispiel


```C++
// AddItems - Uses the CBEM_INSERTITEM message to add items to an
// existing ComboBoxEx control.

BOOL WINAPI AddItems(HWND hwndCB)
{
    
    //  Declare and init locals.
    COMBOBOXEXITEM cbei;
    int iCnt;
    

    typedef struct {
        int iImage;
        int iSelectedImage;
        int iIndent;
        LPTSTR pszText;
    } ITEMINFO, *PITEMINFO;

    ITEMINFO IInf[ ] = {
        { 0, 3,  0, L"first"}, 
        { 1, 4,  1, L"second"},
        { 2, 5,  2, L"third"},
        { 0, 3,  0, L"fourth"},
        { 1, 4,  1, L"fifth"},
        { 2, 5,  2, L"sixth"},
        { 0, 3,  0, L"seventh"},
        { 1, 4,  1, L"eighth"},
        { 2, 5,  2, L"ninth"},
        { 0, 3,  0, L"tenth"},
        { 1, 4,  1, L"eleventh"},
        { 2, 5,  2, L"twelfth"},
        { 0, 3,  0, L"thirteenth"},
        { 1, 4,  1, L"fourteenth"},
        { 2, 5,  2, L"fifteenth"}
    };

    // Set the mask common to all items.
    cbei.mask = CBEIF_TEXT | CBEIF_INDENT |
                CBEIF_IMAGE| CBEIF_SELECTEDIMAGE;

    for(iCnt=0;iCnt<MAX_ITEMS;iCnt++){
        // Initialize the COMBOBOXEXITEM struct.
        cbei.iItem          = iCnt;
        cbei.pszText        = IInf[iCnt].pszText;
        cbei.cchTextMax     = sizeof(IInf[iCnt].pszText);
        cbei.iImage         = IInf[iCnt].iImage;
        cbei.iSelectedImage = IInf[iCnt].iSelectedImage;
        cbei.iIndent        = IInf[iCnt].iIndent;
    
        
        // Tell the ComboBoxEx to add the item. Return FALSE if 
        // this fails.
        if(SendMessage(hwndCB,CBEM_INSERTITEM,0,(LPARAM)&cbei) == -1)
            return FALSE;
    }
    // Assign the existing image list to the ComboBoxEx control 
    // and return TRUE. 
    // g_himl is the handle to the existing image list
    SendMessage(hwndCB,CBEM_SETIMAGELIST,0,(LPARAM)g_himl);

    // Set size of control to make sure it's displayed correctly now
    // that the image list is set.
    SetWindowPos(hwndCB,NULL,20,20,250,120,SWP_NOACTIVATE);

    return TRUE; 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx-Steuerelementreferenz](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 