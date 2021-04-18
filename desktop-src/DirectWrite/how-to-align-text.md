---
title: Ausrichten von Text
description: Sie können DirectWrite-Text mithilfe der SetTextAlignment-Methode der idschreitetextformat-Schnittstelle ausrichten.
ms.assetid: 7f79dcff-11f6-4e74-b5bd-98bfebe6e393
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb765860f2fbaac94409aa9ec20c2269beb45cbb
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "106372549"
---
# <a name="how-to-align-text"></a>Ausrichten von Text

Sie können [DirectWrite](direct-write-portal.md) -Text mithilfe der [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) -Methode der [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle ausrichten, wie im folgenden Code gezeigt, in dem der Text zentriert ist.


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



Der Text kann am führenden oder nachfolgenden Rand des layoutfelds ausgerichtet werden, oder er kann zentriert werden. Die folgende Abbildung zeigt Text, bei dem die Ausrichtung auf [**dwrite \_ Text \_ Alignment, \_ Leading**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**dwrite \_ Text \_ Alignment \_ Center**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)und [**dwrite \_ Text \_ Alignment \_ Trailing**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)festgelegt ist.

![Abbildung von Text Absätzen mit führenden, zentrierten und nachfolgenden ausrichtungszeichen](images/textalignment.png)

> [!Note]  
> Die Ausrichtung hängt von der Leserichtung ab, das obige ist für Leserichtung von links nach rechts vorgesehen. Die Leserichtung von rechts nach Links wäre das Gegenteil.

 

Ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt verwendet die Ausrichtung, die für das von Ihnen bei der Erstellung des Layouts angegebene [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) festgelegt wurde. Verwenden Sie [**idschreitetextlayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment), um die Textausrichtung zu ändern.

 

 
