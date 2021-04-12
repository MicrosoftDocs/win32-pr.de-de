---
title: Erstellen eines Objekt Zeigers
description: Erstellen eines Objekt Zeigers
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206592"
---
# <a name="creating-an-object-pointer"></a>Erstellen eines Objekt Zeigers

Aviball verwendet die folgende Struktur als Objekt Zeiger. Der erste Member dieser Struktur verweist auf die virtuelle Funktions Tabelle, die aviball verwendet, um auf seine Funktionen zuzugreifen. Anwendungen können diese Struktur in den Datentyp "pvistream" umwandeln. Bei Methoden, die den-Datentyp "pvistream" verwenden, wird nur der Zeiger auf die virtuelle Funktions Tabelle verwendet. Die Elemente, die dem Zeiger auf die virtuelle Funktions Tabelle folgen, werden intern von aviball verwendet.


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 




