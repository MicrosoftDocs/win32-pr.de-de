---
title: Öffnen mehrerer AVI-Dateien
description: Öffnen mehrerer AVI-Dateien
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- initavi-Funktion
- termavi-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339067"
---
# <a name="opening-multiple-avi-files"></a>Öffnen mehrerer AVI-Dateien

Wenn Ihre Anwendung mehrere Dateien öffnet, sollte Sie Routinen wie die folgenden einfachen Funktionen enthalten. Die Anwendung verwendet die Funktion "initavi" während der Initialisierung und die Funktion "termavi" während ihrer Beendigung. Diese Funktionen wrappen einfach die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion.


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 