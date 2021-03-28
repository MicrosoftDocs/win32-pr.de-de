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
# <a name="setting-the-text-alignment"></a>Festlegen der Text Ausrichtung

Die Textausrichtung für einen Gerätekontext kann mithilfe der Funktionen [**gettextalign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) und [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) abgefragt und festgelegt werden. Die Text Ausrichtungs Einstellungen legen fest, wie Text relativ zu einer angegebenen Position positioniert wird. Text kann am rechten oder linken Rand der Position ausgerichtet oder zentriert werden. Sie kann auch oberhalb oder unterhalb des Punkts ausgerichtet werden.

Das folgende Beispiel zeigt eine Methode, mit der bestimmt wird, welches Flag für die horizontale Ausrichtung festgelegt ist:


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



Sie können auch die [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) -Funktion verwenden, um die aktuelle Position zu aktualisieren, wenn eine Textausgabe Funktion aufgerufen wird. Im folgenden Beispiel wird z. b. die [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) -Funktion verwendet, um die aktuelle Position zu aktualisieren, wenn die [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion aufgerufen wird. In diesem Beispiel ist der *carial* -Parameter eine ganze Zahl, die die Anzahl der Arial-Schriftarten angibt.


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
> Sie sollten [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) nicht mit TA \_ updatecp verwenden, wenn Sie [**scriptstringout**](/windows/win32/api/usp10/nf-usp10-scriptstringout)verwenden, da ausgewählter Text nicht ordnungsgemäß gerendert wird. Wenn Sie dieses Flag verwenden müssen, können Sie es bei Bedarf zurücksetzen und zurücksetzen, um das Problem zu vermeiden.

 

 

 
