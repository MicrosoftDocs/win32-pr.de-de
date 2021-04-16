---
title: Beispiel für Manipulation und Trägheit
description: Das Beispiel für Manipulation und Trägheit zeigt, wie systemeigenen Windows-basierten Anwendungen, die die Windows-Eingabe-API verwenden, Windows-Berührungs Unterstützung hinzugefügt wird.
ms.assetid: 6a6e2e39-026e-47a3-b936-16f6a740a3af
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows-Fingereingabe, Manipulationen
- Windows-Fingereingabe, Trägheit
- Beispiel für Windows-Fingereingabe, Manipulation und Trägheit
- Beispiel für Manipulation und Trägheit
- Windows-Touchscreen, _IManipulationEventSink-Schnittstelle
- Windows-Berührungs-, IManipulationProcessor-Schnittstelle
- Windows-Berührungs-, IInertiaProcessor-Schnittstelle
- Manipulationen, Beispielcode
- Manipulationen, Codebeispiele
- Manipulationen, _IManipulationEventSink-Schnittstelle
- Manipulationen, IManipulationProcessor-Schnittstelle
- Trägheit, Beispielcode
- Trägheit, Codebeispiele
- Trägheit, IInertiaProcessor-Schnittstelle
- _IManipulationEventSink-Schnittstelle
- IManipulationProcessor-Schnittstelle, Codebeispiele
- IManipulationProcessor-Schnittstelle, Beispielcode
- IInertiaProcessor-Schnittstelle, Codebeispiele
- IInertiaProcessor-Schnittstelle, Beispielcode
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: a17b634fbe79d72e79fc5c9e03ef64a30cb46411
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551320"
---
# <a name="manipulation-and-inertia-sample"></a>Beispiel für Manipulation und Trägheit

Das Beispiel für Manipulation und Trägheit zeigt, wie systemeigenen Windows-basierten Anwendungen, die die Windows-Eingabe-API verwenden, Windows-Berührungs Unterstützung hinzugefügt wird. Das Beispiel implementiert die grundlegenden Funktionen der API, um die Übersetzung, Drehung und Skalierung von Objekten und das Anwenden von Trägheit-Eigenschaften zu ermöglichen. Das Beispiel zeigt auch, wie Sie Ihren Windows-Berührungs Anwendungen grundlegende Mausunterstützung zur Verfügung gestellt werden. In der folgenden Abbildung wird gezeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot, der zwei Felder mit Farbverläufen im Beispiel für Manipulation und Trägheit anzeigt](images/manip-inertia-sample.png)

Die Felder mit Farbverläufen können unabhängig von einem Benutzer bearbeitet werden, wenn Sie die Anwendung von einem Computer ausführen, der Windows-Fingereingabe unterstützt.

## <a name="register-the-touch-window"></a>Registrieren des Finger eingabefensters

Bevor Sie Finger Eingaben erhalten können, müssen Sie das System zuerst Benachrichtigen, dass es sich bei Ihrer Anwendung um eine Windows-Berührungs Anwendung handelt, indem Sie die folgende Funktion aufrufen:

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a>Implementieren der _IManipulationEventSink-Schnittstelle

