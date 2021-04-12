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
# <a name="creating-an-object-pointer"></a><span data-ttu-id="1cae0-103">Erstellen eines Objekt Zeigers</span><span class="sxs-lookup"><span data-stu-id="1cae0-103">Creating an Object Pointer</span></span>

<span data-ttu-id="1cae0-104">Aviball verwendet die folgende Struktur als Objekt Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1cae0-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="1cae0-105">Der erste Member dieser Struktur verweist auf die virtuelle Funktions Tabelle, die aviball verwendet, um auf seine Funktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1cae0-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="1cae0-106">Anwendungen können diese Struktur in den Datentyp "pvistream" umwandeln.</span><span class="sxs-lookup"><span data-stu-id="1cae0-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="1cae0-107">Bei Methoden, die den-Datentyp "pvistream" verwenden, wird nur der Zeiger auf die virtuelle Funktions Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cae0-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="1cae0-108">Die Elemente, die dem Zeiger auf die virtuelle Funktions Tabelle folgen, werden intern von aviball verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cae0-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


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



 

 




