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
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="97886-103">Dxcoreadapterproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="97886-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="97886-104">Definiert Konstanten, die DXCore-Adapter Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="97886-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="97886-105">Übergeben Sie eine dieser Konstanten an die [idxcoreadapter:: getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) -Methode, um die zum Empfangen des Werts der entsprechenden Eigenschaft erforderliche Puffergröße abzurufen. übergeben Sie dann dieselbe Konstante an die [idxcoreadapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) -Methode, um den Wert der Eigenschaft in einem Puffer abzurufen, den Sie zuordnen.</span><span class="sxs-lookup"><span data-stu-id="97886-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="97886-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="97886-106">Syntax</span></span>

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

## <a name="constants"></a><span data-ttu-id="97886-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="97886-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="97886-108">Instanceluid</span><span class="sxs-lookup"><span data-stu-id="97886-108">InstanceLuid</span></span>

<span data-ttu-id="97886-109">Gibt die <em>instanceluid</em> -Adapter Eigenschaft an, die einen lokal eindeutigen Bezeichner enthält, der den Adapter darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="97886-110">Dieser Wert bleibt während der Lebensdauer dieses Adapters konstant.</span><span class="sxs-lookup"><span data-stu-id="97886-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="97886-111">Die LUID eines Adapters ändert sich beim Neustart, beim Treiber Upgrade oder beim Deaktivieren/Aktivieren von Geräten.</span><span class="sxs-lookup"><span data-stu-id="97886-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="97886-112">Die <em>instanceluid</em> -Adapter Eigenschaft weist den Typ <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>auf.</span><span class="sxs-lookup"><span data-stu-id="97886-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="97886-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="97886-113">DriverVersion</span></span>

<span data-ttu-id="97886-114">Gibt die Eigenschaft für den <em>DriverVersion</em> -Adapter an, die die in <b>Word</b>s als <b>LARGE_INTEGER</b>dargestellte Treiber Version enthält.</span><span class="sxs-lookup"><span data-stu-id="97886-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="97886-115">Die Eigenschaft für den <em>DriverVersion</em> -Adapter weist den Typ <b>uint64_t</b>auf, der einen booleschen Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="97886-116">Driverdescription</span><span class="sxs-lookup"><span data-stu-id="97886-116">DriverDescription</span></span>

<span data-ttu-id="97886-117">Gibt die <em>driverdescription</em> -Adapter Eigenschaft an, die ein mit Null endendes Array von <b>char</b>s enthält, das den vom Treiber angegebenen Treiber in <a href="/windows/win32/intl/unicode">UTF-8</a> -Codierung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="97886-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="97886-118">Die Eigenschaft " <em>driverdescription</em> " weist den Typ " <b>char \*</b>" auf.</span><span class="sxs-lookup"><span data-stu-id="97886-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="97886-119">HardwareID</span><span class="sxs-lookup"><span data-stu-id="97886-119">HardwareID</span></span>

<span data-ttu-id="97886-120">Gibt die <em>HardwareID</em> -Adapter Eigenschaft an, die die PnP-Hardware-ID-Teile darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="97886-121">Die <em>HardwareID</em> -Adapter Eigenschaft weist den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">dxcorehardwareid</a>auf.</span><span class="sxs-lookup"><span data-stu-id="97886-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="97886-122">Kmdmodelversion</span><span class="sxs-lookup"><span data-stu-id="97886-122">KmdModelVersion</span></span>

<span data-ttu-id="97886-123">Gibt die <em>kmdmodelversion</em> -Adapter Eigenschaft an, die das Treibermodell darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="97886-124">Die <em>kmdmodelversion</em> -Adapter Eigenschaft weist den Typ <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>auf.</span><span class="sxs-lookup"><span data-stu-id="97886-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="97886-125">Computepreemptiongranularität</span><span class="sxs-lookup"><span data-stu-id="97886-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="97886-126">Gibt die <em>computepreemptiongranularity</em> -Adapter Eigenschaft an, die die Granularität der COMPUTE-Präemption darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="97886-127">Die <em>computepreemptiongranularity</em> -Adapter Eigenschaft weist den Typ <b>uint16_t</b>auf, der einen <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="97886-128">Graphicspree emptiongranularität</span><span class="sxs-lookup"><span data-stu-id="97886-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="97886-129">Gibt die <em>graphicspree emptiongranularity</em> -Adapter Eigenschaft an, die die Granularität der Grafik Präemption darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="97886-130">Die <em>graphicspree emptiongranularity</em> -Adapter Eigenschaft weist den Typ <b>uint16_t</b>auf, der einen <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="97886-131">Dedialisiedadaptermemory</span><span class="sxs-lookup"><span data-stu-id="97886-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="97886-132">Gibt die <em>dedialisiedadaptermemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes des dedizierten Adapter Speichers darstellt, die nicht mit der CPU gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="97886-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="97886-133">Die <em>dedialisiedvideomemory</em> -Adapter Eigenschaft hat den Typ <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="97886-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="97886-134">Dedialisiedsystemmemory</span><span class="sxs-lookup"><span data-stu-id="97886-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="97886-135">Gibt die <em>dedialisiedsystemmemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes für dedizierten System Arbeitsspeicher darstellt, die nicht mit der CPU gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="97886-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="97886-136">Dieser Speicher wird aus dem verfügbaren System Arbeitsspeicher zum Zeitpunkt der Startzeit zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="97886-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="97886-137">Die <em>dedialisiedsystemmemory</em> -Adapter Eigenschaft weist den Typ <b>uint64_t</b>auf.</span><span class="sxs-lookup"><span data-stu-id="97886-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="97886-138">Sharedsystemmemory</span><span class="sxs-lookup"><span data-stu-id="97886-138">SharedSystemMemory</span></span>

