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
# <a name="using-dxcore-to-enumerate-adapters"></a>Verwenden von DXCore zum Auflisten von Adaptern

DXCore ist eine adapterenumerationsapi für DirectX-Geräte, sodass sich einige ihrer Funktionen mit denen von [DXGI](../direct3ddxgi/dx-graphics-dxgi.md)überschneiden.

DXCore ermöglicht das verfügbar machen neuer Gerätetypen im Benutzermodus, wie z. b. mcdm (Microsoft Compute Driver Model), für die Verwendung mit [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [directml](../direct3d12/dml.md)und [Windows Machine Learning](/windows/ai/windows-ml/). DXCore bietet im Gegensatz zu DXGI keine Informationen über die Anzeige bezogene Technologie oder Eigenschaften.

In den nächsten Abschnitten werden die Hauptfunktionen von DXCore mit einigen Codebeispielen (geschrieben in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)) betrachtet. Die unten gezeigten Codebeispiele werden aus der vollständigen Quell Code Auflistung extrahiert, die Sie im Thema [minimale DXCore-Anwendung](dxcore-source-code.md)finden können.

## <a name="create-an-adapter-factory"></a>Erstellen einer AdapterFactory

Sie beginnen die DXCore-adapterenumeration, indem Sie ein adapterfactoryobjekt erstellen, das durch die [**idxcoreadapterfactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle dargestellt wird. Um eine Factory zu erstellen, schließen Sie die `dxcore.h` Header Datei ein, und rufen Sie die kostenlose [**dxcorecreateadapterfactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) -Funktion auf.

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Abrufen einer Adapter Liste

Anders als bei DXGI erstellt eine neu erstellte DXCore-AdapterFactory nicht automatisch eine Momentaufnahme des Adapter Zustands des Systems. Stattdessen erstellt DXCore diese Momentaufnahme, wenn Sie explizit ein Adapter Listen Objekt abrufen, das durch die [**idxcoreadapterlist**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle dargestellt wird.

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Wählen Sie einen geeigneten Adapter aus der Liste aus.

In diesem Abschnitt wird veranschaulicht, wie Sie bei einem Adapter Listen Objekt den ersten Hardware Adapter in der Liste finden.

Die [**idxcoreadapterlist:: getadaptercount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) -Methode gibt Aufschluss über die Anzahl der Elemente in der Liste, und [**idxcoreadapterlist:: GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) Ruft einen bestimmten Adapter nach Index ab.

Sie können dann die Eigenschaften des Adapters Abfragen, indem Sie die folgenden Schritte ausführen.

- Um zu bestätigen, dass es zum Abrufen des Werts einer bestimmten Eigenschaft für diesen Adapter in dieser Betriebssystemversion gültig ist, rufen Sie zunächst [**idxcoreadapter:: ispropertysupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md)auf. Übergeben Sie einen Wert der [**dxcoreadapterproperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) -Enumeration, um die Eigenschaft zu identifizieren, zu der Sie Abfragen.
- Überprüfen Sie optional die Größe des Eigenschafts Werts mit einem Aufrufen von [**idxcoreadapter:: getpropertysize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Für eine Eigenschaft wie **dxcoreadapterproperty:: ishardware**, bei der es sich um einen einfachen booleschen Wert handelt, ist dieser Schritt nicht erforderlich.
- Und schließlich rufen Sie den Wert der Eigenschaft durch Aufrufen von [**idxcoreadapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md)ab.

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Wählen Sie den bevorzugten Adapter aus, indem Sie eine Adapter Liste sortieren.

Sie können eine DXCore-Adapter Liste sortieren, indem Sie die [idxcoreadapterlist:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) -Methode aufrufen.

Die [dxcoreadapterpreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) -Enumeration definiert Werte, die Sortierkriterien darstellen. Übergeben Sie ein Array dieser Werte, um Sie zu **Sortieren**, und lesen Sie dann den ersten Adapter in der sich ergebenden sortierten Liste.

Um zu ermitteln, ob ein Sortierungstyp von **Sort** interpretiert werden soll, müssen Sie zuerst [idxcoreadapterlist:: isadapterpreferencesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)aufrufen.

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

## <a name="query-and-set-adapter-state-properties"></a>Abfrage und Festlegen des Adapter Status (Eigenschaften)

Sie können den Zustand eines angegebenen Zustands Elements eines Adapters abrufen und festlegen, indem Sie die [**idxcoreadapter:: querystate**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) -Methode und die [**idxcoreadapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) -Methode aufrufen.

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

In der Praxis sollten Sie vor dem Aufrufen von " **querystate** " und " **SetState**" [isquerystaatupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) aufrufen, um zu bestätigen, dass die Abfrage der Statusart für diesen Adapter und dieses Betriebssystem (OS) verfügbar ist.

## <a name="adapter-list-freshness"></a>Aktualität der Adapter Liste

Wenn eine Adapter Liste aufgrund von veränderlichen Systembedingungen veraltet ist, wird Sie als solche gekennzeichnet. Sie können die Aktualität einer Adapter Liste ermitteln, indem Sie die [**idxcoreadapterlist:: isstale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) -Methode abrufen.

Bequemer ist jedoch, dass Sie Benachrichtigungen für Bedingungen wie Veraltung abonnieren können. Übergeben Sie hierzu [**dxcorenotificationtype:: adapterliststale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) an [**idxcoreadapterfactory:: registereventnotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), und speichern Sie das zurückgegebene Cookie sicher für die spätere Verwendung.

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

Sie können dann ein neues, Aktuelles Adapter Listen Objekt aus dem bereits vorhanden Factoryobjekt generieren. Die Behandlung dieser Bedingungen ist wichtig für die nahtlose Reaktion auf Ereignisse wie das eintreffen und Entfernen von Adaptern (unabhängig davon, ob es sich um eine GPU oder einen spezialisierten Compute-Adapter handelt) und die angemessene Verschiebung von Arbeits Auslastungen als Reaktion.

Bevor Sie das Adapter Listen Objekt zerstören, müssen Sie den Cookie-Wert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen aufzuheben, indem Sie [idxcoreadapterfactory:: unregistereventnotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen. Wenn Sie die Registrierung nicht aufheben, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Anzeigeinformationen

> [!NOTE]
> DXCore stellt keine Anzeigeinformationen bereit. Verwenden Sie bei Bedarf die Windows-Runtime [**displaymonitor**](/uwp/api/windows.devices.display.displaymonitor) -Klasse, um diese Informationen abzurufen. Die [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) eines Adapters stellt einen allgemeinen Bezeichner bereit, mit dem Sie einem DXCore-Adapter [**Display Monitor. displayadapterid**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) -Informationen zuordnen können. Um die LUID eines Adapters zu erhalten, übergeben Sie [**dxcoreadapterproperty:: instanceluid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) an die [**idxcoreadapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) -Methode.

## <a name="see-also"></a>Siehe auch

* [Minimale DXCore-Anwendung](dxcore-source-code.md)
* [DXCore-Referenz](./dxcore-reference.md)
* [Direct3D 12-Grafiken](../direct3d12/direct3d-12-graphics.md)