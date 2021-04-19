---
description: 'Schritt 3:'
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 'Schritt 3: QueryInterface-Unterstützung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356998"
---
# <a name="step-3-support-queryinterface"></a>Schritt 3: QueryInterface-Unterstützung

Gehen Sie folgendermaßen vor, um die neuen Schnittstellen des Filters für Clients verfügbar zu machen:

-   Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt Public Declaration Ihres Filters ein:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Überschreiben Sie [**cunknown:: nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) , um die IIDs der beiden Schnittstellen zu überprüfen:
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

Weiter: [Schritt 4. Erstellen Sie die Eigenschaften Seite](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md)
</dt> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



