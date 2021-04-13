---
title: Beispiel für die Windows-Berührungs Bearbeitung (mtmanipulation)
description: In diesem Abschnitt wird das Beispiel für die Windows-Berührungs Bearbeitung beschrieben.
ms.assetid: 59b9279c-ffa3-42c3-a01f-3ea7aca8f235
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows-Fingereingabe, Manipulationen
- Windows-Fingereingabe, Bearbeitungs Beispiel
- Manipulationen, Beispielcode
- Manipulationen, Codebeispiele
- Bearbeitungs Beispiel
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: b93ac4d7cd6724d5475c919c74b90eaf106d2803
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389859"
---
# <a name="windows-touch-manipulation-sample-mtmanipulation"></a>Beispiel für die Windows-Berührungs Bearbeitung (mtmanipulation)

In diesem Abschnitt wird das Beispiel für die Windows-Berührungs Bearbeitung beschrieben.

Das Beispiel zur Bearbeitung von Windows-Finger Eingaben veranschaulicht, wie ein Objekt mithilfe der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle übersetzt, gedreht und skaliert und eine [**_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Ereignis Senke implementiert wird. Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot, der das Beispiel für die Windows-touchmanipulation anzeigt, mit einem gedrehten, blau umschließenen weißen Rechteck mit blauen Linien aus umgekehrten Ecken](images/mtmanipulation.png)

Für dieses Beispiel wird eine **cdrawingobject** -Klasse erstellt, die Programm gesteuert übersetzt, gedreht oder skaliert werden kann. Eine [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle wird instanziiert. Eine Manipulations Ereignis Senke wird erstellt, die einen Zeiger auf die **cdrawingobject** -Klasse und die **IManipulationProcessor** -Schnittstelle für Ihren Konstruktor akzeptiert. Ein Verbindungspunkt mit dem IManipulationProcessor wird in der Implementierung der Manipulation-Ereignis Senke erstellt, sodass Ereignisse, die von **IManipulationProcessor** ausgelöst werden, von der Ereignis Senke empfangen werden. Berührungs Daten werden an die **IManipulationProcessor** -Schnittstelle geleitet, und die Schnittstelle gibt dann [**_IManipulationEvent**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) Ereignisse aus. Die Ereignishandler in der **CManipulationEventSink** -Klasse aktualisieren die Ausrichtung des **cdrawingobject** durch Aufrufen von Accessoren für den Zeiger auf das **cdrawingobject-Objekt**.

Der folgende Code zeigt, wie das Fenster für die Berührungs Einrichtung eingerichtet wird und wie **cdrawingobject** und [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) instanziiert und an den **CManipulationEventSink** -Konstruktor übergeben werden.

```C++
CDrawingObject g_cRect; // CDrawingObject class holds information about the rectangle
                        // and it is responsible for painting the rectangle.

(...)

BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
(...)
    // Register application window for receiving multi-touch input. Use default settings.
    if (!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multi-touch input", L"Error", MB_OK);
        return FALSE;
    }
    ASSERT(IsTouchWindow(hWnd, NULL));

    // Instantiate the ManipulationProcessor object
    HRESULT hr = CoCreateInstance(__uuidof(ManipulationProcessor), NULL, CLSCTX_ALL, IID_PPV_ARGS(&g_pIManipProc));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"InitInstance: failed to instantiate the ManipulationProcessor object");
        return FALSE;
    }

    // Instantiate the event sink with the manipulation processor and pointer to the rectangle object
    g_pManipulationEventSink = new CManipulationEventSink(&g_cRect);
    if (g_pManipulationEventSink == NULL)
    {
        ASSERT(g_pManipulationEventSink && L"InitInstance: failed to instantiate the CManipulationEventSink class");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        return FALSE;
    }

    // Establish the link between ManipulationEventSink and ManipulationProcessor
    if (!g_pManipulationEventSink->Connect(g_pIManipProc))
    {
        ASSERT(FALSE && L"InitInstance: failed to connect ManipulationEventSink and ManipulationProcessor");
        g_pIManipProc->Release();
        g_pIManipProc = NULL;
        g_pManipulationEventSink->Release();
        g_pManipulationEventSink = NULL;
        return FALSE;
    }
```

Der folgende Code zeigt den Konstruktor für die Manipulation-Ereignis Senke " **CManipulationEventSink**".

```C++
CManipulationEventSink::CManipulationEventSink(CDrawingObject* pcDrawingObject)
:   m_cRefCount(1),
    m_pConnection(NULL),
    m_dwCookie(0),
    m_pcDrawingObject(pcDrawingObject)
{
    ASSERT((pcDrawingObject != NULL) && L"CManipulationEventSink constructor: incorrect argument");
}
```

Der folgende Code zeigt, wie die Ereignis Senke mit dem Manipulations Prozessor verbunden ist.

```C++
bool CManipulationEventSink::Connect(IManipulationProcessor* pManipulationProcessor)
{
    // Check input arguments
    if (pManipulationProcessor == NULL)
    {
        ASSERT((pManipulationProcessor != NULL) && L"CManipulationEventSink::Create : incorrect arguments");
        return false;
    }

    // Check object state
    if ((m_dwCookie != 0) || (m_pConnection != NULL))
    {
        ASSERT((m_dwCookie == 0) && (m_pConnection == NULL) && L"CManipulationEventSink::Connect : connection already established");
        return false;
    }

    // Get the container with the connection points.
    IConnectionPointContainer* pConnectionContainer = NULL;
    HRESULT hr = pManipulationProcessor->QueryInterface(&pConnectionContainer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get the container with the connection points");
        return false;
    }

    // Get a connection point.
    hr = pConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnection);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to get a connection point");
        pConnectionContainer->Release();
        return false;
    }

    // Release the connection container.
    pConnectionContainer->Release();

    // Advise. Establishes an advisory connection between the connection point and the
    // caller's sink object.
    hr = m_pConnection->Advise(this, &m_dwCookie);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CManipulationEventSink::Connect : failed to Advise");
        m_pConnection->Release();
        m_pConnection = NULL;
        return false;
    }

    return true;
}
```

Der folgende Code zeigt, wie Berührungs Daten an die Manipulations Ereignis Senke übermittelt werden.

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
(...)

    switch (message)
    {
 (...)
    // WM_TOUCH message handlers
    case WM_TOUCH:
        {
            // WM_TOUCH message can contain several messages from different contacts
            // packed together.
            // Message parameters need to be decoded:
            UINT  cInputs  = (int) wParam;      // Number of actual per-contact messages
            TOUCHINPUT* pInputs = new TOUCHINPUT[cInputs]; // Allocate the storage for the parameters of the per-contact messages
            if (pInputs == NULL)
            {
                break;
            }
            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT)))
            {
                // For each contact, dispatch the message to the appropriate message
                // handler.
                for (unsigned int i = 0; i < cInputs; i++)
                {
                    if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN)
                    {
                        g_pIManipProc->ProcessDown(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE)
                    {
                        g_pIManipProc->ProcessMove(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                    else if (pInputs[i].dwFlags & TOUCHEVENTF_UP)
                    {
                        g_pIManipProc->ProcessUp(pInputs[i].dwID, (FLOAT)pInputs[i].x, (FLOAT)pInputs[i].y);
                    }
                }
            }
            else
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute GetTouchInputInfo");
                delete [] pInputs;
                break;
            }
            if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
            {
                // error handling, presumably out of memory
                ASSERT(FALSE && L"Error: failed to execute CloseTouchInputHandle");
                delete [] pInputs;
                break;
            }
            delete [] pInputs;

            // Force redraw of the rectangle
            InvalidateRect(hWnd, NULL, TRUE);
        }
        break;
