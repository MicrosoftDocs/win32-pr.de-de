---
title: 'DXCoreAdapterProperty '
description: Definiert Konstanten, die DXCore-Adaptereigenschaften angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: aca9093eb85971621cf232b4713d811535619b59c3d07e0b8b490d063b9d7ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042928"
---
# <a name="dxcoreadapterproperty-enum"></a>DXCoreAdapterProperty-Enum

Definiert Konstanten, die DXCore-Adaptereigenschaften angeben. Übergeben Sie eine dieser Konstanten an die [IDXCoreAdapter::GetPropertySize-Methode,](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) um die Puffergröße abzurufen, die zum Empfangen des Werts der entsprechenden Eigenschaft erforderlich ist. Übergeben Sie dann dieselbe Konstante an die [IDXCoreAdapter::GetProperty-Methode,](./nf-dxcore_interface-idxcoreadapter-getproperty.md) um den Wert der Eigenschaft in einem Puffer abzurufen, den Sie zuordnen.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a>Konstanten

### <a name="instanceluid"></a>InstanceLuid

Gibt die <em>InstanceLuid-Adaptereigenschaft</em> an, die einen lokal eindeutigen Bezeichner enthält, der den Adapter darstellt. Dieser Wert bleibt für die Lebensdauer dieses Adapters konstant. Die LUID eines Adapters ändert sich bei Neustart, Treiberupgrade oder Gerätedeaktivierung/-aktivierung.

Die <em>InstanceLuid-Adaptereigenschaft</em> hat den Typ <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Gibt die <em>DriverVersion-Adaptereigenschaft</em> an, die die Treiberversion enthält, die in <b>WORD</b>s als <b>LARGE_INTEGER.</b>

Die <em>DriverVersion-Adaptereigenschaft</em> verfügt über den Typ <b>uint64_t</b>, der einen booleschen Wert darstellt.

### <a name="driverdescription"></a>DriverDescription

Gibt die <em>DriverDescription-Adaptereigenschaft</em> an, die ein auf NULL beendetes Array von <b>CHAR-Werten</b>enthält, die den Treiber in <a href="/windows/win32/intl/unicode">der UTF-8-Codierung</a> beschreiben, wie vom Treiber angegeben.

Die <em>DriverDescription-Adaptereigenschaft</em> hat den Typ <b>char*</b>.

### <a name="hardwareid"></a>HardwareID

Gibt die <em>HardwareID-Adaptereigenschaft</em> an, die die PnP-Hardware-ID-Teile darstellt.

Die <em>HardwareID-Adaptereigenschaft</em> hat den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Gibt die <em>KmdModelVersion-Adaptereigenschaft</em> an, die das Treibermodell darstellt.

Die <em>KmdModelVersion-Adaptereigenschaft</em> hat den Typ <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Gibt die <em>ComputePreemptionGranularity-Adaptereigenschaft</em> an, die die Computepräemptionsgranularität darstellt.

Die <em>ComputePreemptionGranularity-Adaptereigenschaft</em> verfügt über den Typ <b>uint16_t</b>, der <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">einen</a> D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY darstellt.

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Gibt die <em>GraphicsPreemptionGranularity-Adaptereigenschaft</em> an, die die Grafikpräemptionsgranularität darstellt.

Die <em>GraphicsPreemptionGranularity-Adaptereigenschaft</em> verfügt über den <b>Typ</b>uint16_t , der <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">einen</a> D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY darstellt.

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Gibt die <em>DedicatedAdapterMemory-Adaptereigenschaft</em> an, die die Anzahl der Bytes des dedizierten Adapterspeichers darstellt, die nicht für die CPU freigegeben werden.

Die <em>DedicatedVideoMemory-Adaptereigenschaft</em> hat den <b>Typ uint64_t.</b>

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Gibt die <em>DedicatedSystemMemory-Adaptereigenschaft</em> an, die die Anzahl der Bytes des dedizierten Systemspeichers darstellt, die nicht für die CPU freigegeben sind. Dieser Arbeitsspeicher wird während des Startvorgangs aus dem verfügbaren Systemspeicher zugeordnet.

Die <em>DedicatedSystemMemory-Adaptereigenschaft</em> hat den <b>Typ uint64_t.</b>

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Gibt die <em>SharedSystemMemory-Adaptereigenschaft</em> an, die die Anzahl der Bytes des freigegebenen Systemspeichers darstellt. Dies ist der maximale Wert des Systemspeichers, der während des Betriebs vom Adapter verbraucht werden kann. Jeder zufällige Arbeitsspeicher, der vom Treiber bei der Verwaltung und Verwendung des Videospeichers verbraucht wird, ist zusätzlich.

Die <em>SharedSystemMemory-Adaptereigenschaft</em> hat den <b>Typ uint64_t.</b>

### <a name="acgcompatible"></a>AcgCompatible

Gibt die <em>AcgCompatible-Adaptereigenschaft</em> an, die angibt, ob der Adapter mit Prozessen kompatibel ist, die beliebigen Codeschutz erzwingen.

Die <em>AcgCompatible-Adaptereigenschaft</em> hat den Typ <b>bool.</b>

### <a name="ishardware"></a>IsHardware

Gibt die <em>IsHardware-Adaptereigenschaft</em> an, die bestimmt, ob es sich um einen Hardwareadapter handelt. Ein Adapter, der kein Hardwareadapter ist, ist ein Softwareadapter.

Die <em>IsHardware-Adaptereigenschaft</em> hat den Typ <b>bool.</b>

### <a name="isintegrated"></a>IsIntegrated

Gibt die <em>IsIntegrated-Adaptereigenschaft</em> an, die bestimmt, ob der Adapter als integrierter Grafikprozessor (iGPU) gemeldet wird.

Die <em>IsIntegrated-Adaptereigenschaft</em> hat den Typ <b>bool.</b>

### <a name="isdetachable"></a>IsDetachable

Gibt die <em>IsDetachable-Adaptereigenschaft</em> an, die bestimmt, ob der Adapter als abtrennbar oder wechselbar gemeldet wurde.

Die <em>IsDetachable-Adaptereigenschaft</em> hat den Typ <b>bool</b>.

<b>Hinweis:</b>. Auch wenn <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> für diese Eigenschaft angibt, kann der Adapter weiterhin als entfernt gemeldet werden, z. B. bei einer Fehlfunktion oder `false` treiberaktualisierung.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore](../dxcore-enum-adapters.md) zum Aufzählen von Adaptern