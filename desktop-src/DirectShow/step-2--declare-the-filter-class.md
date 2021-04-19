---
description: 'Schritt 2:'
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Schritt 2: Deklarieren der Filter Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369734"
---
# <a name="step-2-declare-the-filter-class"></a>Schritt 2: Deklarieren der Filter Klasse

Dies ist Schritt 2 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).

Deklarieren Sie zunächst eine C++-Klasse, die die Basisklasse erbt:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Jeder der Filterklassen sind PIN-Klassen zugeordnet. Abhängig von den spezifischen Anforderungen Ihres Filters müssen Sie möglicherweise die PIN-Klassen überschreiben. Im Fall von **ctransformfilter** delegieren die Pins den größten Teil ihrer Arbeit an den Filter, sodass Sie die Pins wahrscheinlich nicht außer Kraft setzen müssen.

Sie müssen eine eindeutige CLSID für den Filter generieren. Sie können das Hilfsprogramm GUIDGEN oder uuidgen verwenden. Kopieren Sie niemals eine vorhandene GUID. Es gibt mehrere Möglichkeiten, eine CLSID zu deklarieren. Im folgenden Beispiel wird das **\_ GUID** -Makro definieren verwendet:


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Schreiben Sie als nächstes eine Konstruktormethode für den Filter:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Beachten Sie, dass einer der Parameter für den [**ctransformfilter**](ctransformfilter-ctransformfilter.md) -Konstruktor die zuvor definierte CLSID ist.

Weiter: [Schritt 3. Unterstützung der Medientyp Aushandlung](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



