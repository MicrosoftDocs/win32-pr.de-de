---
title: Übersicht über Deskriptoren
description: Deskriptoren werden durch API-Aufrufe erstellt und identifizieren Ressourcen.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cb5834c513b99e737ba8a106ea5303a978751573ffd2ca1a97fb59e385b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733842"
---
# <a name="descriptors-overview"></a>Übersicht über Deskriptoren

Deskriptoren werden durch API-Aufrufe erstellt und identifizieren Ressourcen.

-   [Deskriptordaten](#descriptor-data)
-   [Deskriptorhandles](#descriptor-handles)
-   [NULL-Deskriptoren](#null-descriptors)
-   [Standarddeskriptoren](#default-descriptors)
-   [Zugehörige Themen](#related-topics)

## <a name="descriptor-data"></a>Deskriptordaten

Ein Deskriptor ist ein relativ kleiner Datenblock, der ein Objekt für die GPU in einem GPU-spezifischen nicht transparenten Format vollständig beschreibt. Es gibt verschiedene Arten von Deskriptoren, die Zielansichten (RTVs), Tiefenschablonenansichten (DSVs), Shaderressourcenansichten (SRVs), ungeordnete Zugriffsansichten (UNVs), konstanten Pufferansichten &mdash; (CBVs) und Sampler rendern.

Deskriptoren variieren je nach GPU-Hardware. Sie können die Größe einer SRV-, UAV- oder CBV-Datei abfragen, indem Sie [**ID3D12Device::GetDescriptorHandleIncrementSize aufrufen.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) Deskriptoren werden in dieser Dokumentation als unteilbare Einheiten dargestellt. Hier ist ein Beispiel.

![srv, cbv, uav und sampler](images/single-descriptor.png)

Deskriptoren werden durch API-Aufrufe erstellt und enthalten Informationen wie die Ressource und die MIP-Zuordnungen, die der Deskriptor enthalten soll.

Der Treiber verfolgt keine Verweise auf Deskriptoren nach oder enthält sie, es liegt an der App, sicherzustellen, dass der richtige Deskriptortyp verwendet wird und dass die Informationen aktuell sind. Es gibt eine kleine Ausnahme: Der Treiber überprüft Renderzielbindungen, um sicherzustellen, dass Austauschketten ordnungsgemäß funktionieren.

Objektdeskriptoren müssen nicht freigegeben oder freigegeben werden. Treiber fügen keine Zuordnungen an die Erstellung eines Deskriptors an. Ein Deskriptor kann jedoch Verweise auf andere Zuordnungen codieren, für die die Anwendung die Lebensdauer besitzt. Beispielsweise muss ein Deskriptor für einen SRV die virtuelle Adresse der D3D-Ressource (z. B. eine Textur) enthalten, auf die der SRV verweist. Die Anwendung muss sicherstellen, dass kein SRV-Deskriptor verwendet wird, wenn die zugrunde liegende D3D-Ressource, von der sie abhängt, zerstört wurde oder geändert wird (z. B. als nichtresident deklariert).

Die primäre Möglichkeit zur Verwendung von Deskriptoren besteht in derEntortierung in Deskriptorhaps, die Speicher für Deskriptoren sichern.

## <a name="descriptor-handles"></a>Deskriptorhandles

Ein Deskriptorhand handle ist die eindeutige Adresse des Deskriptors. Er ähnelt einem Zeiger, ist aber nicht transparent, da seine Implementierung hardwarespezifisch ist. Das Handle ist über Deskriptor-Heaps hinweg eindeutig, sodass beispielsweise ein Array von Handles auf Deskriptoren in mehreren Heaps verweisen kann.

CPU-Handles sind für die sofortige Verwendung bestimmt, z. B. das Kopieren, wenn sowohl die Quelle als auch das Ziel identifiziert werden müssen. Unmittelbar nach der Verwendung (z. B. einem Aufruf von [**ID3D12GraphicsCommandList::OMSetRenderTargets)**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)können sie wiederverwendet oder der zugrunde liegende Heap verworfen werden.

GPU-Handles sind nicht zur sofortigen Verwendung da sie Speicherorte aus einer Befehlsliste identifizieren &mdash; und zur GPU-Ausführungszeit verwendet werden können. Sie müssen beibehalten werden, bis alle Befehlslisten, die auf sie verweisen, vollständig ausgeführt wurden.

Um ein Deskriptorhand handle für den Anfang eines Heaps zu erstellen, rufen Sie nach dem Erstellen des Deskriptorhaps selbst eine der folgenden Methoden auf:

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Diese Methoden geben die folgenden Strukturen zurück:

-   [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**D3D12 \_ \_ GPU-DESKRIPTORHAND \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Da die Größe der Deskriptoren je nach Hardware variiert, verwenden Sie, um das Inkrement zwischen jedem Deskriptor in einem Heap zu erhalten:

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

Es ist sicher, eine Startposition mit einer Reihe von Schritten zu vertauschen, Handles zu kopieren und Handles an API-Aufrufe zu übergeben. Es ist nicht sicher, ein Handle so zu dereferenzieren, als wäre es ein gültiger CPU-Zeiger, und die Bits innerhalb eines Handles können nicht analysiert werden.

Einige Hilfsstrukturen wurden mit Initialisierungsmitgliedern hinzugefügt, um die Verwaltung von Handles etwas zu vereinfachen.

-   [**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE**](cd3dx12-cpu-descriptor-handle.md)
-   [**CD3DX12 \_ \_ GPU-DESKRIPTORHAND \_ HANDLE**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>NULL-Deskriptoren

Beim Erstellen von Deskriptoren mitHILFE von API-Aufrufen übergeben Anwendungen NULL für den Ressourcenzeiger in der Deskriptordefinition, um den Effekt von nichts zu erreichen, das beim Zugriff durch einen Shader gebunden ist.

Der Rest des Deskriptors muss so weit wie möglich aufgefüllt werden. Im Fall von Shader-Ressourcenansichten (SrVs) kann beispielsweise der Deskriptor verwendet werden, um den Typ der Ansicht (Texture1D, Texture2D und so weiter) zu unterscheiden. Numerische Parameter im Ansichtsdeskriptor, z. B. die Anzahl von Mipmaps, müssen alle auf Werte festgelegt werden, die für eine Ressource gültig sind.

In vielen Fällen gibt es ein definiertes Verhalten für den Zugriff auf eine ungebundene Ressource, z. B. SRVs, die Standardwerte zurückgeben. Diese werden beim Zugriff auf einen NULL-Deskriptor verwendet, solange der Typ des Shaderzugriffs mit dem Deskriptortyp kompatibel ist. Wenn ein Shader beispielsweise einen Texture2D-SRV erwartet und auf einen null-SRV zutritt, der als Texture1D definiert ist, ist das Verhalten nicht definiert und kann zur Gerätezurücksetzung führen.

Um einen NULL-Deskriptor zu erstellen, übergeben Sie zusammenfassend für den pResource-Parameter, wenn Sie die Ansicht mit Methoden wie `null` [**CreateShaderResourceView erstellen.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)  Legen Sie für den Ansichtsbeschreibungsparameter *pDesc* eine Konfiguration fest, die funktioniert, wenn die Ressource nicht NULL ist (andernfalls kann ein Absturz auf einer Hardware auftreten).

Stammdeskriptoren sollten jedoch nicht auf NULL festgelegt werden.

Auf Hardware der [](./hardware-support.md)Ebene 1 (siehe Hardwareebenen) müssen alle Deskriptoren, die (über Deskriptortabellen) gebunden sind, entweder als echte Deskriptoren oder NULL-Deskriptoren initialisiert werden, auch wenn die Hardware nicht darauf zuspricht. Andernfalls ist das Verhalten nicht definiert.

Auf Hardware der Ebene 2 gilt dies für gebundene CBV- und UAV-Deskriptoren, aber nicht für SRV-Deskriptoren.

Auf Hardware der Ebene 3 gibt es keine Einschränkung, vorausgesetzt, dass nie auf nicht initialisierte Deskriptoren zugegriffen wird.

## <a name="default-descriptors"></a>Standarddeskriptoren

Um einen Standarddeskriptor für eine bestimmte Ansicht zu erstellen, übergeben Sie einen gültigen *pResource-Parameter* an die Create View-Methode (z. B. [**CreateShaderResourceView),**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)übergeben aber **NULL** für den *pDesc-Parameter.* Wenn die Ressource beispielsweise 14 Mips enthält, enthält die Ansicht 14 Mips. Der Standardfall deckt die offensichtlichste Zuordnung einer Ressource zu einer Ansicht ab. Dies erfordert, dass die Ressource mit einem vollqualifizierten Formatnamen zugeordnet wird (z. B. DXGI_FORMAT_R8G8B8A8_UNORM_SRGB **anstelle** **DXGI_FORMAT_R8G8B8A8_TYPELESS).**

Standarddeskriptoren können nicht mit einer Raytracingbeschleunigungsstrukturansicht verwendet werden, da der bereitgestellte *pResource-Parameter* **NULL** sein muss und der Speicherort über **[D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv) übergeben werden muss.

## <a name="related-topics"></a>Zugehörige Themen

[Deskriptoren](descriptors.md)