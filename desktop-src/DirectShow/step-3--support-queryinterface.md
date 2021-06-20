---
description: Machen Sie die neuen Schnittstellen eines Filters für Clients verfügbar, wenn Sie eine Filtereigenschaftsseite für einen benutzerdefinierten DirectShow-Filter erstellen.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 'Schritt 3: Unterstützung von QueryInterface'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410023"
---
# <a name="step-3-support-queryinterface"></a>Schritt 3: Unterstützung von QueryInterface

Gehen Sie wie folgt vor, um die neuen Schnittstellen des Filters für Clients verfügbar zu machen:

-   Schließen Sie [**das DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) in den öffentlichen Deklarationsabschnitt Ihres Filters ein:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Überschreiben [**Sie CUnknown::NonDelegatingQueryInterface,**](cunknown-nondelegatingqueryinterface.md) um nach den IIDs der beiden Schnittstellen zu überprüfen:
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

[Erstellen einer Filtereigenschaftsseite](creating-a-filter-property-page.md)
</dt> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



