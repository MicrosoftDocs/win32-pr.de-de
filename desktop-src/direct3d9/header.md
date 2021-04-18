---
description: Die folgenden Definitionen sollten verwendet werden, wenn der binäre Header direkt gelesen und geschrieben wird.
ms.assetid: 19c36f94-8088-417d-867d-3a02912087dc
title: Header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfaa589382812cfd752d47cc8b95cda0139385b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343552"
---
# <a name="header"></a><span data-ttu-id="48ff7-103">Header</span><span class="sxs-lookup"><span data-stu-id="48ff7-103">Header</span></span>

<span data-ttu-id="48ff7-104">Die folgenden Definitionen sollten verwendet werden, wenn der binäre Header direkt gelesen und geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="48ff7-104">The following definitions should be used when directly reading and writing the binary header.</span></span>

> [!Note]  
> <span data-ttu-id="48ff7-105">Komprimierte Datenströme werden zurzeit nicht unterstützt und werden daher hier nicht ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="48ff7-105">Compressed data streams are not currently supported and are therefore not detailed here.</span></span>

 


```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```



## <a name="related-topics"></a><span data-ttu-id="48ff7-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48ff7-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48ff7-107">Binärcodierung</span><span class="sxs-lookup"><span data-stu-id="48ff7-107">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