```

Der folgende Code zeigt, wie die Ereignishandler die Objekt Ausrichtung und-Größe für Manipulations Änderungs Ereignisse aktualisieren.

```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta(
    /* [in] */ FLOAT /* x */,
    /* [in] */ FLOAT /* y */,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT /* expansionDelta */,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT /* cumulativeTranslationX */,
    /* [in] */ FLOAT /* cumulativeTranslationY */,
    /* [in] */ FLOAT /* cumulativeScale */,
    /* [in] */ FLOAT /* cumulativeExpansion */,
    /* [in] */ FLOAT /* cumulativeRotation */)
{
    m_pcDrawingObject->ApplyManipulationDelta(translationDeltaX,translationDeltaY,scaleDelta,rotationDelta);

    return S_OK;
}
```

Der folgende Code ist die Implementierung von **applymanipulationdelta** in der **cdrawingobject** -Klasse.

```C++
// This function is responsible for manipulation of the rectangle.
// It is called from CManipulationEventSink class.
// in:
//      translationDeltaX - shift of the x-coordinate (1/100 of pixel units)
//      translationDeltaY - shift of the y-coordinate (1/100 of pixel units)
//             scaleDelta - scale factor (zoom in/out)
//          rotationDelta - rotation angle in radians
void CDrawingObject::ApplyManipulationDelta(
    const FLOAT translationDeltaX,
    const FLOAT translationDeltaY,
    const FLOAT scaleDelta,
    const FLOAT rotationDelta
)
{
    _ptCenter.x += (LONG) (translationDeltaX / 100.0);
    _ptCenter.y += (LONG) (translationDeltaY / 100.0);

    _dScalingFactor *= scaleDelta;

    _dRotationAngle -= rotationDelta; // we are substracting because Y-axis is down
}
```

Nachdem die Mittelpunkte, der Skalierungsfaktor und der Drehungs Winkel des **cdrawingobject** aktualisiert wurden, zeichnet sich das Objekt selbst transformiert.

## <a name="related-topics"></a>Zugehörige Themen

Beispiel für [Multitouch-Bearbeitungs Anwendung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulation/cpp), [Manipulation und Trägheit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTManipulationInertia/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)
