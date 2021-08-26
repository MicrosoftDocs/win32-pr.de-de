---
title: Verwenden von DXCore zum Auflisten von Adaptern
description: Ein Blick auf die Hauptfeatures von DXCore mit einigen Codebeispielen sowie eine vollständige Quellcodeauflistung einer minimalen DXCore-Anwendung.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: fc2120c85b48b89478d1a10c8cf853c947e6553d
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812357"
---
# <a name="using-dxcore-to-enumerate-adapters"></a>Verwenden von DXCore zum Auflisten von Adaptern

DXCore ist eine Adapterenumerations-API für DirectX-Geräte, sodass sich einige ihrer Einrichtungen mit denen von [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)überschneiden.

DXCore ermöglicht die Belichtung neuer Gerätetypen im Benutzermodus, z. B. MCDM (Microsoft Compute Driver Model), für die Verwendung mit [Direct3D 12,](../direct3d12/directx-12-programming-guide.md) [DirectML](/windows/ai/directml/dml)und [Windows Machine Learning](/windows/ai/windows-ml/). DXCore stellt im Gegensatz zu DXGI keine Informationen zu anzeigebezogenen Technologien oder Eigenschaften bereit.

In den nächsten Abschnitten betrachten wir die Hauptfunktionen von DXCore mit einigen Codebeispielen (geschrieben in [C++/WinRT).](/windows/uwp/cpp-and-winrt-apis) Die unten gezeigten Codebeispiele werden aus der vollständigen Quellcodeauflistung extrahiert, die Sie im Thema [Minimale DXCore-Anwendung](dxcore-source-code.md)finden.

## <a name="create-an-adapter-factory"></a>Erstellen einer Adapterfactory

Sie beginnen mit der DXCore-Adapterenumeration, indem Sie ein Adapterfactoryobjekt erstellen, das durch die [**IDXCoreAdapterFactory-Schnittstelle**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) dargestellt wird. Um eine Factory zu erstellen, schließen Sie die `dxcore.h` Headerdatei ein, und rufen Sie die kostenlose [**DXCoreCreateAdapterFactory-Funktion**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) auf.

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Abrufen einer Adapterliste

Im Gegensatz zu DXGI erstellt eine neu erstellte DXCore-Adapterfactory nicht automatisch eine Momentaufnahme des Adapterzustands des Systems. Stattdessen erstellt DXCore diese Momentaufnahme, wenn Sie explizit ein Adapterlistenobjekt abrufen, das durch die [**IDXCoreAdapterList-Schnittstelle**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) dargestellt wird.

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Auswählen eines geeigneten Adapters aus der Liste

In diesem Abschnitt wird veranschaulicht, wie Sie bei verwendung eines Adapterlistenobjekts den ersten Hardwareadapter in der Liste finden können.

Die [**IDXCoreAdapterList::GetAdapterCount-Methode**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) teilt Ihnen die Anzahl der Elemente in der Liste mit, und [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) ruft einen bestimmten Adapter nach Index ab.

Sie können dann die Eigenschaften dieses Adapters abfragen, indem Sie diese Schritte ausführen.

- Zunächst rufen Sie [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md)auf, um zu bestätigen, dass es gültig ist, den Wert einer bestimmten Eigenschaft für diesen Adapter für diese Betriebssystemversion abzurufen. Übergeben Sie einen Wert der [**DXCoreAdapterProperty-Enumeration,**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) um zu identifizieren, welche Eigenschaft Sie abfragen.
- Bestätigen Sie optional die Größe des Eigenschaftswerts mit einem Aufruf von [**IDXCoreAdapter::GetPropertySize.**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md) Für eine Eigenschaft wie **DXCoreAdapterProperty::IsHardware**, bei der es sich um einen einfachen booleschen Wert handelt, ist dieser Schritt nicht erforderlich.
- Rufen Sie abschließend den Wert der Eigenschaft ab, indem [**Sie IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)aufrufen.

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Auswählen des bevorzugten Adapters durch Sortieren einer Adapterliste

Sie können eine DXCore-Adapterliste sortieren, indem Sie die [IDXCoreAdapterList::Sort-Methode](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) aufrufen.

Die [DXCoreAdapterPreference-Enumeration](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) definiert Werte, die Sortierkriterien darstellen. Übergeben Sie ein Array dieser Werte an **Sort**, und lesen Sie dann den ersten Adapter in der resultierenden sortierten Liste aus.

Rufen Sie zuerst [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)auf, um zu bestimmen, ob ein Sortiertyp von **Sort** verstanden werden soll.

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

## <a name="query-and-set-adapter-state-properties"></a>Abfragen und Festlegen des Adapterzustands (Eigenschaften)

Sie können den Zustand eines angegebenen Zustandselements eines Adapters abrufen und festlegen, indem Sie die Methoden [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) und [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) aufrufen.

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

In der Praxis sollten Sie vor dem Aufrufen von **QueryState** und **SetState** [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) aufrufen, um zu bestätigen, dass die Abfrage der Zustandsart für diesen Adapter und dieses Betriebssystem (Betriebssystem) verfügbar ist.

## <a name="adapter-list-freshness"></a>Aktualität der Adapterliste

Sollte eine Adapterliste aufgrund sich ändernder Systembedingungen veraltet sein, wird sie als solche gekennzeichnet. Sie können die Aktualität einer Adapterliste ermitteln, indem Sie die [**IDXCoreAdapterList::Is State-Methode**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) abfragen.

Allerdings können Sie Benachrichtigungen für Bedingungen wie Veraltung abonnieren. Übergeben Sie hierzu [**DXCoreNotificationType::AdapterList Stade**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) an [**IDXCoreAdapterFactory::RegisterEventNotification,**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)und speichern Sie das zurückgegebene Cookie sicher zur späteren Verwendung.

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

Anschließend können Sie ein neues, aktuelles Adapterlistenobjekt aus dem bereits verwendeten Factoryobjekt generieren. Die Behandlung dieser Bedingungen ist wichtig für die Möglichkeit, nahtlos auf Ereignisse wie das Ein- und Entfernen des Adapters (gpu oder spezialisierter Computeadapter) zu reagieren und workloads entsprechend zu verschieben.

Bevor Sie das Adapterlistenobjekt zerstören, müssen Sie die Registrierung dieses Objekts bei Benachrichtigungen mithilfe des Cookiewerts aufheben, indem Sie [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen. Wenn Sie die Registrierung nicht aufheben, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Anzeigen von Informationen

> [!NOTE]
> DXCore stellt selbst keine Anzeigeinformationen bereit. Bei Bedarf sollten Sie die Windows [**Runtime-Klasse DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) verwenden, um diese Informationen abzurufen. Die [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) eines Adapters stellt einen allgemeinen Bezeichner bereit, mit dem Sie [**DisplayMonitor.DisplayAdapterId-Informationen**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) einen DXCore-Adapter zuordnen können. Um die LUID eines Adapters abzurufen, übergeben Sie [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) an die [**IDXCoreAdapter::GetProperty-Methode.**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)

## <a name="see-also"></a>Siehe auch

* [Minimale DXCore-Anwendung](dxcore-source-code.md)
* [DXCore-Referenz](./dxcore-reference.md)
* [Direct3D 12-Grafiken](../direct3d12/direct3d-12-graphics.md)