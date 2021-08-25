---
title: D3DX12SerializeVersionedRootSignature-Funktion (D3dx12.h)
description: Unterstützt die Aktivierung von Stammsignatur 1.1-Features, wenn diese verfügbar sind, und erfordert keine Verwaltung von zwei Codepfaden zum Erstellen von Stammsignaturen. Diese Hilfsmethode rekonstruiert eine Stammsignatur der Version 1.0, wenn Version 1.1 nicht unterstützt wird.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature-Funktion
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f69e3bf66bcbad61e3d9bf676038f27511f756d7a3a473be2c513553862eb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851154"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>D3DX12SerializeVersionedRootSignature-Funktion

Unterstützt die Aktivierung von Stammsignatur 1.1-Features, wenn diese verfügbar sind, und erfordert keine Verwaltung von zwei Codepfaden zum Erstellen von Stammsignaturen. Diese Hilfsmethode rekonstruiert eine Stammsignatur der Version 1.0, wenn Version 1.1 nicht unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRootSignatureDesc* \[ In\]
</dt> <dd>

Typ: **const D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC \***

Gibt einen [**D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) an, der eine Beschreibung einer beliebigen Version einer Stammsignatur enthält.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Typ: **\_ D3D-STAMMSIGNATURVERSION \_ \_**

Gibt die maximal unterstützte [**D3D-STAMMSIGNATURVERSION \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)an.

</dd> <dt>

*ppBlob* \[ out\]
</dt> <dd>

Typ: **\* \* ID3DBlob**

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob-Schnittstelle**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) empfängt, mit der Sie auf die serialisierte Stammsignatur zugreifen können.

</dd> <dt>

*ppErrorBlob* \[ out, optional\]
</dt> <dd>

Typ: **\* \* ID3DBlob**

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob-Schnittstelle**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) empfängt, die Sie für den Zugriff auf Serialisierungsfehlermeldungen verwenden können, oder **NULL,** wenn keine Fehler vorliegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt **S \_ OK** zurück, wenn erfolgreich. Andernfalls wird einer der [Direct3D 12-Rückgabecodes zurückgegeben.](d3d12-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Diese Funktion wurde zusammen mit dem Windows 10 Anniversary Update (14393) veröffentlicht. Um Windows 10 Versionen vor diesem zu unterstützen, erfordert die Verwendung dieser Funktion, dass d3d12.lib für *das verzögerte Laden* von eingerichtet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