<span data-ttu-id="97886-139">Gibt die <em>sharedsystemmemory</em> -Adapter Eigenschaft an, die die Anzahl von Bytes für freigegebenen System Arbeitsspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="97886-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="97886-140">Dies ist der maximale Wert des System Speichers, der vom Adapter während des Vorgangs genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="97886-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="97886-141">Zusätzlicher Speicherplatz, der vom Treiber beim Verwalten und Verwenden von Videospeicher beansprucht wird, ist zusätzlich.</span><span class="sxs-lookup"><span data-stu-id="97886-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="97886-142">Die <em>sharedsystemmemory</em> -Adapter Eigenschaft hat den Typ <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="97886-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="97886-143">Acgcompatible</span><span class="sxs-lookup"><span data-stu-id="97886-143">AcgCompatible</span></span>

<span data-ttu-id="97886-144">Gibt die <em>acgcompatible</em> -Adapter Eigenschaft an, die angibt, ob der Adapter mit Prozessen kompatibel ist, die einen beliebigen Codewächter erzwingen.</span><span class="sxs-lookup"><span data-stu-id="97886-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="97886-145">Die <em>acgcompatible</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.</span><span class="sxs-lookup"><span data-stu-id="97886-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="97886-146">Ishardware</span><span class="sxs-lookup"><span data-stu-id="97886-146">IsHardware</span></span>

<span data-ttu-id="97886-147">Gibt die <em>ishardware</em> -Adapter Eigenschaft an, die bestimmt, ob es sich um einen Hardware Adapter handelt.</span><span class="sxs-lookup"><span data-stu-id="97886-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="97886-148">Ein Adapter, bei dem es sich nicht um einen Hardware Adapter handelt, ist ein Software Adapter.</span><span class="sxs-lookup"><span data-stu-id="97886-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="97886-149">Die <em>ishardware</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.</span><span class="sxs-lookup"><span data-stu-id="97886-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="97886-150">Isintegriert</span><span class="sxs-lookup"><span data-stu-id="97886-150">IsIntegrated</span></span>

<span data-ttu-id="97886-151">Gibt die <em>isintegrate</em> -Adapter Eigenschaft an, die bestimmt, ob der Adapter als integrierter Grafikprozessor (igpu) gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="97886-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="97886-152">Die <em>isintegrate</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.</span><span class="sxs-lookup"><span data-stu-id="97886-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="97886-153">Isdetabar</span><span class="sxs-lookup"><span data-stu-id="97886-153">IsDetachable</span></span>

<span data-ttu-id="97886-154">Gibt die <em>isdetachable</em> -Adapter Eigenschaft an, mit der bestimmt wird, ob der Adapter als ablösbar gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="97886-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="97886-155">Die <em>isdetachable</em> -Adapter Eigenschaft weist den Typ " <b>bool</b>" auf.</span><span class="sxs-lookup"><span data-stu-id="97886-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="97886-156"><b>Beachten Sie</b>.</span><span class="sxs-lookup"><span data-stu-id="97886-156"><b>Note</b>.</span></span> <span data-ttu-id="97886-157">Auch wenn <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">idxcoreadapter:: GetProperty</a> `false` für diese Eigenschaft angibt, kann der Adapter weiterhin als entfernt gemeldet werden, z. b. bei Fehlern oder Treiberaktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="97886-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="97886-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97886-158">See also</span></span>

<span data-ttu-id="97886-159">[Idxcoreadapter:: getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [idxcoreadapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="97886-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>