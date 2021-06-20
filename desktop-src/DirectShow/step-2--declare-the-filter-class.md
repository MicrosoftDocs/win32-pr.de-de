---
description: Deklarieren Sie eine C++-Klasse, die die Basisklasse erbt, die Sie beim Schreiben eines Transformationsfilters ausgewählt haben.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 'Schritt 2: Deklarieren der Filter-Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410063"
---
# <a name="step-2-declare-the-filter-class"></a>Schritt 2: Deklarieren der Filter-Klasse

Dies ist Schritt 2 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

Deklarieren Sie zunächst eine C++-Klasse, die die Basisklasse erbt:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Jeder Filterklasse sind Pinklassen zugeordnet. Je nach den spezifischen Anforderungen Ihres Filters müssen Sie möglicherweise die Pin-Klassen überschreiben. Im Fall von **CTransformFilter** delegieren die Pins den Großteil ihrer Arbeit an den Filter, sodass Sie die Stecknadeln wahrscheinlich nicht überschreiben müssen.

Sie müssen eine eindeutige CLSID für den Filter generieren. Sie können das Hilfsprogramm Guidgen oder Uuidgen verwenden. Kopieren Sie niemals eine vorhandene GUID. Es gibt mehrere Möglichkeiten, eine CLSID zu deklarieren. Im folgenden Beispiel wird das **DEFINE \_ GUID-Makro** verwendet:


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Schreiben Sie als Nächstes eine Konstruktormethode für den Filter:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Beachten Sie, dass einer der Parameter für den [**CTransformFilter-Konstruktor**](ctransformfilter-ctransformfilter.md) die zuvor definierte CLSID ist.

Weiter: [Schritt 3. Unterstützung der Medientypaushandlung](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



