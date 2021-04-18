---
UID: NF:directml.DMLCreateDevice1
title: DMLCreateDevice1-Funktion
description: Erstellt ein directml-Gerät für ein bestimmtes Direct3D 12-Gerät.
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
ms.openlocfilehash: f40c7e6aa82644b67303bc60f6a8b41fa08c6f8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106354893"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>DMLCreateDevice1-Funktion (directml. h)

Erstellt ein directml-Gerät für ein bestimmtes Direct3D 12-Gerät.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Parameter

`d3d12Device`

Typ: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Ein Zeiger auf ein [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) -Objekt, das das Direct3D 12-Gerät darstellt, über das das directml-Gerät erstellt wird. Directml unterstützt alle D3D Featureebene und Direct3D 12-Geräte, die auf einem beliebigen Adapter erstellt werden, einschließlich Warp. Abhängig von den Funktionen des Direct3D 12-Geräts sind jedoch möglicherweise nicht alle Features in der directml verfügbar. Weitere Informationen finden Sie [unter idmldevice:: checkfeaturesupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) .

Wenn der **DMLCreateDevice1** -Aufrufvorgang erfolgreich ist, behält das directml-Gerät einen starken Verweis auf das angegebene Direct3D 12-Gerät bei.

`flags`

Typ: <b>DML_CREATE_DEVICE_FLAGS</b>

Ein [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) Wert, der zusätzliche Geräte Erstellungs Optionen angibt.

`minimumFeatureLevel`

Typ: <b>DML_FEATURE_LEVEL</b>

Ein [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) Wert, der die minimale Unterstützung für die Featureebene angibt.

Dieser Parameter kann für Aufrufer nützlich sein, die eine bestimmte Version von directml benötigen, die jedoch möglicherweise eine ältere Version von directml aufrufen. Dies kann z. b. der Fall sein, wenn der Benutzer die Anwendung auf einer älteren Version von Windows 10 ausführt.

Anwendungen, die explizit von der Funktionalität abhängig sind, die auf einer bestimmten Featureebene eingeführt wurde, können Sie als *minimumfeaturelevel* angeben. Dadurch wird sichergestellt, dass **DMLCreateDevice1** nicht erfolgreich ist, es sei denn, die zugrunde liegende Implementierung *ist mindestens so* fähig wie die angeforderte minimale Funktionsebene.

Beachten Sie, dass das zugrunde liegende directml-Gerät tatsächlich eine höhere Funktionsebene als das angeforderte Mindestwert unterstützen kann, da dieser Parameter eine *minimale* Funktionsebene angibt. Nachdem die Geräte Erstellung erfolgreich war, können Sie alle featureebenen Abfragen, die von diesem Gerät unterstützt werden. verwenden Sie dazu [idmldevice:: checkfeaturesupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Typ: <b>refID</b>

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die im <i>Gerät</i>zurückgegeben werden soll. Dies wird als GUID von [idmldevice](/windows/win32/api/directml/nn-directml-idmldevice)erwartet.

`ppv`

Typ: \_ com \_ outptr \_ opt \_ <b>void * *</b>

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf das Gerät empfängt. Dies ist die Adresse eines Zeigers auf ein [idmldevice](/windows/win32/api/directml/nn-directml-idmldevice), das das erstellte directml-Gerät darstellt.


## <a name="return-value"></a>Rückgabewert

Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Wenn die Funktion erfolgreich ausgeführt wird, wird <b>S_OK</b>zurückgegeben. Andernfalls wird ein [HRESULT](/windows/desktop/winprog/windows-data-types) -Fehlercode zurückgegeben.

Wenn diese Version von directml die angeforderte *minimumfeaturelevel* nicht unterstützt, gibt diese Funktion **DXGI_ERROR_UNSUPPORTED** zurück.

Die Grafik Tools Feature on Demand (FOD) muss installiert sein, um die directml-debugschichten verwenden zu können. Wenn das [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) -Flag in *Flags* angegeben ist und die debugschichten nicht installiert sind, gibt **DMLCreateDevice1** **DXGI_ERROR_SDK_COMPONENT_MISSING** zurück.

## <a name="remarks"></a>Bemerkungen

Eine neuere Version dieser Funktion, [DMLCreateDevice1](), wurde in directml, Version 1.1.0, eingeführt. **DMLCreateDevice1** entspricht dem Aufrufen von **DMLCreateDevice1** und der Bereitstellung eines *minimumfeaturelevel* [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der directml-Version eingeführt `1.1.0` .

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml. h |
| **Bibliothek** | Directml. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Siehe auch

* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [DirectML-Versionsverlauf](../dml-version-history.md)
* [DirectML-Verlauf auf Featureebene](/windows/win32/direct3d12/dml-feature_level-history)    
* [Verwenden der directml-debugschicht](../dml-debug-layer.md)