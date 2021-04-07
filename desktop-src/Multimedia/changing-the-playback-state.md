---
title: Ändern des Wiedergabe Zustands
description: Ändern des Wiedergabe Zustands
ms.assetid: 69ede616-aea4-4b7c-a12b-014ac0485b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9401c79e6bb89f4f21c5e3c220b48dc99a2b6109
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727328"
---
# <a name="changing-the-playback-state"></a>Ändern des Wiedergabe Zustands

In den folgenden Beispielen wird gezeigt, wie die Befehle anhalten, fort [**setzen,**](resume.md) [**Anhalten**](stop.md)und [**Suchen**](seek.md) in der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion [**verwendet werden.**](pause.md)


```C++
// Assume the file was opened with the alias 'movie'. 
 
// Pause play. 
mciSendString("pause movie", NULL, 0, NULL); 
 
// Resume play. 
mciSendString("resume movie", NULL, 0, NULL); 
 
// Stop play. 
mciSendString("stop movie", NULL, 0, NULL); 
 
// Seek to the beginning. 
mciSendString("seek movie to start", NULL, 0, NULL); 
 
```



Im folgenden Beispiel wird gezeigt, wie der Suchmodus geändert wird:


```C++
// Set seek mode with the string interface. 
// Assume the file was opened with the alias 'movie'. 
 
void SetSeekMode(BOOL fExact) 
{ 
    if (fExact) 
        mciSendString("set movie seek exactly on", NULL, 0, NULL); 
    else 
        mciSendString("set movie seek exactly off", NULL, 0, NULL); 
} 
```



 

 