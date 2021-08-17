---
description: Deklarieren von Filterinformationen
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Deklarieren von Filterinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953199"
---
# <a name="declaring-filter-information"></a>Deklarieren von Filterinformationen

Der erste Schritt besteht im Deklarieren der Filterinformationen, falls erforderlich. DirectShow definiert die folgenden Strukturen zum Beschreiben von Filtern, Pins und Medientypen:



| Struktur                                               | Beschreibung             |
|---------------------------------------------------------|-------------------------|
| [**AMOVIESETUP-FILTER \_**](amoviesetup-filter.md)       | Beschreibt einen Filter.     |
| [**AMOVIESETUP \_ PIN**](amoviesetup-pin.md)             | Beschreibt eine Stecknadel.        |
| [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) | Beschreibt einen Medientyp. |



 

Diese Strukturen sind geschachtelt. Die **AMOVEIESETUP \_ FILTER-Struktur** verfügt über einen Zeiger auf ein Array von **AMOVIESETUP-PIN-Strukturen, \_** und jede dieser Strukturen verfügt über einen Zeiger auf ein Array von **AMOVEIESETUP \_ MEDIATYPE-Strukturen.** Zusammen stellen diese Strukturen genügend Informationen bereit, damit die [**IFilterMapper2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) einen Filter finden kann. Sie sind keine vollständige Beschreibung eines Filters. Wenn der Filter beispielsweise mehrere Instanzen desselben Pins erstellt, sollten Sie nur eine [**AMOVIESETUP-PIN-Struktur \_**](amoviesetup-pin.md) für diesen Pin deklarieren. Außerdem ist kein Filter erforderlich, um jede Kombination von Medientypen zu unterstützen, die er registriert. und ist nicht erforderlich, um jeden unterstützten Medientyp zu registrieren.

Deklarieren Sie die Einrichtungsstrukturen als globale Variablen in Ihrer DLL. Das folgende Beispiel zeigt einen Filter mit einem Ausgabepin:


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



Der Filtername wird als statische globale Variable deklariert, da er an anderer Stelle erneut verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



