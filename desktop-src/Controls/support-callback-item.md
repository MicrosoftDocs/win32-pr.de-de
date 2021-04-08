---
title: Vorgehensweise beim unterstützen von Rückruf Elementen
description: In diesem Thema wird veranschaulicht, wie Rückruf Elemente unterstützt werden.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949228"
---
# <a name="how-to-support-callback-items"></a>Vorgehensweise beim unterstützen von Rückruf Elementen

In diesem Thema wird veranschaulicht, wie Rückruf Elemente unterstützt werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Wenn die Anwendung Rückruf Elemente in einem ComboBoxEx-Steuerelement verwendet, muss Sie darauf vorbereitet sein, den [cben \_ getdispinfo](cben-getdispinfo.md) -Benachrichtigungs Code zu verarbeiten. Ein ComboBoxEx-Steuerelement sendet diese Benachrichtigung, wenn der Besitzer bestimmte Element Informationen bereitstellen muss. Weitere Informationen zu Rückruf Elementen finden Sie unter [Callback Items (Rückruf](comboboxex-controls.md)Elemente).

Die folgende Anwendungs definierte Funktion verarbeitet [cben \_ getdispinfo](cben-getdispinfo.md) durch Bereitstellen von Attributen für ein bestimmtes Element. Beachten Sie, dass der **Mask** -Member der eingehenden [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur auf cbeif \_ di \_ SetItem festgelegt wird. Wenn Sie **Mask** auf diesen Wert festlegen, behält das Steuerelement die Element Informationen bei, sodass die Informationen nicht erneut angefordert werden müssen.

## <a name="complete-example"></a>Vollständiges Beispiel


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu ComboBoxEx-Steuerelementen](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx-Steuerelement Verweis](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 