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
# <a name="manipulation-and-inertia-sample"></a><span data-ttu-id="3e0fb-124">Beispiel für Manipulation und Trägheit</span><span class="sxs-lookup"><span data-stu-id="3e0fb-124">Manipulation and Inertia Sample</span></span>

<span data-ttu-id="3e0fb-125">Das Beispiel für Manipulation und Trägheit zeigt, wie systemeigenen Windows-basierten Anwendungen, die die Windows-Eingabe-API verwenden, Windows-Berührungs Unterstützung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-125">The Manipulation and Inertia sample shows how to add Windows Touch support to native Windows-based applications that use the Windows Touch API.</span></span> <span data-ttu-id="3e0fb-126">Das Beispiel implementiert die grundlegenden Funktionen der API, um die Übersetzung, Drehung und Skalierung von Objekten und das Anwenden von Trägheit-Eigenschaften zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-126">The sample implements the basic features of the API to enable translation, rotation, and scaling for objects and applying inertia properties to them.</span></span> <span data-ttu-id="3e0fb-127">Das Beispiel zeigt auch, wie Sie Ihren Windows-Berührungs Anwendungen grundlegende Mausunterstützung zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-127">The sample also shows how to give your Windows Touch applications basic mouse support.</span></span> <span data-ttu-id="3e0fb-128">In der folgenden Abbildung wird gezeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-128">The following image shows how the sample looks when it runs.</span></span>

![Screenshot, der zwei Felder mit Farbverläufen im Beispiel für Manipulation und Trägheit anzeigt](images/manip-inertia-sample.png)

<span data-ttu-id="3e0fb-130">Die Felder mit Farbverläufen können unabhängig von einem Benutzer bearbeitet werden, wenn Sie die Anwendung von einem Computer ausführen, der Windows-Fingereingabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-130">The boxes with gradients can be manipulated independently by a user when they run the application from a computer that supports Windows Touch.</span></span>

## <a name="register-the-touch-window"></a><span data-ttu-id="3e0fb-131">Registrieren des Finger eingabefensters</span><span class="sxs-lookup"><span data-stu-id="3e0fb-131">Register the Touch Window</span></span>

<span data-ttu-id="3e0fb-132">Bevor Sie Finger Eingaben erhalten können, müssen Sie das System zuerst Benachrichtigen, dass es sich bei Ihrer Anwendung um eine Windows-Berührungs Anwendung handelt, indem Sie die folgende Funktion aufrufen:</span><span class="sxs-lookup"><span data-stu-id="3e0fb-132">Before you can receive touch input, you first must notify the system that your application is a Windows Touch application by calling the following function:</span></span>

```C++
   RegisterTouchWindow(g_hWnd, 0);
```

## <a name="implement-the-_imanipulationeventsink-interface"></a><span data-ttu-id="3e0fb-133">Implementieren der _IManipulationEventSink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3e0fb-133">Implement the _IManipulationEventSink Interface</span></span>

