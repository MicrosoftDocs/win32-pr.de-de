---
description: Im konventionell kann der Benutzer die Position der Einfügemarke (CP) auswählen, indem er entweder auf die nachfolgende Hälfte des Zeichens &\# 0034; CP-1&\# 0034; oder die führende Hälfte des Zeichens &\# 0034; CP&\# 0034; klickt.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Übersetzen des X-Offsets in der Einfügemarke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865484"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Übersetzen des X-Offsets in der Einfügemarke

Im konventionalbereich kann der Benutzer die Position der Einfügemarke (CP) auswählen, indem er entweder auf die nachfolgende Hälfte des Zeichens "CP-1" oder die führende Hälfte des Zeichens "CP" klickt. Eine Anwendung kann die Übersetzung von mousehit x Offset in die Position der Einfügemarke wie folgt implementieren:


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Bei Skripts, die die Einfügemarke zu Cluster Grenzen ausrichten, gibt ein [**scriptxchandecp-Skript**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) zurück, wobei *ftrailing* entweder auf 0 oder die Breite des Clusters in Code Punkten festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



