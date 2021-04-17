---
title: Erstellen der Haupt Animations Objekte
description: Um die Windows-Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, eine kleine Gruppe von Haupt Animations Objekten zu erstellen.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Animation-Manager-Objekte Windows-Animation, erstellen
- Animation Zeit Geber Objekte Windows-Animation, erstellen
- Übergangs Bibliotheksobjekte Windows-Animation, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390787"
---
# <a name="create-the-main-animation-objects"></a>Erstellen der Haupt Animations Objekte

Um die Windows-Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, eine kleine Gruppe von Haupt Animations Objekten zu erstellen.

## <a name="overview"></a>Übersicht

Verwenden Sie die [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um den Animations-Manager, den Animations Timer und die Übergangs Bibliotheksobjekte zu erstellen.

Diese Objekte werden zum Erstellen und Anzeigen von Animationen benötigt, sodass Sie normalerweise erst freigegeben werden, wenn die Anwendung heruntergefahren wird. Wenn keine Möglichkeit besteht, dass registrierte Rückrufe einen Verweis Durchlauf erstellt haben, reicht das Freigeben der Objekte für eine ordnungsgemäße Bereinigung aus. Andernfalls kann die Anwendung bereinigt werden, indem die Rückrufe (an der Stelle von **null** ) oder durch Aufrufen der [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) -Methode des Animations-Managers gelöscht werden.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen. Weitere Informationen finden Sie unter der CMainWindow:: initializeanimation-Methode.


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



Beachten Sie die folgenden Definitionen von "MainWindow. h".


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

Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Erstellen von Animations Variablen](create-animation-variables.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**Iuianimationmanager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**Iuianimationtimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**Iuianimationtransitionlibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Übersicht über Windows-Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 