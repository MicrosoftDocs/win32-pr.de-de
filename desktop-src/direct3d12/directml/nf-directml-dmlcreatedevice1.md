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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417182"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>DMLCreateDevice1-Funktion (directml.h)

Erstellt ein DirectML-Gerät für ein bestimmtes Direct3D 12-Gerät.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Ein Zeiger auf eine [ID3D12Device,](/windows/win32/api/d3d12/nn-d3d12-id3d12device) die das Direct3D 12-Gerät darstellt, über das das DirectML-Gerät erstellt werden soll. DirectML unterstützt alle D3D-Featureebenen und Direct3D 12-Geräte, die auf einem beliebigen Adapter erstellt wurden, einschließlich WARP. Allerdings sind möglicherweise nicht alle Features in DirectML abhängig von den Funktionen des Direct3D 12-Geräts verfügbar. Weitere Informationen finden Sie unter [IDMLDevice::CheckFeatureSupport.](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)

Wenn der Aufruf von **DMLCreateDevice1** erfolgreich ist, behält das DirectML-Gerät einen starken Verweis auf das bereitgestellte Direct3D 12-Gerät bei.

`flags`

Typ: <b>DML_CREATE_DEVICE_FLAGS</b>

Ein [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) Wert, der zusätzliche Optionen für die Geräteerstellung angibt.

`minimumFeatureLevel`

Typ: <b>DML_FEATURE_LEVEL</b>

Ein [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) Wert, der die erforderliche Mindestunterstützung auf Featureebene angibt.

Dieser Parameter kann für Aufrufer nützlich sein, die eine bestimmte Version von DirectML benötigen, aber möglicherweise eine ältere Version von DirectML aufrufen. Dies kann beispielsweise passieren, wenn der Benutzer Ihre Anwendung auf einer älteren Version von Windows 10 ausführt.

Anwendungen, die explizit von Funktionen abhängig sind, die in einer bestimmten Featureebene eingeführt wurden, können sie als *minimumFeatureLevel* angeben. Dadurch wird sichergestellt, dass **DMLCreateDevice1** nicht erfolgreich ist, es sei denn, die zugrunde liegende Implementierung ist *mindestens* so fähig wie diese angeforderte Mindestfunktionsebene.

Beachten Sie, dass das zugrunde liegende DirectML-Gerät möglicherweise eine höhere Featureebene als das angeforderte Minimum unterstützt, da dieser Parameter eine *Mindestfunktionsebene* angibt. Sobald die Geräteerstellung erfolgreich ist, können Sie alle von diesem Gerät unterstützten Featureebenen mit [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)abfragen.

`riid`

Typ: <b>REFIID</b>

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die auf <i>dem Gerät</i>zurückgegeben werden soll. Es wird erwartet, dass dies die GUID von [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)ist.

`ppv`

Typ: \_ COM \_ Outptr \_ opt \_ <b>void**</b>

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf das Gerät empfängt. Dies ist die Adresse eines Zeigers auf einen [IDMLDevice,](/windows/win32/api/directml/nn-directml-idmldevice)der das erstellte DirectML-Gerät darstellt.


## <a name="return-value"></a>Rückgabewert

Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Wenn die Funktion erfolgreich ist, wird <b>S_OK</b>zurückgegeben. Andernfalls wird ein [HRESULT-Fehlercode](/windows/desktop/winprog/windows-data-types) zurückgegeben.

Wenn diese DirectML-Version das angeforderte *MinimumFeatureLevel* nicht unterstützt, gibt diese Funktion **DXGI_ERROR_UNSUPPORTED** zurück.

Das Grafiktools-Feature on Demand (FOD) muss installiert sein, um die DirectML-Debugebenen verwenden zu können. Wenn das [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) Flag in *Flags* angegeben ist und die Debugebenen nicht installiert sind, gibt **DMLCreateDevice1** **DXGI_ERROR_SDK_COMPONENT_MISSING** zurück.

## <a name="remarks"></a>Hinweise

Eine neuere Version dieser Funktion, [DMLCreateDevice1,]()wurde in DirectML Version 1.1.0 eingeführt. **DMLCreateDevice1** entspricht dem Aufrufen von **DMLCreateDevice1** und dem Bereitstellen eines *minimumFeatureLevel-Werts* [von DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Verfügbarkeit

Diese API wurde in der DirectML-Version `1.1.0` eingeführt.

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml.h |
| **Bibliothek** | DirectML.lib |
| **Dll** | DirectML.dll |

## <a name="see-also"></a>Siehe auch

* [DML_FEATURE_LEVEL-Enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [DirectML-Versionsverlauf](../dml-version-history.md)
* [DirectML-Verlauf auf Featureebene](/windows/win32/direct3d12/dml-feature_level-history)    
* [Verwenden der DirectML-Debugebene](../dml-debug-layer.md)