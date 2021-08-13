---
title: Ausrichten von Text
description: Sie können DirectWrite Text mithilfe der SetTextAlignment-Methode der IDWriteTextFormat-Schnittstelle ausrichten.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a9d73443577468d794e43dc62d19e7dd24a86227ba6b5e5d8c3542cdded8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650365"
---
# <a name="how-to-align-text"></a>Ausrichten von Text

Sie können [DirectWrite](direct-write-portal.md) Text mithilfe der [**SetTextAlignment-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) der [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ausrichten, wie im folgenden Code gezeigt, der den Text zentriert.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Der Text kann am führenden oder nachgestellten Rand des Layoutfelds ausgerichtet oder zentriert werden. Die folgende Abbildung zeigt Text, für den die Ausrichtung auf [**DWRITE \_ TEXT \_ ALIGNMENT \_ LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE \_ TEXT ALIGNMENT \_ \_ CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)und [**DWRITE \_ TEXT ALIGNMENT \_ \_ TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)festgelegt ist.

![Abbildung von Textabständen mit vorn, zentriert und nachgestellter Ausrichtung](images/textalignment.png)

> [!Note]  
> Die Ausrichtung hängt von der Leserichtung ab, die obige ist für die Leserichtung von links nach rechts. Für die Leserichtung von rechts nach links wäre dies das Gegenteil.

 

Ein [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet die Ausrichtung, die für das [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) festgelegt wurde, das Sie beim Erstellen des Layouts bereitgestellt haben. Um die Textausrichtung zu ändern, verwenden [**Sie IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).

 

 
