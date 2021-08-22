---
description: Machen Sie die neuen Schnittstellen eines Filters für Clients verfügbar, wenn Sie eine Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter erstellen.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 'Schritt 3: Unterstützung von QueryInterface'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0761a0ecf57bc7769cf40623c6929655a9f757b66b35bb506167d4263a7e02a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072454"
---
# <a name="step-3-support-queryinterface"></a>Schritt 3: Unterstützung von QueryInterface

Gehen Sie wie folgt vor, um die neuen Schnittstellen des Filters für Clients verfügbar zu machen:

-   Schließen Sie das [**DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) in den Öffentlichen Deklarationsabschnitt Ihres Filters ein:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Überschreiben Sie [**CUnknown::NonDelegatingQueryInterface,**](cunknown-nondelegatingqueryinterface.md) um nach den IIDs der beiden Schnittstellen zu suchen:
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

    

Weiter: [Schritt 4. Erstellen Sie die Eigenschaftenseite](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Filtereigenschaftenseite](creating-a-filter-property-page.md)
</dt> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



