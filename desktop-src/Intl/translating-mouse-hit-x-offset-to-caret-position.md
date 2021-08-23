---
description: Herkömmlicher artiell kann der Benutzer die Caretposition (cp) auswählen, indem er entweder auf die nach unten gezeigte Hälfte des Zeichens &\# 0034;cp-1&0034; oder auf die führende Hälfte des Zeichens \# &\# 0034;cp&\# 0034; klickt.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Übersetzen des Maustreffer-X-Offsets in die Position des Caretzeichens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e135efaccb6454e55999d21f00e762d749eb380751848aef88cf4b4e5b8e913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693180"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Übersetzen des Maustreffer-X-Offsets in die Position des Caretzeichens

Im Herkömmlichen kann der Benutzer die Position des Caretzeichens (cp) auswählen, indem er entweder auf die hintere Hälfte des Zeichens "cp-1" oder die führende Hälfte des Zeichens "cp" klickt. Eine Anwendung kann die Übersetzung des Maustreffer-X-Offsets in die Position des Caretzeichens wie folgt implementieren:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Bei Skripts, die das Caret-Zeichen an Clustergrenzen ausrichten, wird ein Aufruf von [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) zurückgegeben, bei dem *fTrailing* entweder auf 0 oder die Breite des Clusters in Codepunkten festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



