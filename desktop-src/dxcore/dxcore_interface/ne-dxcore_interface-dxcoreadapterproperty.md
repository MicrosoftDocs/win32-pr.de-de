---
title: 'DXCoreAdapterProperty '
description: Definiert Konstanten, die DXCore-Adapter Eigenschaften angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338470"
---
# <a name="dxcoreadapterproperty-enum"></a>Dxcoreadapterproperty-Enumeration

Definiert Konstanten, die DXCore-Adapter Eigenschaften angeben. Übergeben Sie eine dieser Konstanten an die [idxcoreadapter:: getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) -Methode, um die zum Empfangen des Werts der entsprechenden Eigenschaft erforderliche Puffergröße abzurufen. übergeben Sie dann dieselbe Konstante an die [idxcoreadapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) -Methode, um den Wert der Eigenschaft in einem Puffer abzurufen, den Sie zuordnen.

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

### <a name="instanceluid"></a>Instanceluid

Gibt die <em>instanceluid</em> -Adapter Eigenschaft an, die einen lokal eindeutigen Bezeichner enthält, der den Adapter darstellt. Dieser Wert bleibt während der Lebensdauer dieses Adapters konstant. Die LUID eines Adapters ändert sich beim Neustart, beim Treiber Upgrade oder beim Deaktivieren/Aktivieren von Geräten.

Die <em>instanceluid</em> -Adapter Eigenschaft weist den Typ <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>auf.

### <a name="driverversion"></a>DriverVersion

Gibt die Eigenschaft für den <em>DriverVersion</em> -Adapter an, die die in <b>Word</b>s als <b>LARGE_INTEGER</b>dargestellte Treiber Version enthält.

Die Eigenschaft für den <em>DriverVersion</em> -Adapter weist den Typ <b>uint64_t</b>auf, der einen booleschen Wert darstellt.

### <a name="driverdescription"></a>Driverdescription

Gibt die <em>driverdescription</em> -Adapter Eigenschaft an, die ein mit Null endendes Array von <b>char</b>s enthält, das den vom Treiber angegebenen Treiber in <a href="/windows/win32/intl/unicode">UTF-8</a> -Codierung beschreibt.

Die Eigenschaft " <em>driverdescription</em> " weist den Typ " <b>char *</b>" auf.

### <a name="hardwareid"></a>HardwareID

Gibt die <em>HardwareID</em> -Adapter Eigenschaft an, die die PnP-Hardware-ID-Teile darstellt.

Die <em>HardwareID</em> -Adapter Eigenschaft weist den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">dxcorehardwareid</a>auf.

### <a name="kmdmodelversion"></a>Kmdmodelversion

Gibt die <em>kmdmodelversion</em> -Adapter Eigenschaft an, die das Treibermodell darstellt.

Die <em>kmdmodelversion</em> -Adapter Eigenschaft weist den Typ <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>auf.

### <a name="computepreemptiongranularity"></a>Computepreemptiongranularität

Gibt die <em>computepreemptiongranularity</em> -Adapter Eigenschaft an, die die Granularität der COMPUTE-Präemption darstellt.

Die <em>computepreemptiongranularity</em> -Adapter Eigenschaft weist den Typ <b>uint16_t</b>auf, der einen <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> Wert darstellt.

### <a name="graphicspreemptiongranularity"></a>Graphicspree emptiongranularität

Gibt die <em>graphicspree emptiongranularity</em> -Adapter Eigenschaft an, die die Granularität der Grafik Präemption darstellt.

Die <em>graphicspree emptiongranularity</em> -Adapter Eigenschaft weist den Typ <b>uint16_t</b>auf, der einen <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> Wert darstellt.

### <a name="dedicatedadaptermemory"></a>Dedialisiedadaptermemory

Gibt die <em>dedialisiedadaptermemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes des dedizierten Adapter Speichers darstellt, die nicht mit der CPU gemeinsam genutzt werden.

Die <em>dedialisiedvideomemory</em> -Adapter Eigenschaft hat den Typ <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>Dedialisiedsystemmemory

Gibt die <em>dedialisiedsystemmemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes für dedizierten System Arbeitsspeicher darstellt, die nicht mit der CPU gemeinsam genutzt werden. Dieser Speicher wird aus dem verfügbaren System Arbeitsspeicher zum Zeitpunkt der Startzeit zugeordnet.

Die <em>dedialisiedsystemmemory</em> -Adapter Eigenschaft weist den Typ <b>uint64_t</b>auf.

### <a name="sharedsystemmemory"></a>Sharedsystemmemory

Gibt die <em>sharedsystemmemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes für freigegebenen System Arbeitsspeicher darstellt. Dies ist der maximale Wert des System Speichers, der vom Adapter während des Vorgangs genutzt werden kann. Zusätzlicher Speicherplatz, der vom Treiber beim Verwalten und Verwenden von Videospeicher beansprucht wird, ist zusätzlich.

Die <em>sharedsystemmemory</em> -Adapter Eigenschaft hat den Typ <b>uint64_t</b>.

### <a name="acgcompatible"></a>Acgcompatible

Gibt die <em>acgcompatible</em> -Adapter Eigenschaft an, die angibt, ob der Adapter mit Prozessen kompatibel ist, die einen beliebigen Codewächter erzwingen.

Die <em>acgcompatible</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.

### <a name="ishardware"></a>Ishardware

Gibt die <em>ishardware</em> -Adapter Eigenschaft an, die bestimmt, ob es sich um einen Hardware Adapter handelt. Ein Adapter, bei dem es sich nicht um einen Hardware Adapter handelt, ist ein Software Adapter.

Die <em>ishardware</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.

### <a name="isintegrated"></a>Isintegriert

Gibt die <em>isintegrate</em> -Adapter Eigenschaft an, die bestimmt, ob der Adapter als integrierter Grafikprozessor (igpu) gemeldet wird.

Die <em>isintegrate</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.

### <a name="isdetachable"></a>Isdetabar

Gibt die <em>isdetachable</em> -Adapter Eigenschaft an, mit der bestimmt wird, ob der Adapter als ablösbar gemeldet wurde.

Die <em>isdetachable</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.

<b>Beachten Sie</b>. Auch wenn <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">idxcoreadapter:: GetProperty</a> `false` für diese Eigenschaft angibt, kann der Adapter weiterhin als entfernt gemeldet werden, z. b. bei Fehlern oder Treiberaktualisierungen.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter:: getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [idxcoreadapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)