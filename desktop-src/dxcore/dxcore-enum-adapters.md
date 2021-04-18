---
title: Verwenden von DXCore zum Auflisten von Adaptern
description: Sehen Sie sich die Haupt Features von DXCore mit einigen Codebeispielen sowie eine vollständige Quell Code Auflistung einer minimalen DXCore-Anwendung an.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338463"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="21385-103">Verwenden von DXCore zum Auflisten von Adaptern</span><span class="sxs-lookup"><span data-stu-id="21385-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="21385-104">DXCore ist eine adapterenumerationsapi für DirectX-Geräte, sodass sich einige ihrer Funktionen mit denen von [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)überschneiden.</span><span class="sxs-lookup"><span data-stu-id="21385-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="21385-105">DXCore ermöglicht das verfügbar machen neuer Gerätetypen im Benutzermodus, wie z. b. mcdm (Microsoft Compute Driver Model), für die Verwendung mit [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [directml](../direct3d12/dml.md)und [Windows Machine Learning](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="21385-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="21385-106">DXCore bietet im Gegensatz zu DXGI keine Informationen über die Anzeige bezogene Technologie oder Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21385-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="21385-107">In den nächsten Abschnitten werden die Hauptfunktionen von DXCore mit einigen Codebeispielen (geschrieben in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)) betrachtet.</span><span class="sxs-lookup"><span data-stu-id="21385-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="21385-108">Die unten gezeigten Codebeispiele werden aus der vollständigen Quell Code Auflistung extrahiert, die Sie im Thema [minimale DXCore-Anwendung](dxcore-source-code.md)finden können.</span><span class="sxs-lookup"><span data-stu-id="21385-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="21385-109">Erstellen einer AdapterFactory</span><span class="sxs-lookup"><span data-stu-id="21385-109">Create an adapter factory</span></span>

