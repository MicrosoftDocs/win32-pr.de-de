---
title: Unterstützen von Rückrufelementen
description: In diesem Thema wird veranschaulicht, wie Rückrufelemente unterstützt werden.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df078b8be8cd02f56592a74de4242b515974a740df01d3cd4bd36074d5f8e022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968220"
---
# <a name="how-to-support-callback-items"></a>Unterstützen von Rückrufelementen

In diesem Thema wird veranschaulicht, wie Rückrufelemente unterstützt werden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Wenn Ihre Anwendung Rückrufelemente in einem ComboBoxEx-Steuerelement verwenden soll, muss sie für die Handhabung des [CBEN \_ GETDISPINFO-Benachrichtigungscodes](cben-getdispinfo.md) vorbereitet sein. Ein ComboBoxEx-Steuerelement sendet diese Benachrichtigung, wenn der Besitzer bestimmte Elementinformationen bereitstellen muss. Weitere Informationen zu Rückrufelementen finden Sie unter [Rückrufelemente.](comboboxex-controls.md)

Die folgende anwendungsdefinierte Funktion verarbeitet [CBEN \_ GETDISPINFO,](cben-getdispinfo.md) indem Attribute für ein bestimmtes Element angegeben werden. Beachten Sie, dass der **Mask-Member** der eingehenden [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) auf CBEIF \_ DI \_ SETITEM festgelegt wird. Durch **Festlegen der** Maske auf diesen Wert behält das Steuerelement die Elementinformationen bei, sodass es die Informationen nicht erneut anfordern muss.

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

[ComboBoxEx-Steuerelementreferenz](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Verwenden von ComboBoxEx-Steuerelementen](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 