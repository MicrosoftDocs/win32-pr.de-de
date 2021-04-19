---
description: Schritt 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Schritt 10. COM-Registrierung unterstützen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364046"
---
# <a name="step-10-support-com-registration"></a>Schritt 10. COM-Registrierung unterstützen

Die letzte verbleibende Aufgabe besteht in der Unterstützung der com-Registrierung, sodass der Eigenschaften Frame neue Instanzen der Eigenschaften Seite erstellen kann. Fügen Sie dem Global *g \_ Templates* -Array einen weiteren [**cfactor ytemplate**](cfactorytemplate.md) -Eintrag hinzu, der zum Registrieren aller COM-Objekte in der dll verwendet wird. Fügen Sie keine Filter Informationen für die Eigenschaften Seite ein.


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



Wenn Sie *g \_ ctemplates* deklarieren, wie im folgenden Code gezeigt, verfügt er automatisch über den richtigen Wert, basierend auf der Array Größe:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Fügen Sie `CreateInstance` der Eigenschaften Seiten Klasse außerdem eine statische Methode hinzu. Sie können der Methode einen beliebigen Namen geben, aber die Signatur muss mit der Signatur identisch sein, die im folgenden Beispiel gezeigt wird:


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



Um die Eigenschaften Seite zu testen, registrieren Sie die dll, und laden Sie dann den Filter in GraphEdit. Klicken Sie mit der rechten Maustaste auf den Filter, und wählen Sie **Filtereigenschaften**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> <dt>

[Erstellen einer DirectShow-Filter-dll](how-to-create-a-dll.md)
</dt> </dl>

 

 



