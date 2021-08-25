---
title: Ändern des Wiedergabezustands
description: Ändern des Wiedergabezustands
ms.assetid: 69ede616-aea4-4b7c-a12b-014ac0485b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d168a482259277d30b2a8d1dc70481c02612a6d7e63ea85ad06fd5499cc0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808180"
---
# <a name="changing-the-playback-state"></a>Ändern des Wiedergabezustands

In den folgenden Beispielen wird gezeigt, wie sie die Befehle [**"pause",**](pause.md) [**"resume",**](resume.md) [**"stop"**](stop.md)und [**"seek"**](seek.md) in der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) verwenden.


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



Das folgende Beispiel zeigt, wie der Suchmodus geändert wird:


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



 

 