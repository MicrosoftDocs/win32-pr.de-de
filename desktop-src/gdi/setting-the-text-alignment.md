---
description: Die Textausrichtung für einen Gerätekontext kann mithilfe der Funktionen gettextalign und setTextAlign abgefragt und festgelegt werden.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Festlegen der Text Ausrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979448"
---
# <a name="setting-the-text-alignment"></a><span data-ttu-id="cc6cf-103">Festlegen der Text Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="cc6cf-103">Setting the Text Alignment</span></span>

<span data-ttu-id="cc6cf-104">Die Textausrichtung für einen Gerätekontext kann mithilfe der Funktionen [**gettextalign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) und [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) abgefragt und festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="cc6cf-105">Die Text Ausrichtungs Einstellungen legen fest, wie Text relativ zu einer angegebenen Position positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="cc6cf-106">Text kann am rechten oder linken Rand der Position ausgerichtet oder zentriert werden. Sie kann auch oberhalb oder unterhalb des Punkts ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="cc6cf-107">Das folgende Beispiel zeigt eine Methode, mit der bestimmt wird, welches Flag für die horizontale Ausrichtung festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="cc6cf-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



<span data-ttu-id="cc6cf-108">Sie können auch die [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) -Funktion verwenden, um die aktuelle Position zu aktualisieren, wenn eine Textausgabe Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="cc6cf-109">Im folgenden Beispiel wird z. b. die [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) -Funktion verwendet, um die aktuelle Position zu aktualisieren, wenn die [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="cc6cf-110">In diesem Beispiel ist der *carial* -Parameter eine ganze Zahl, die die Anzahl der Arial-Schriftarten angibt.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> <span data-ttu-id="cc6cf-111">Sie sollten [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) nicht mit TA \_ updatecp verwenden, wenn Sie [**scriptstringout**](/windows/win32/api/usp10/nf-usp10-scriptstringout)verwenden, da ausgewählter Text nicht ordnungsgemäß gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="cc6cf-112">Wenn Sie dieses Flag verwenden müssen, können Sie es bei Bedarf zurücksetzen und zurücksetzen, um das Problem zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cc6cf-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 
