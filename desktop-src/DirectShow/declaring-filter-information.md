---
description: Deklarieren von Filter Informationen
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Deklarieren von Filter Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747409"
---
# <a name="declaring-filter-information"></a>Deklarieren von Filter Informationen

Der erste Schritt besteht darin, die Filter Informationen bei Bedarf zu deklarieren. DirectShow definiert die folgenden Strukturen zum Beschreiben von Filtern, Pins und Medientypen:



| Struktur                                               | BESCHREIBUNG             |
|---------------------------------------------------------|-------------------------|
| [**amoviesetup- \_ Filter**](amoviesetup-filter.md)       | Beschreibt einen Filter.     |
| [**amoviesetup- \_ PIN**](amoviesetup-pin.md)             | Beschreibt eine PIN.        |
| [**amoviesetup- \_ mediaType**](amoviesetup-mediatype.md) | Beschreibt einen Medientyp. |



 

Diese Strukturen sind eingebettet. Die **amoveiesetup- \_ Filter** Struktur verfügt über einen Zeiger auf ein Array von **amoviesetup- \_ Pin** -Strukturen, die jeweils über einen Zeiger auf ein Array von **amoveiesetup \_ mediaType** -Strukturen verfügen. Zusammenstellen diese Strukturen ausreichend Informationen für die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle bereit, um einen Filter zu suchen. Dabei handelt es sich nicht um eine komplette Beschreibung eines Filters. Wenn der Filter beispielsweise mehrere Instanzen derselben Pin erstellt, sollten Sie nur eine [**amoviesetup- \_ Pin**](amoviesetup-pin.md) -Struktur für diese Pin deklarieren. Außerdem ist kein Filter erforderlich, um jede Kombination von Medientypen zu unterstützen, die registriert werden. Es ist auch nicht erforderlich, jeden Medientyp zu registrieren, den er unterstützt.

Deklarieren Sie die Setup Strukturen als globale Variablen in der dll. Das folgende Beispiel zeigt einen Filter mit einer Ausgabe-PIN:


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



Der Filter Name wird als statische globale Variable deklariert, da er an anderer Stelle wieder verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



