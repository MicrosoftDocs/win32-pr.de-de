---
description: Factory-Vorlagen Array
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factory-Vorlagen Array
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125599"
---
# <a name="factory-template-array"></a>Factory-Vorlagen Array

Die Factory-Vorlage enthält die folgenden öffentlichen Member-Variablen:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Die zwei Funktionszeiger " [**m \_ lpfnnew**](cfactorytemplate-m-lpfnnew.md) " und " [**m \_ lpfninit**](cfactorytemplate-m-lpfninit.md)" verwenden die folgenden Typdefinitionen:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

Der erste ist die Instanziierung-Funktion für die Komponente. Die zweite ist eine optionale Initialisierungsfunktion. Wenn Sie eine Initialisierungsfunktion bereitstellen, wird diese innerhalb der DLL-Einstiegspunkt Funktion aufgerufen. (Die DLL-Einstiegspunkt Funktion wird weiter unten in diesem Artikel erläutert.)

Angenommen, Sie erstellen eine DLL, die eine Komponente mit dem Namen cmycomponent enthält, die von [**cunknown**](cunknown.md)erbt. Sie müssen die folgenden Elemente in der DLL angeben:

-   Die Initialisierungsfunktion, eine öffentliche Methode, die eine neue Instanz von cmycomponent zurückgibt.
-   Ein globales Array von Factory-Vorlagen mit dem Namen *g- \_ Vorlagen.* Dieses Array enthält die Factory-Vorlage für cmycomponent.
-   Eine globale Variable mit dem Namen " *g \_ ctemplates* ", die die Größe des Arrays angibt.

Im folgenden Beispiel wird gezeigt, wie Sie diese Elemente deklarieren:


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



Die `CreateInstance` -Methode ruft den-Klassenkonstruktor auf und gibt einen Zeiger auf die neue Klasseninstanz zurück. Der Parameter- *Punk* ist ein Zeiger auf die aggregierte [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Sie können diesen Parameter einfach an den-Klassenkonstruktor übergeben. Der *PHR* -Parameter ist ein Zeiger auf einen HRESULT-Wert. Der Klassenkonstruktor legt diesen auf einen geeigneten Wert fest. wenn der Konstruktor jedoch fehlschlägt, legen Sie den Wert auf "E \_ outo fmemory" fest.

Das [**Name**](name.md) -Makro generiert eine Zeichenfolge in Debugbuilds, wird jedoch in Einzelhandels Builds in **null** aufgelöst. Sie wird in diesem Beispiel verwendet, um der Komponente einen Namen zu geben, der in Debugprotokollen enthalten ist, aber keinen Arbeitsspeicher in der endgültigen Version einnimmt.

Die- `CreateInstance` Methode kann einen beliebigen Namen haben, da die Klassenfactory auf den Funktionszeiger in der Factoryvorlage verweist. Allerdings sind *g- \_ Vorlagen* und *g \_ ctemplates* globale Variablen, die von der Klassenfactory erwartet werden, sodass Sie genau diese Namen aufweisen müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-dll](how-to-create-a-dll.md)
</dt> </dl>

 

 
