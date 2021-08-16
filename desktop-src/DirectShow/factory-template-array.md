---
description: Factoryvorlagenarray
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factoryvorlagenarray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1888a2a054473865c713d96cdfa5706c35229dc938f23513a95066176ab138c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401845"
---
# <a name="factory-template-array"></a>Factoryvorlagenarray

Die Factoryvorlage enthält die folgenden öffentlichen Membervariablen:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Die beiden Funktionszeiger [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) und [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)verwenden die folgenden Typdefinitionen:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

Der erste ist die Instanziierungsfunktion für die Komponente. Die zweite ist eine optionale Initialisierungsfunktion. Wenn Sie eine Initialisierungsfunktion bereitstellen, wird sie aus der DLL-Einstiegspunktfunktion aufgerufen. (Die DLL-Einstiegspunktfunktion wird weiter unten in diesem Artikel erläutert.)

Angenommen, Sie erstellen eine DLL, die eine Komponente namens CMyComponent enthält, die von [**CUnknown**](cunknown.md)erbt. Sie müssen die folgenden Elemente in ihrer DLL angeben:

-   Die Initialisierungsfunktion, eine öffentliche Methode, die eine neue Instanz von CMyComponent zurückgibt.
-   Ein globales Array von Factoryvorlagen mit dem Namen *g \_ Templates.* Dieses Array enthält die Factoryvorlage für CMyComponent.
-   Eine globale Variable mit dem Namen *g \_ cTemplates,* die die Größe des Arrays angibt.

Das folgende Beispiel zeigt, wie diese Elemente deklariert werden:


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



Die `CreateInstance` -Methode ruft den Klassenkonstruktor auf und gibt einen Zeiger auf die neue Klasseninstanz zurück. Der *Parameter pUnk* ist ein Zeiger auf die aggregierende [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Sie können diesen Parameter einfach an den Klassenkonstruktor übergeben. Der *Parameter pHr* ist ein Zeiger auf einen HRESULT-Wert. Der Klassenkonstruktor legt diesen auf einen entsprechenden Wert fest. Wenn der Konstruktor jedoch fehlschlägt, legen Sie den Wert auf E \_ OUTOFMEMORY fest.

Das [**NAME-Makro**](name.md) generiert eine Zeichenfolge in Debugbuilds, wird aber in Verkaufsbuilds in **NULL** aufgelöst. Sie wird in diesem Beispiel verwendet, um der Komponente einen Namen zu geben, der in Debugprotokollen angezeigt wird, aber in der endgültigen Version keinen Arbeitsspeicher belegt.

Die `CreateInstance` -Methode kann einen beliebigen Namen haben, da die Klassenfactory auf den Funktionszeiger in der Factoryvorlage verweist. g *\_ Templates* und *g \_ cTemplates* sind jedoch globale Variablen, die von der Klassenfactory erwartet werden, sodass sie genau diese Namen aufweisen müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
