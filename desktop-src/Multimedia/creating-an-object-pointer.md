---
title: Erstellen eines Objektzeigers
description: Erstellen eines Objektzeigers
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144683"
---
# <a name="creating-an-object-pointer"></a>Erstellen eines Objektzeigers

AVIBall verwendet die folgende -Struktur als Objektzeiger. Der erste Member dieser Struktur verweist auf die virtuelle Funktionstabelle, die AVIBall für den Zugriff auf seine Funktionen verwendet. Anwendungen können diese Struktur in den PAVISTREAM-Datentyp umstrukturieren. Methoden, die den PAVISTREAM-Datentyp verwenden, verwenden nur den Zeiger auf die virtuelle Funktionstabelle. Die Member, die dem Zeiger auf die virtuelle Funktionstabelle folgen, werden intern von AVIBall verwendet.


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



 

 