<span data-ttu-id="21385-110">Sie beginnen die DXCore-adapterenumeration, indem Sie ein adapterfactoryobjekt erstellen, das durch die [**idxcoreadapterfactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="21385-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="21385-111">Um eine Factory zu erstellen, schließen Sie die `dxcore.h` Header Datei ein, und rufen Sie die kostenlose [**dxcorecreateadapterfactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="21385-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="21385-112">Abrufen einer Adapter Liste</span><span class="sxs-lookup"><span data-stu-id="21385-112">Retrieve an adapter list</span></span>

<span data-ttu-id="21385-113">Anders als bei DXGI erstellt eine neu erstellte DXCore-AdapterFactory nicht automatisch eine Momentaufnahme des Adapter Zustands des Systems.</span><span class="sxs-lookup"><span data-stu-id="21385-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="21385-114">Stattdessen erstellt DXCore diese Momentaufnahme, wenn Sie explizit ein Adapter Listen Objekt abrufen, das durch die [**idxcoreadapterlist**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="21385-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="21385-115">Wählen Sie einen geeigneten Adapter aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="21385-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="21385-116">In diesem Abschnitt wird veranschaulicht, wie Sie bei einem Adapter Listen Objekt den ersten Hardware Adapter in der Liste finden.</span><span class="sxs-lookup"><span data-stu-id="21385-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="21385-117">Die [**idxcoreadapterlist:: getadaptercount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) -Methode gibt Aufschluss über die Anzahl der Elemente in der Liste, und [**idxcoreadapterlist:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) Ruft einen bestimmten Adapter nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="21385-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="21385-118">Sie können dann die Eigenschaften des Adapters Abfragen, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="21385-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="21385-119">Um zu bestätigen, dass es zum Abrufen des Werts einer bestimmten Eigenschaft für diesen Adapter in dieser Betriebssystemversion gültig ist, rufen Sie zunächst [**idxcoreadapter:: ispropertysupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md)auf.</span><span class="sxs-lookup"><span data-stu-id="21385-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="21385-120">Übergeben Sie einen Wert der [**dxcoreadapterproperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) -Enumeration, um die Eigenschaft zu identifizieren, zu der Sie Abfragen.</span><span class="sxs-lookup"><span data-stu-id="21385-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="21385-121">Überprüfen Sie optional die Größe des Eigenschafts Werts mit einem Aufrufen von [**idxcoreadapter:: getpropertysize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="21385-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="21385-122">Für eine Eigenschaft wie **dxcoreadapterproperty:: ishardware**, bei der es sich um einen einfachen booleschen Wert handelt, ist dieser Schritt nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="21385-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="21385-123">Und schließlich rufen Sie den Wert der Eigenschaft durch Aufrufen von [**idxcoreadapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="21385-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="21385-124">Wählen Sie den bevorzugten Adapter aus, indem Sie eine Adapter Liste sortieren.</span><span class="sxs-lookup"><span data-stu-id="21385-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="21385-125">Sie können eine DXCore-Adapter Liste sortieren, indem Sie die [idxcoreadapterlist:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21385-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="21385-126">Die [dxcoreadapterpreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) -Enumeration definiert Werte, die Sortierkriterien darstellen.</span><span class="sxs-lookup"><span data-stu-id="21385-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="21385-127">Übergeben Sie ein Array dieser Werte, um Sie zu **Sortieren**, und lesen Sie dann den ersten Adapter in der sich ergebenden sortierten Liste.</span><span class="sxs-lookup"><span data-stu-id="21385-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="21385-128">Um zu ermitteln, ob ein Sortierungstyp von **Sort** interpretiert werden soll, müssen Sie zuerst [idxcoreadapterlist:: isadapterpreferencesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21385-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="21385-129">Abfrage und Festlegen des Adapter Status (Eigenschaften)</span><span class="sxs-lookup"><span data-stu-id="21385-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="21385-130">Sie können den Zustand eines angegebenen Zustands Elements eines Adapters abrufen und festlegen, indem Sie die [**idxcoreadapter:: querystate**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) -Methode und die [**idxcoreadapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21385-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="21385-131">In der Praxis sollten Sie vor dem Aufrufen von " **querystate** " und " **SetState**" [isquerystaatupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) aufrufen, um zu bestätigen, dass die Abfrage der Statusart für diesen Adapter und dieses Betriebssystem (OS) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="21385-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="21385-132">Aktualität der Adapter Liste</span><span class="sxs-lookup"><span data-stu-id="21385-132">Adapter list freshness</span></span>

<span data-ttu-id="21385-133">Wenn eine Adapter Liste aufgrund von veränderlichen Systembedingungen veraltet ist, wird Sie als solche gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="21385-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="21385-134">Sie können die Aktualität einer Adapter Liste ermitteln, indem Sie die [**idxcoreadapterlist:: isstale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="21385-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="21385-135">Bequemer ist jedoch, dass Sie Benachrichtigungen für Bedingungen wie Veraltung abonnieren können.</span><span class="sxs-lookup"><span data-stu-id="21385-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="21385-136">Übergeben Sie hierzu [**dxcorenotificationtype:: adapterliststale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) an [**idxcoreadapterfactory:: registereventnotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), und speichern Sie das zurückgegebene Cookie sicher für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="21385-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="21385-137">Sie können dann ein neues, Aktuelles Adapter Listen Objekt aus dem bereits vorhanden Factoryobjekt generieren.</span><span class="sxs-lookup"><span data-stu-id="21385-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="21385-138">Die Behandlung dieser Bedingungen ist wichtig für die nahtlose Reaktion auf Ereignisse wie das eintreffen und Entfernen von Adaptern (unabhängig davon, ob es sich um eine GPU oder einen spezialisierten Compute-Adapter handelt) und die angemessene Verschiebung von Arbeits Auslastungen als Reaktion.</span><span class="sxs-lookup"><span data-stu-id="21385-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="21385-139">Bevor Sie das Adapter Listen Objekt zerstören, müssen Sie den Cookie-Wert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen aufzuheben, indem Sie [idxcoreadapterfactory:: unregistereventnotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21385-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="21385-140">Wenn Sie die Registrierung nicht aufheben, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="21385-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="21385-141">Anzeigeinformationen</span><span class="sxs-lookup"><span data-stu-id="21385-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="21385-142">DXCore stellt keine Anzeigeinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="21385-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="21385-143">Verwenden Sie bei Bedarf die Windows-Runtime [**displaymonitor**](/uwp/api/windows.devices.display.displaymonitor) -Klasse, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="21385-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="21385-144">Die [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) eines Adapters stellt einen allgemeinen Bezeichner bereit, mit dem Sie einem DXCore-Adapter [**Display Monitor. displayadapterid**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) -Informationen zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="21385-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="21385-145">Um die LUID eines Adapters zu erhalten, übergeben Sie [**dxcoreadapterproperty:: instanceluid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) an die [**idxcoreadapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="21385-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="21385-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21385-146">See also</span></span>

* [<span data-ttu-id="21385-147">Minimale DXCore-Anwendung</span><span class="sxs-lookup"><span data-stu-id="21385-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="21385-148">DXCore-Referenz</span><span class="sxs-lookup"><span data-stu-id="21385-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="21385-149">Direct3D 12-Grafiken</span><span class="sxs-lookup"><span data-stu-id="21385-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)