<span data-ttu-id="3e0fb-134">Die [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Ereignis Senke enthält drei Funktionen: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)und [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span><span class="sxs-lookup"><span data-stu-id="3e0fb-134">The [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink contains three functions: [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted).</span></span> <span data-ttu-id="3e0fb-135">Diese Rückruf Funktionen werden von der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle und der [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle verwendet, um die Werte zurückzugeben, die von den Prozessoren berechnet werden, nachdem Sie die Funktionen [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**processupwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**processdownwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)und [**processmuvewithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-135">These callback functions are used by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for returning the values calculated by the processors after they invoke the [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime), [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), and [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions.</span></span> <span data-ttu-id="3e0fb-136">Das folgende Codebeispiel zeigt eine Beispiel Implementierung einer **_IManipulationEvents** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-136">The following code example shows an example implementation of a **_IManipulationEvents** interface.</span></span>

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

## <a name="create-com-objects-and-set-up-the-imanipulationprocessor-and-iinertiaprocessor-interfaces"></a><span data-ttu-id="3e0fb-137">Erstellen von COM-Objekten und Einrichten der Schnittstellen IManipulationProcessor und IInertiaProcessor</span><span class="sxs-lookup"><span data-stu-id="3e0fb-137">Create COM Objects and Set up the IManipulationProcessor and IInertiaProcessor Interfaces</span></span>

<span data-ttu-id="3e0fb-138">Die API stellt eine Implementierung der Schnittstellen [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) und [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) bereit.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-138">The API provides an implementation of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) and [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span> <span data-ttu-id="3e0fb-139">Erstellen Sie eine Instanz von, und verweisen Sie auf die COM-Objekte aus der zuvor implementierten [**imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Ereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-139">You should create an instance of and reference the COM objects from the [**IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) event sink that was implemented earlier.</span></span>

## <a name="handle-wm_touch-messages"></a><span data-ttu-id="3e0fb-140">Behandeln von WM_TOUCH Meldungen</span><span class="sxs-lookup"><span data-stu-id="3e0fb-140">Handle WM_TOUCH Messages</span></span>

<span data-ttu-id="3e0fb-141">Die Eingabedaten müssen aus den [**WM_TOUCH**](wm-touchdown.md) Nachrichten extrahiert werden, und später muss Sie verarbeitet werden, um den richtigen Bearbeitungs Prozessor zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-141">The input data must be extracted from the [**WM_TOUCH**](wm-touchdown.md) messages and then later must be processed to feed the correct manipulation processor.</span></span>

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
> <span data-ttu-id="3e0fb-142">Um die [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) -Funktion verwenden zu können, müssen Sie in Ihrer Anwendung über eine hohe dpi-Unterstützung verfügen.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-142">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="3e0fb-143">Weitere Informationen zur Unterstützung von High dpi finden Sie im Abschnitt " [High dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) " in MSDN.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-143">For more information about supporting high DPI, visit the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

## <a name="pass-touchinput-structures-to-the-appropriate-processor"></a><span data-ttu-id="3e0fb-144">Übergeben von TOUCHINPUT-Strukturen an den entsprechenden Prozessor</span><span class="sxs-lookup"><span data-stu-id="3e0fb-144">Pass TOUCHINPUT Structures to the Appropriate Processor</span></span>

<span data-ttu-id="3e0fb-145">Nachdem die Daten mithilfe der [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) -Funktion aus den [**WM_TOUCH**](wm-touchdown.md) Nachrichten extrahiert wurden, können Sie die Daten in den Manipulations Prozessor übertragen, indem Sie die Funktionen [**processupwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**processdownwithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)oder [**processfuvewithtime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) aufrufen, je nachdem, welches **dwFlag** in der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-145">After the data is extracted from the [**WM_TOUCH**](wm-touchdown.md) messages by using the [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) function, feed the data into the manipulation processor by invoking [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime), [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime), or [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime) functions, depending on the **dwFlag** set in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure.</span></span>

> [!Note]  
> <span data-ttu-id="3e0fb-146">Bei der Unterstützung mehrerer Manipulationen muss ein neuer Manipulations Prozessor erstellt werden, wenn das in der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur definierte **dwID** zum Senden der Daten an das korrekte [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Objekt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-146">When supporting multiple manipulations, a new manipulation processor must be created if the **dwID** defined in the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure must be used to send the data to the correct [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object.</span></span>

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

## <a name="set-up-inertia-within-manipulationcompleted"></a><span data-ttu-id="3e0fb-147">Einrichten der Trägheit innerhalb von "manipulationabgeschlossene"</span><span class="sxs-lookup"><span data-stu-id="3e0fb-147">Set up Inertia within ManipulationCompleted</span></span>

<span data-ttu-id="3e0fb-148">Nachdem die [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) -Methode aufgerufen wurde, muss das [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Objekt die Werte für das [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Objekt, das mit **IManipulationProcessor** verknüpft ist, zum Aufrufen von Trägheit festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-148">After the [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) method is invoked, the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) object must set the values for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) object linked to the **IManipulationProcessor** to invoke inertia.</span></span> <span data-ttu-id="3e0fb-149">Im folgenden Codebeispiel wird gezeigt, wie das **IInertiaProcessor** -Objekt aus der **IManipulationProcessor** -Methode " **manipulationabgeschlossene**" eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-149">The following code example shows how to set up the **IInertiaProcessor** object from the **IManipulationProcessor** method **ManipulationCompleted**.</span></span>

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

## <a name="clean-up-your-com-objects"></a><span data-ttu-id="3e0fb-150">Bereinigen der COM-Objekte</span><span class="sxs-lookup"><span data-stu-id="3e0fb-150">Clean up your COM Objects</span></span>

<span data-ttu-id="3e0fb-151">Wenn die Anwendung geschlossen wird, müssen Sie die COM-Objekte bereinigen.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-151">When your application closes, you must clean up your COM objects.</span></span> <span data-ttu-id="3e0fb-152">Der folgende Code zeigt, wie Sie die Ressourcen freigeben können, die im Beispiel zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-152">The following code shows how you can free the resources that were allocated in the sample.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3e0fb-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e0fb-153">Related topics</span></span>

<span data-ttu-id="3e0fb-154">Beispiel für [Multitouch-Bearbeitungs Anwendung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation und Trägheit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="3e0fb-154">[Multi-touch Manipulation Application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation and Inertia Sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>