Die [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Ereignis Senke enthält drei Funktionen: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)und [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted). Diese Rückruf Funktionen werden von der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle und der [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle verwendet, um die Werte zurückzugeben, die von den Prozessoren berechnet werden, nachdem Sie die Funktionen [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**processupwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**processdownwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)und [**processmuvewithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) aufgerufen haben. Das folgende Codebeispiel zeigt eine Beispiel Implementierung einer **_IManipulationEvents** -Schnittstelle.

```C++
#include "cmanipulationeventsink.h"
#include <math.h>

CManipulationEventSink::CManipulationEventSink(HWND hWnd, CDrawingObject *dObj, int iTimerId, BOOL inertia) {
    // Manipulation & Inertia Processors
    m_manip = NULL;
    m_inert = NULL;

    // Connection points for COM.
    m_pConPointContainer = NULL;
    m_pConnPoint = NULL;

    // Reference to an object associated with this event sink.
    m_dObj = dObj;

    // Handle to the window used for computing boundaries.
    m_hWnd = hWnd;

    // The unique timer id for this manipulation event sink.
    m_iTimerId = iTimerId;

    m_bInertia = inertia;

    m_cRefCount = 1;
}


CManipulationEventSink::~CManipulationEventSink()
{

}


HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted(
    FLOAT x,
    FLOAT y)
{
    KillTimer(m_hWnd, m_iTimerId);

    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    FLOAT x,
    FLOAT y,
    FLOAT translationDeltaX,
    FLOAT translationDeltaY,
    FLOAT scaleDelta,
    FLOAT expansionDelta,
    FLOAT rotationDelta,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    FLOAT pivot = 0.0f;

    // Apply transformation based on rotationDelta (in radians).
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta.
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta.
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    if(!m_bInertia)
    {
        // Set values for one-finger rotations.
        FLOAT fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->GetWidth()/2, 2)
                           + pow(m_dObj->GetHeight()/2, 2)))*0.4f;
        FLOAT fPivotPtX    = m_dObj->GetCenterX();
        FLOAT fPivotPtY    = m_dObj->GetCenterY();

        m_manip->put_PivotPointX(fPivotPtX);
        m_manip->put_PivotPointY(fPivotPtY);
        m_manip->put_PivotRadius(fPivotRadius);
    }
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted(
    FLOAT x,
    FLOAT y,
    FLOAT cumulativeTranslationX,
    FLOAT cumulativeTranslationY,
    FLOAT cumulativeScale,
    FLOAT cumulativeExpansion,
    FLOAT cumulativeRotation)
{
    if(!m_bInertia)
    {
        SetupInertia();

        // Kick off timer that handles inertia.
        SetTimer(m_hWnd, m_iTimerId, DESIRED_MILLISECONDS, NULL);
    }
    else
    {
        // Stop timer that handles inertia.
        KillTimer(m_hWnd, m_iTimerId);
    }

    return S_OK;
}
```

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a>Erstellen von COM-Objekten und Einrichten der Schnittstellen IManipulationProcessor und IInertiaProcessor

Die API stellt eine Implementierung der Schnittstellen [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) und [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) bereit. Erstellen Sie eine Instanz von, und verweisen Sie auf die COM-Objekte aus der zuvor implementierten [**imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Ereignis Senke.

## <a name="handle-wm_touch-messages"></a>Behandeln von WM_TOUCH Meldungen

Die Eingabedaten müssen aus den [**WM_TOUCH**](wm-touchdown.md) Nachrichten extrahiert werden, und später muss Sie verarbeitet werden, um den richtigen Bearbeitungs Prozessor zu übermitteln.

```C++
switch (msg)
{
    case WM_TOUCH:

      iNumContacts = LOWORD(wParam);
      hInput       = (HTOUCHINPUT)lParam;
      pInputs      = new TOUCHINPUT[iNumContacts];

      // Get each touch input info and feed each
      // tagTOUCHINPUT into the process input handler.

      if(pInputs != NULL)
      {
          if(GetTouchInputInfo(hInput, iNumContacts,
               pInputs, sizeof(TOUCHINPUT)))
          {
              for(int i = 0; i < iNumContacts; i++)
              {
                  // Bring touch input info into client coordinates.
                  ptInputs.x = pInputs[i].x/100;
                  ptInputs.y = pInputs[i].y/100;
                  ScreenToClient(g_hWnd, &ptInputs);

                  pInputs[i].x = ptInputs.x;
                  pInputs[i].y = ptInputs.y;

                  g_ctDriver->ProcessInputEvent(pInputs[i]);
              }
          }
      }

      delete [] pInputs;
      break;
}
```

> [!Note]  
> Um die [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) -Funktion verwenden zu können, müssen Sie in Ihrer Anwendung über eine hohe dpi-Unterstützung verfügen. Weitere Informationen zur Unterstützung von High dpi finden Sie im Abschnitt " [High dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) " in MSDN.

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a>Übergeben von TOUCHINPUT-Strukturen an den entsprechenden Prozessor

Nachdem die Daten mithilfe der [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) -Funktion aus den [**WM_TOUCH**](wm-touchdown.md) Nachrichten extrahiert wurden, können Sie die Daten in den Manipulations Prozessor übertragen, indem Sie die Funktionen [**processupwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**processdownwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)oder [**processfuvewithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) aufrufen, je nachdem, welches **dwFlag** in der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur festgelegt ist.

> [!Note]  
> Bei der Unterstützung mehrerer Manipulationen muss ein neuer Manipulations Prozessor erstellt werden, wenn das in der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur definierte **dwID** zum Senden der Daten an das korrekte [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Objekt verwendet werden muss.

```C++
CoreObject* coCurrent = m_coHead;

while(coCurrent!=NULL && !bFoundObj)
{
    if(dwEvent & TOUCHEVENTF_DOWN)
    {
        DownEvent(coCurrent, inData, &bFoundObj);
    }
    else if(dwEvent & TOUCHEVENTF_MOVE)
    {
        MoveEvent(coCurrent, inData);
    }
    else if(dwEvent & TOUCHEVENTF_UP)
    {
        UpEvent(coCurrent, inData);
    }
    coCurrent = coCurrent->coNext;
}

VOID CComTouchDriver::DownEvent(CoreObject* coRef, tagTOUCHINPUT inData, BOOL* bFound) {
    DWORD dwPCursor = inData.dwID;
    DWORD dwPTime   = inData.dwTime;
    int x           = inData.x;
    int y           = inData.y;

    // Check that the user has touched within an object's region and fed to the object's manipulation processor.

    if(coRef->doDrawing->InRegion(x, y) &&
        !HasCursor(coRef, dwPCursor))
    {
        ...

        // Feed values to the Manipulation Processor.
        coRef->manipulationProc->ProcessDownWithTime(dwPCursor, (FLOAT)x, (FLOAT)y, dwPTime);

        ...
    }
}
```

## <a name="set-up-inertia-within-manipulationcompleted"></a>Einrichten der Trägheit innerhalb von "manipulationabgeschlossene"

Nachdem die [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) -Methode aufgerufen wurde, muss das [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Objekt die Werte für das [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Objekt, das mit **IManipulationProcessor** verknüpft ist, zum Aufrufen von Trägheit festlegen. Im folgenden Codebeispiel wird gezeigt, wie das **IInertiaProcessor** -Objekt aus der **IManipulationProcessor** -Methode " **manipulationabgeschlossene**" eingerichtet wird.

```C++
    int iVWidth       = GetSystemMetrics(SM_CXVIRTUALSCREEN);
    int iVHeight      = GetSystemMetrics(SM_CYVIRTUALSCREEN);

    RECT rc;
    GetClientRect(m_hWnd, &rc);
    FLOAT lCWidth     = (FLOAT)rc.right;
    FLOAT lCHeight    = (FLOAT)rc.bottom;

    // Set properties for inertia events.

    // Deceleration for tranlations in pixel / msec^2.
    m_inert->put_DesiredDeceleration(0.001f);

    // Deceleration for rotations in radians / msec^2.
    m_inert->put_DesiredAngularDeceleration(0.00001f);

    // Calculate borders and elastic margin to be set.
    // They are relative to the width and height of the object.

    FLOAT fHOffset = m_dObj->GetWidth()  * 0.5f;
    FLOAT fVOffset = m_dObj->GetHeight() * 0.5f;

    // Elastic margin is in pixels - note that it offsets the boundary.

    FLOAT fHElasticMargin = 25.0f;
    FLOAT fVElasticMargin = 25.0f;

    FLOAT fBoundaryLeft   = fHOffset + fHElasticMargin;
    FLOAT fBoundaryTop    = fVOffset + fVElasticMargin;
    FLOAT fBoundaryRight  = lCWidth - fHOffset - fHElasticMargin;
    FLOAT fBoundaryBottom = lCHeight - fVOffset - fVElasticMargin;

    // Set borders and elastic margin.

    m_inert->put_BoundaryLeft(fBoundaryLeft);
    m_inert->put_BoundaryTop(fBoundaryTop);
    m_inert->put_BoundaryRight(fBoundaryRight);
    m_inert->put_BoundaryBottom(fBoundaryBottom);

    m_inert->put_ElasticMarginLeft(fHElasticMargin);
    m_inert->put_ElasticMarginTop(fVElasticMargin);
    m_inert->put_ElasticMarginRight(fHElasticMargin);
    m_inert->put_ElasticMarginBottom(fVElasticMargin);

    // Set initial origins.

    m_inert->put_InitialOriginX(m_dObj->GetCenterX());
    m_inert->put_InitialOriginY(m_dObj->GetCenterY());

    FLOAT fVX;
    FLOAT fVY;
    FLOAT fVR;

    m_manip->GetVelocityX(&fVX);
    m_manip->GetVelocityY(&fVY);
    m_manip->GetAngularVelocity(&fVR);

    // Set initial velocities for inertia processor.

    m_inert->put_InitialVelocityX(fVX);
    m_inert->put_InitialVelocityY(fVY);
    m_inert->put_InitialAngularVelocity(fVR);
```

## <a name="clean-up-your-com-objects"></a>Bereinigen der COM-Objekte

Wenn die Anwendung geschlossen wird, müssen Sie die COM-Objekte bereinigen. Der folgende Code zeigt, wie Sie die Ressourcen freigeben können, die im Beispiel zugeordnet wurden.

```C++
CComTouchDriver::~CComTouchDriver(VOID) {
    CoreObject* coCurrent = m_coHead;

    // Clean up COM objects.

    while(coCurrent!=NULL)
    {
        coCurrent->inertiaEventSink->Release();
        coCurrent->manipulationEventSink->Release();
        coCurrent->inertiaProc->Release();
        coCurrent->manipulationProc->Release();
        coCurrent = coCurrent->coNext;
    }
}
```

## <a name="related-topics"></a>Zugehörige Themen

Beispiel für [Multitouch-Bearbeitungs Anwendung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation und Trägheit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)