---
description: So erhalten Sie Ereignisse aus der Netzwerkquelle
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: So erhalten Sie Ereignisse aus der Netzwerkquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753584"
---
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="882d3-103">So erhalten Sie Ereignisse aus der Netzwerkquelle</span><span class="sxs-lookup"><span data-stu-id="882d3-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="882d3-104">Der Quell Konflikt Löser ermöglicht einer Anwendung das Erstellen einer Netzwerkquelle und das Öffnen einer Verbindung mit einer bestimmten URL.</span><span class="sxs-lookup"><span data-stu-id="882d3-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="882d3-105">Die Netzwerkquelle löst Ereignisse aus, um den Anfang und das Ende des asynchronen Vorgangs zum Öffnen einer Verbindung zu markieren.</span><span class="sxs-lookup"><span data-stu-id="882d3-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="882d3-106">Eine Anwendung kann sich für diese Ereignisse mithilfe der [**IMF sourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle registrieren.</span><span class="sxs-lookup"><span data-stu-id="882d3-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="882d3-107">Diese Schnittstelle macht die [**IMF sourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode verfügbar, die von der Netzwerkquelle direkt aufgerufen wird, wenn die URL asynchron geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="882d3-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="882d3-108">Die Netzwerkquelle benachrichtigt die Anwendung, wenn Sie mit dem Öffnen der URL beginnt, indem das [meconnectstart](meconnectstart.md) -Ereignis aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="882d3-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="882d3-109">Die Netzwerkquelle löst dann das [meconnectend](meconnectend.md) -Ereignis aus, wenn der Öffnungsvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="882d3-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="882d3-110">Um diese Ereignisse an die Anwendung zu senden, verwendet die Netzwerkquelle die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle nicht, da diese Ereignisse vor der Erstellung der Netzwerkquelle ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="882d3-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="882d3-111">Die Anwendung kann alle anderen Netzwerk Quell Ereignisse mithilfe der **IMF mediaeventgenerator** -Schnittstelle der Medien Sitzung erhalten.</span><span class="sxs-lookup"><span data-stu-id="882d3-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="882d3-112">So erhalten Sie Ereignisse aus der Netzwerkquelle</span><span class="sxs-lookup"><span data-stu-id="882d3-112">To get events from the network source</span></span>

1.  <span data-ttu-id="882d3-113">Implementieren Sie die [**IMF sourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="882d3-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="882d3-114">Führen Sie in ihrer Implementierung der [**IMF sourceopenmonitor:: onsourceevent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) -Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="882d3-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="882d3-115">Rufen Sie den Ereignis Status durch Aufrufen von [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)ab.</span><span class="sxs-lookup"><span data-stu-id="882d3-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="882d3-116">Diese Methode gibt an, ob der Vorgang, der das Ereignis ausgelöst hat, z. b. ein quellresolver-Methodenaufrufe, erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="882d3-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="882d3-117">Wenn der Vorgang nicht erfolgreich ist, ist der Status ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="882d3-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="882d3-118">Verarbeiten Sie das Ereignis basierend auf dem Ereignistyp: [meconnectstart](meconnectstart.md) oder [meconnectend](meconnectend.md), den die Anwendung durch Aufrufen von [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype)abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="882d3-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="882d3-119">Konfigurieren Sie ein Schlüssel-Wert-Paar in einem Eigenschaften Speicher Objekt zum Speichern eines Zeigers auf die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Implementierung, die in Schritt 1 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="882d3-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="882d3-120">Erstellen Sie ein Eigenschaften Speicher Objekt, indem Sie die **pscreatememorypropertystore** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="882d3-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="882d3-121">Legen Sie die [**mfpkey \_ sourceopenmonitor**](mfpkey-sourceopenmonitor-property.md) -Eigenschaft in einer **PropertyKey** -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="882d3-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="882d3-122">Geben Sie den \_ Wert "VT Unknown Type Data" in einer **PROPVARIANT** -Struktur an, indem Sie den **IUnknown** -Zeiger auf die Implementierung der Anwendung der [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="882d3-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="882d3-123">Legen Sie das Schlüssel-Wert-Paar im Eigenschaften Speicher durch Aufrufen von **IPropertyStore:: SetValue** fest.</span><span class="sxs-lookup"><span data-stu-id="882d3-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="882d3-124">Übergeben Sie den Eigenschafts Speicher Zeiger an die Quell Auflösungs Methoden, die die Anwendung verwendet, um die Netzwerkquelle zu erstellen, z. b. [**imfsourceresolver:: deateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) und andere.</span><span class="sxs-lookup"><span data-stu-id="882d3-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="882d3-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="882d3-125">Example</span></span>

<span data-ttu-id="882d3-126">Im folgenden Beispiel wird gezeigt, wie Sie die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle implementieren, um Ereignisse aus der Netzwerkquelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="882d3-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



<span data-ttu-id="882d3-127">Im folgenden Beispiel wird gezeigt, wie die [**mfpkey \_ sourceopenmonitor**](mfpkey-sourceopenmonitor-property.md) -Eigenschaft in der Netzwerkquelle festgelegt wird, wenn Sie die URL öffnen:</span><span class="sxs-lookup"><span data-stu-id="882d3-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="882d3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="882d3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="882d3-129">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="882d3-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



