---
title: Erstellen der Hauptanimationsobjekte
description: Um Windows Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, einen kleinen Satz von Hauptanimationsobjekten zu erstellen.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Animation Manager-Objekte Windows Animation , erstellen
- Animation timer objects Windows Animation , creating
- Übergangsbibliotheksobjekte Windows Animation , erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3023e5934581850bb6aa21e7d41d92642bb01fadfcf7531fcacabca74b411f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137403"
---
# <a name="create-the-main-animation-objects"></a>Erstellen der Hauptanimationsobjekte

Um Windows Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, einen kleinen Satz von Hauptanimationsobjekten zu erstellen.

## <a name="overview"></a>Übersicht

Verwenden Sie die [**CoCreateInstance-Funktion,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) um den Animations-Manager, den Animationstimer und die Übergangsbibliotheksobjekte zu erstellen.

Diese Objekte werden zum Erstellen und Anzeigen von Animationen benötigt, sodass sie in der Regel erst freigegeben werden sollten, wenn die Anwendung heruntergefahren wird. Wenn keine Möglichkeit besteht, dass registrierte Rückrufe einen Verweiszyklus erstellt haben könnten, ist die Freigabe der Objekte für eine ordnungsgemäße Bereinigung ausreichend. Andernfalls kann die Anwendung die Bereinigung durch Löschen der Rückrufe (Übergabe von **NULL** anstelle der einzelnen) oder durch Aufrufen der [**Shutdown-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) des Animations-Managers erreichen.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus MainWindow.cpp in den beispielen für Windows Animationen. siehe die CMainWindow::InitializeAnimation-Methode.


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



Beachten Sie die folgenden Definitionen aus MainWindow.h.


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a>Nächster Schritt

Nach Abschluss dieses Schritts ist der nächste Schritt: [Erstellen von Animationsvariablen](create-animation-variables.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows Übersicht über Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 