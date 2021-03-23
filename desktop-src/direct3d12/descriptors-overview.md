---
title: Übersicht über Deskriptoren
description: Deskriptoren werden von API-aufrufen erstellt und identifizieren Ressourcen.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548700"
---
# <a name="descriptors-overview"></a>Übersicht über Deskriptoren

Deskriptoren werden von API-aufrufen erstellt und identifizieren Ressourcen.

-   [Deskriptordaten](#descriptor-data)
-   [Deskriptorhandles](#descriptor-handles)
-   [NULL-Deskriptoren](#null-descriptors)
-   [Standard Deskriptoren](#default-descriptors)
-   [Verwandte Themen](#related-topics)

## <a name="descriptor-data"></a>Deskriptordaten

Ein Deskriptor ist ein relativ kleiner Datenblock, in dem ein Objekt für die GPU vollständig in einem GPU-spezifischen, nicht transparenten Format beschrieben wird. Es gibt mehrere verschiedene Arten von Deskriptoren zum &mdash; Renderziel (rtvs), tiefen Schablonen Sichten (DSVs), Shader-Ressourcen Sichten (Srvs), unsortierter Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers.

Die Größe der Deskriptoren variiert abhängig von der GPU-Hardware. Sie können die Größe eines SRV, UAV oder CBV Abfragen, indem Sie [**ID3D12Device:: getdescriptorhandleincrementsize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)aufrufen. In dieser Dokumentation werden Deskriptoren als unteilbare Einheiten angezeigt. Im folgenden finden Sie ein Beispiel.

![SRV, CBV, UAV und Sampler](images/single-descriptor.png)

Deskriptoren werden von API-aufrufen erstellt und enthalten Informationen wie die Ressource und MIP-Maps, die der Deskriptor enthalten soll.

Der Treiber verfolgt keine Verweise auf Deskriptoren oder hält Verweise darauf. es liegt an der APP, sicherzustellen, dass der richtige Deskriptortyp verwendet wird und dass die Informationen aktuell sind. Es gibt eine kleine Ausnahme. der Treiber prüft renderzielbindungen, um sicherzustellen, dass Swapketten ordnungsgemäß funktionieren.

Objekt Deskriptoren müssen nicht freigegeben oder freigegeben werden. Treiber fügen keine Zuordnungen an die Erstellung eines Deskriptors an. Ein Deskriptor kann jedoch Verweise auf andere Zuordnungen codieren, für die die Anwendung die Lebensdauer besitzt. Beispielsweise muss ein Deskriptor für einen SRV die virtuelle Adresse der D3D-Ressource (z. b. eine Textur) enthalten, auf die sich der SRV bezieht. Es liegt in der Verantwortung der Anwendung, sicherzustellen, dass Sie keinen SRV-Deskriptor verwendet, wenn die zugrunde liegende D3D-Ressource, von der Sie abhängt, zerstört wurde oder geändert wird (z. b. als nicht residente deklariert).

Die primäre Methode, Deskriptoren zu verwenden, besteht darin, Sie in deskriptorheaps zu platzieren, die für Deskriptoren Arbeitsspeicher unterstützen.

## <a name="descriptor-handles"></a>Deskriptorhandles

Ein Deskriptorhandle ist die eindeutige Adresse des Deskriptors. Sie ähnelt einem-Zeiger, ist aber nicht transparent, da die Implementierung Hardware spezifisch ist. Das Handle ist über deskriptorheaps hinweg eindeutig, sodass z. b. ein Array von Handles auf Deskriptoren in mehreren Heaps verweisen kann.

CPU-Handles sind für die sofortige Verwendung vorgesehen, z. b. das Kopieren, wenn Quelle und Ziel identifiziert werden müssen. Unmittelbar nach der Verwendung (z. b. einem [**ID3D12GraphicsCommandList:: omstrendertargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)-Befehl) können Sie wieder verwendet werden, oder der zugrunde liegende Heap kann verworfen werden.

GPU-Handles dienen nicht der unmittelbaren Verwendung &mdash; , Sie identifizieren Positionen aus einer Befehlsliste, die zur GPU-Ausführungszeit verwendet werden. Sie müssen beibehalten werden, bis alle Befehlslisten, auf die verwiesen wird, vollständig ausgeführt wurden.

Zum Erstellen eines Deskriptorhandles für den Anfang eines Heaps rufen Sie nach dem Erstellen des deskriptorheaps eine der folgenden Methoden auf:

-   [**ID3D12DescriptorHeap:: getcpudescriptor Lenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap:: getgpudescriptor Lenker forheapstart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Diese Methoden geben die folgenden Strukturen zurück:

-   [**D3D12- \_ CPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**D3D12- \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

Wenn die Größe der Deskriptoren von der Hardware abweicht, verwenden Sie Folgendes, um das Inkrement zwischen den einzelnen Deskriptoren in einem Heap zu erzielen:

-   [**ID3D12Device:: getDescriptor handleinkrementsize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

Es ist sicher, eine Startposition mit einer Reihe von Schritten zu versetzen, Handles zu kopieren und Handles an API-Aufrufe zu übergeben. Es ist nicht sicher, ein Handle so zu dereferenzieren, als ob es sich um einen gültigen CPU-Zeiger handelt, oder um die Bits innerhalb eines Handles zu analysieren.

Einige Hilfsstrukturen wurden mit Initialisierungs Membern hinzugefügt, um die Verwaltung von Handles etwas zu vereinfachen.

-   [**CD3DX12- \_ CPU- \_ \_ Deskriptorhandle**](cd3dx12-cpu-descriptor-handle.md)
-   [**CD3DX12- \_ GPU- \_ \_ Deskriptorhandle**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>NULL-Deskriptoren

Beim Erstellen von Deskriptoren mithilfe von API-aufrufen übergeben Anwendungen NULL für den Ressourcen Zeiger in der deskriptordefinition, um die Auswirkung von nichts zu erreichen, wenn von einem Shader darauf zugegriffen wird.

Der restliche Deskriptor muss so weit wie möglich aufgefüllt werden. Im Fall von Shader-Ressourcen Sichten (Srvs) kann der Deskriptor beispielsweise verwendet werden, um den Ansichtstyp (Texture1D, Texture2D usw.) zu unterscheiden. Numerische Parameter im Ansichts Deskriptor (z. b. die Anzahl von Mipmaps) müssen auf Werte festgelegt werden, die für eine Ressource gültig sind.

In vielen Fällen gibt es ein definiertes Verhalten für den Zugriff auf eine nicht gebundene Ressource, wie z. b. Srvs, die Standardwerte zurückgeben. Diese werden berücksichtigt, wenn auf einen NULL-Deskriptor zugegriffen wird, solange der Shader-Zugriff mit dem Deskriptortyp kompatibel ist. Wenn ein Shader z. b. einen Texture2D SRV erwartet und auf einen NULL-SRV zugreift, der als Texture1D definiert ist, ist das Verhalten nicht definiert und könnte zum Zurücksetzen des Geräts führen.

Wenn Sie einen NULL-Deskriptor erstellen möchten, übergeben Sie `null` für den *presource* -Parameter, wenn Sie die Sicht mit Methoden wie z. b. " [**kreateshaderresourceview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)" erstellen. Legen Sie für den Ansichts Beschreibungs Parameter *pdesc* eine Konfiguration fest, die funktioniert, wenn die Ressource nicht NULL war (andernfalls tritt möglicherweise ein Absturz auf der Hardware auf).

Stamm Deskriptoren sollten jedoch nicht auf NULL festgelegt werden.

Auf Tier1-Hardware (siehe [**Hardware Stufen**](./hardware-support.md)) müssen alle Deskriptoren, die gebunden sind (über deskriptortabellen), entweder als echte Deskriptoren oder NULL-Deskriptoren initialisiert werden. Dies gilt auch, wenn die Hardware nicht darauf zugreifen kann. andernfalls ist das Verhalten nicht definiert.

Auf Instanzen-Hardware gilt dies für gebundene CBV-und UAV-Deskriptoren, jedoch nicht für SRV-Deskriptoren.

Auf Instanzen-Hardware gibt es keine Einschränkung, vorausgesetzt, dass nicht initialisierte Deskriptoren nie aufgerufen werden.

## <a name="default-descriptors"></a>Standard Deskriptoren

Wenn Sie einen Standard Deskriptor für eine bestimmte Ansicht erstellen möchten, übergeben Sie einen gültigen *presource* -Parameter an die CREATE VIEW-Methode (z. b. " [**kreateshaderresourceview**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)"), übergeben jedoch **null** für den *pdesc* -Parameter. Wenn die Ressource z. b. 14 MIPS enthielt, würde die Sicht 14 MIPS enthalten. Der Standardfall deckt die offensichtlichste Zuordnung einer Ressource zu einer Ansicht ab. Dies erfordert, dass die Ressource mit einem voll qualifizierten Format Namen (z. b. **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** anstatt **DXGI_FORMAT_R8G8B8A8_TYPELESS**) zugeordnet wird.

Standard Deskriptoren können nicht mit einer Strukturansicht der Raytracing-Beschleunigung verwendet werden, da der angegebene *presource* -Parameter **null** sein muss und der Speicherort über einen [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/Windows/Win32/API/d3d12/NS-d3d12-d3d12_raytracing_acceleration_structure_srv) übergeben werden muss.

## <a name="related-topics"></a>Verwandte Themen

[Deskriptoren](descriptors.md)