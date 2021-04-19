---
title: D3DX12SerializeVersionedRootSignature-Funktion (D3dx12. h)
description: Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten. Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.
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
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355162"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>D3DX12SerializeVersionedRootSignature-Funktion

Unterstützt die Aktivierung von root Signature 1,1-Features, wenn diese verfügbar sind. es ist nicht erforderlich, zwei Codepfade zum Aufbauen von Stamm Signaturen zu verwalten. Diese Hilfsmethode rekonstruiert eine Stamm Signatur der Version 1,0, wenn Version 1,1 nicht unterstützt wird.

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

*prootsignatueinlösen* \[ in\]
</dt> <dd>

Typ: **Konstanten D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC \***

Gibt eine mit [**D3D12 \_ versionierte Stamm \_ \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) an, die eine Beschreibung einer beliebigen Version einer Stamm Signatur enthält.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Type: **D3D \_ root \_ Signature \_ Version**

Gibt die maximal unterstützte D3D-Stamm [**\_ \_ Signatur \_ Version**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)an.

</dd> <dt>

*ppBlob* \[ vorgenommen\]
</dt> <dd>

Typ: **ID3DBlob \* \***

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle empfängt, mit der Sie auf die serialisierte Stamm Signatur zugreifen können.

</dd> <dt>

*pperrorblob* \[ Out, optional\]
</dt> <dd>

Typ: **ID3DBlob \* \***

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle empfängt, die Sie verwenden können, um auf Fehlermeldungen des Serialisierungsprogramms zuzugreifen, oder **null** , wenn keine Fehler vorliegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt bei Erfolg **S \_ OK** zurück; andernfalls wird einer der [Rückgabe Codes Direct3D 12 zurückgegeben](d3d12-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Bemerkungen

Diese Funktion wurde im Zusammenhang mit dem Windows 10 Anniversary Update (14393) veröffentlicht. Um Windows 10-Versionen zu unterstützen, muss für die Verwendung dieser Funktion d3d12. lib für das *verzögerte Laden* eingerichtet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

