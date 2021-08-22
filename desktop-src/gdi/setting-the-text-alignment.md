---
description: Sie können die Textausrichtung für einen Gerätekontext abfragen und festlegen, indem Sie die Funktionen GetTextAlign und SetTextAlign verwenden.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Festlegen der Textausrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78edffa9febaee0fd624cc97c4a908da349ad65526799e1c4bd3450137b62a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468420"
---
# <a name="setting-the-text-alignment"></a>Festlegen der Textausrichtung

Sie können die Textausrichtung für einen Gerätekontext abfragen und festlegen, indem Sie die [**Funktionen GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) und [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) verwenden. Die Textausrichtungseinstellungen bestimmen, wie Text relativ zu einer angegebenen Position positioniert wird. Text kann rechts oder links von der Position ausgerichtet oder um ihn zentriert werden. sie kann auch oberhalb oder unterhalb des Punkts ausgerichtet werden.

Das folgende Beispiel zeigt eine Methode zum Bestimmen, welches Flag für die horizontale Ausrichtung festgelegt ist:


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



Sie können auch die [**SetTextAlign-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) verwenden, um die aktuelle Position zu aktualisieren, wenn eine Textausgabefunktion aufgerufen wird. Im folgenden Beispiel wird beispielsweise die [**SetTextAlign-Funktion**](/windows/win32/api/wingdi/nf-wingdi-settextalign) verwendet, um die aktuelle Position zu aktualisieren, wenn die [**TextOut-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) aufgerufen wird. In diesem Beispiel ist der *cArial-Parameter* eine ganze Zahl, die die Anzahl der Arial-Schriftarten angibt.


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
> Sie sollten [**SetTextAlign nicht mit**](/windows/win32/api/wingdi/nf-wingdi-settextalign) TA UPDATECP verwenden, wenn \_ Sie [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout)verwenden, da ausgewählter Text nicht ordnungsgemäß gerendert wird. Wenn Sie dieses Flag verwenden müssen, können Sie es nach Bedarf zurücksetzen, um das Problem zu vermeiden.

 

 

 
