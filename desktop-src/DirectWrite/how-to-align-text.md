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
# <a name="how-to-align-text"></a><span data-ttu-id="b35d1-103">Ausrichten von Text</span><span class="sxs-lookup"><span data-stu-id="b35d1-103">How to Align Text</span></span>

<span data-ttu-id="b35d1-104">Sie können [DirectWrite](direct-write-portal.md) -Text mithilfe der [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) -Methode der [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle ausrichten, wie im folgenden Code gezeigt, in dem der Text zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="b35d1-104">You can align [DirectWrite](direct-write-portal.md) text by using the [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) method of the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface, as shown in the following code that centers the text.</span></span>


```C++
HRESULT hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

if (FAILED(hr))
{
    // Report the error
}
```



<span data-ttu-id="b35d1-105">Der Text kann am führenden oder nachfolgenden Rand des layoutfelds ausgerichtet werden, oder er kann zentriert werden.</span><span class="sxs-lookup"><span data-stu-id="b35d1-105">The text can be aligned to the leading or trailing edge of the layout box, or it can be centered.</span></span> <span data-ttu-id="b35d1-106">Die folgende Abbildung zeigt Text, bei dem die Ausrichtung auf [**dwrite \_ Text \_ Alignment, \_ Leading**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**dwrite \_ Text \_ Alignment \_ Center**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)und [**dwrite \_ Text \_ Alignment \_ Trailing**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b35d1-106">The following illustration shows text with the alignment set to [**DWRITE\_TEXT\_ALIGNMENT\_LEADING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), [**DWRITE\_TEXT\_ALIGNMENT\_CENTER**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), and [**DWRITE\_TEXT\_ALIGNMENT\_TRAILING**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment), respectively.</span></span>

![Abbildung von Text Absätzen mit führenden, zentrierten und nachfolgenden ausrichtungszeichen](images/textalignment.png)

> [!Note]  
> <span data-ttu-id="b35d1-108">Die Ausrichtung hängt von der Leserichtung ab, das obige ist für Leserichtung von links nach rechts vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b35d1-108">The alignment is dependent on reading direction, the above is for left-to-right reading direction.</span></span> <span data-ttu-id="b35d1-109">Die Leserichtung von rechts nach Links wäre das Gegenteil.</span><span class="sxs-lookup"><span data-stu-id="b35d1-109">For right-to-left reading direction it would be the opposite.</span></span>

 

<span data-ttu-id="b35d1-110">Ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt verwendet die Ausrichtung, die für das von Ihnen bei der Erstellung des Layouts angegebene [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b35d1-110">An [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object will use the alignment that has been designated for the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provided by you when creating the layout.</span></span> <span data-ttu-id="b35d1-111">Verwenden Sie [**idschreitetextlayout:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment), um die Textausrichtung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b35d1-111">To change the text alignment, use [**IDWriteTextLayout::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment).</span></span>

 

 
