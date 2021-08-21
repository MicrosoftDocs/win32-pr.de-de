---
description: Schritt 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Schritt 10. Unterstützung der COM-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68efdeda754d5f7b728138a26a6bc9f4b782918f8c4b5140fd2457bcee6012f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652150"
---
# <a name="step-10-support-com-registration"></a>Schritt 10. Unterstützung der COM-Registrierung

Die letzte verbleibende Aufgabe besteht darin, die COM-Registrierung zu unterstützen, damit der Eigenschaftenrahmen neue Instanzen Ihrer Eigenschaftenseite erstellen kann. Fügen Sie dem globalen *g \_ Templates-Array* einen weiteren [**CFactoryTemplate-Eintrag**](cfactorytemplate.md) hinzu, der zum Registrieren aller COM-Objekte in ihrer DLL verwendet wird. Fügen Sie keine Filtersatzinformationen für die Eigenschaftenseite ein.


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



Wenn Sie *g \_ cTemplates* wie im folgenden Code gezeigt deklarieren, verfügt es automatisch über den richtigen Wert basierend auf der Arraygröße:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Fügen Sie außerdem der Eigenschaftenseitenklasse eine statische `CreateInstance` Methode hinzu. Sie können die Methode nach Belieben benennen, aber die Signatur muss mit der signatur übereinstimmen, die im folgenden Beispiel gezeigt wird:


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



Registrieren Sie zum Testen der Eigenschaftenseite die DLL, und laden Sie dann den Filter in GraphEdit. Klicken Sie mit der rechten Maustaste auf den Filter, und wählen Sie **Filtereigenschaften** aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> <dt>

[Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 



