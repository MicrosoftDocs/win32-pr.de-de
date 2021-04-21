---
UID: NF:directml.DMLCreateDevice1
title: DMLCreateDevice1-Funktion
description: Erstellt ein DirectML-Gerät für ein bestimmtes Direct3D 12-Gerät.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803773"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="38320-103">DMLCreateDevice1-Funktion (directml.h)</span><span class="sxs-lookup"><span data-stu-id="38320-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="38320-104">Erstellt ein DirectML-Gerät für ein bestimmtes Direct3D 12-Gerät.</span><span class="sxs-lookup"><span data-stu-id="38320-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38320-105">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="38320-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="38320-106">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="38320-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38320-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="38320-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="38320-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="38320-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="38320-109">Typ: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="38320-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="38320-110">Ein Zeiger auf eine [ID3D12Device,](/windows/win32/api/d3d12/nn-d3d12-id3d12device) die das Direct3D 12-Gerät darstellt, über das das DirectML-Gerät erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38320-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="38320-111">DirectML unterstützt alle D3D-Featureebenen und Direct3D 12-Geräte, die auf jedem Adapter erstellt werden, einschließlich WARP.</span><span class="sxs-lookup"><span data-stu-id="38320-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="38320-112">Abhängig von den Funktionen des Direct3D 12-Geräts sind jedoch möglicherweise nicht alle Features in DirectML verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38320-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="38320-113">Weitere [Informationen finden Sie unter IDMLDevice::CheckFeatureSupport.](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)</span><span class="sxs-lookup"><span data-stu-id="38320-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="38320-114">Wenn der Aufruf von **DMLCreateDevice1** erfolgreich ist, behält das DirectML-Gerät einen starken Verweis auf das angegebene Direct3D 12-Gerät bei.</span><span class="sxs-lookup"><span data-stu-id="38320-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="38320-115">Typ: <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="38320-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="38320-116">Ein [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) Wert, der zusätzliche Optionen für die Geräteerstellung ankn.)</span><span class="sxs-lookup"><span data-stu-id="38320-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="38320-117">Typ: <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="38320-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="38320-118">Ein [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) Wert, der die erforderliche Mindestunterstützung auf Featureebene an gibt.</span><span class="sxs-lookup"><span data-stu-id="38320-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="38320-119">Dieser Parameter kann für Aufrufer nützlich sein, die eine bestimmte Version von DirectML benötigen, aber möglicherweise eine ältere Version von DirectML aufrufen.</span><span class="sxs-lookup"><span data-stu-id="38320-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="38320-120">Dies kann beispielsweise der Fall sein, wenn der Benutzer Ihre Anwendung auf einer älteren Version von Windows 10.</span><span class="sxs-lookup"><span data-stu-id="38320-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="38320-121">Anwendungen, die explizit von Funktionen abhängig sind, die in einer bestimmten Featureebene eingeführt wurden, können sie als *minimumFeatureLevel angeben.*</span><span class="sxs-lookup"><span data-stu-id="38320-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="38320-122">Dadurch wird sichergestellt, **dass DMLCreateDevice1** nicht erfolgreich  ist, es sei denn, die zugrunde liegende Implementierung ist mindestens so leistungsfähig wie diese angeforderte Minimale Featureebene.</span><span class="sxs-lookup"><span data-stu-id="38320-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="38320-123">Beachten Sie, dass das  zugrunde liegende DirectML-Gerät möglicherweise eine höhere Featureebene unterstützt als das angeforderte Minimum, da dieser Parameter eine minimale Featureebene angibt.</span><span class="sxs-lookup"><span data-stu-id="38320-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="38320-124">Sobald die Geräteerstellung erfolgreich ist, können Sie alle von diesem Gerät unterstützten Featureebenen mit [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)abfragen.</span><span class="sxs-lookup"><span data-stu-id="38320-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="38320-125">Typ: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="38320-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="38320-126">Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die auf <i>dem Gerät</i>zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="38320-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="38320-127">Es wird erwartet, dass dies die GUID von [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)ist.</span><span class="sxs-lookup"><span data-stu-id="38320-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="38320-128">Typ: \_ COM \_ Outptr \_ opt \_ <b>void\*\*</b></span><span class="sxs-lookup"><span data-stu-id="38320-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="38320-129">Ein Zeiger auf einen Speicherblock, der einen Zeiger auf das Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="38320-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="38320-130">Dies ist die Adresse eines Zeigers auf einen [IDMLDevice,](/windows/win32/api/directml/nn-directml-idmldevice)der das erstellte DirectML-Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="38320-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="38320-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38320-131">Return value</span></span>

<span data-ttu-id="38320-132">Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="38320-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="38320-133">Wenn die Funktion erfolgreich ausgeführt wird, wird <b>S_OK</b>zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38320-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="38320-134">Andernfalls wird ein [HRESULT-Fehlercode](/windows/desktop/winprog/windows-data-types) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38320-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="38320-135">Wenn diese DirectML-Version das angeforderte *MinimumFeatureLevel* nicht unterstützt, gibt diese Funktion **DXGI_ERROR_UNSUPPORTED** zurück.</span><span class="sxs-lookup"><span data-stu-id="38320-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="38320-136">Das Grafiktools-Feature on Demand (FOD) muss installiert sein, um die DirectML-Debugebenen verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="38320-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="38320-137">Wenn das [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) Flag in *Flags* angegeben ist und die Debugebenen nicht installiert sind, gibt **DMLCreateDevice1** **DXGI_ERROR_SDK_COMPONENT_MISSING** zurück.</span><span class="sxs-lookup"><span data-stu-id="38320-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="38320-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38320-138">Remarks</span></span>

<span data-ttu-id="38320-139">Eine neuere Version dieser Funktion, [DMLCreateDevice1,]()wurde in DirectML Version 1.1.0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="38320-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="38320-140">**DMLCreateDevice1** entspricht dem Aufrufen von **DMLCreateDevice1** und dem Bereitstellen eines *minimumFeatureLevel* von [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="38320-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="38320-141">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="38320-141">Availability</span></span>

<span data-ttu-id="38320-142">Diese API wurde in DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="38320-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="38320-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38320-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="38320-144">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="38320-144">**Target Platform**</span></span> | <span data-ttu-id="38320-145">Windows</span><span class="sxs-lookup"><span data-stu-id="38320-145">Windows</span></span> |
| <span data-ttu-id="38320-146">**Header**</span><span class="sxs-lookup"><span data-stu-id="38320-146">**Header**</span></span> | <span data-ttu-id="38320-147">directml.h</span><span class="sxs-lookup"><span data-stu-id="38320-147">directml.h</span></span> |
| <span data-ttu-id="38320-148">**Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="38320-148">**Library**</span></span> | <span data-ttu-id="38320-149">DirectML.lib</span><span class="sxs-lookup"><span data-stu-id="38320-149">DirectML.lib</span></span> |
| <span data-ttu-id="38320-150">**Dll**</span><span class="sxs-lookup"><span data-stu-id="38320-150">**DLL**</span></span> | <span data-ttu-id="38320-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="38320-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="38320-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38320-152">See also</span></span>

* [<span data-ttu-id="38320-153">DML_FEATURE_LEVEL Enumeration</span><span class="sxs-lookup"><span data-stu-id="38320-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="38320-154">DirectML-Versionsverlauf</span><span class="sxs-lookup"><span data-stu-id="38320-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="38320-155">DirectML-Verlauf auf Featureebene</span><span class="sxs-lookup"><span data-stu-id="38320-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="38320-156">Verwenden der DirectML-Debugebene</span><span class="sxs-lookup"><span data-stu-id="38320-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)