---
description: Deklarieren der Factory-Vorlage
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Deklarieren der Factory-Vorlage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123692"
---
# <a name="declaring-the-factory-template"></a>Deklarieren der Factory-Vorlage

Der nächste Schritt besteht darin, die Factory-Vorlage für den Filter zu deklarieren. Eine Factoryvorlage ist eine C++-Klasse, die Informationen für die Klassenfactory enthält. Deklarieren Sie in der dll ein globales Array von [**cfactoriytemplate**](cfactorytemplate.md) -Objekten, eines für jeden Filter oder jede COM-Komponente in der dll. Das Array muss als *g- \_ Vorlagen* benannt werden. Weitere Informationen zu Factory-Vorlagen finden [Sie unter Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).

Der **m \_ pamoviesetup- \_ Filter** Member der Factory-Vorlage ist ein Zeiger auf die zuvor beschriebene [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Struktur. Das folgende Beispiel zeigt eine Factory-Vorlage unter Verwendung der im vorherigen Beispiel angegebenen Struktur:


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Wenn Sie keine Filter Informationen deklariert haben, kann der " **m \_ pamovesetup \_** "-Filter **null** sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



