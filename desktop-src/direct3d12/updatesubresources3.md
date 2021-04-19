---
title: Updatesubresources (Stapel Zuordnung)-Funktion (D3dx12. h)
description: Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
keywords:
- Updatesubresources-Funktion
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357226"
---
# <a name="updatesubresources-stack-allocating-function"></a>Updatesubresources (Stapel Zuordnung)-Funktion

Aktualisiert unter Ressourcen mit einer Implementierung zur Stapel Zuweisung.

## <a name="syntax"></a>Syntax


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcmdlist* \[ in\]
</dt> <dd>

Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Die Befehlsliste als Zeiger auf eine [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pdestinationresource* \[ in\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die Ziel Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pintermediate* \[ in\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die zwischen Ressource als Zeiger auf eine [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*Intermediateoffset* 
</dt> <dd>

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Der Offset in Bytes der zwischen Ressource.

</dd> <dt>

*Firstsubresource* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten unter Quelle in der Ressource. Gültige Werte reichen von 0 bis *maxsubresources*.

</dd> <dt>

*Numsubresources* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der unter Ressourcen in der Ressource. Gültige Werte liegen zwischen 1 und (*maxsubresources*  -  *firstsubresource*).

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Typ: **[ **D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf D3D12-unter Berichts [**\_ \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Strukturen, die Beschreibungen der für das Update verwendeten unter Berichtsdaten enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Cookies in Bytes.

## <a name="remarks"></a>Bemerkungen

Die Deklaration dieser Funktion beginnt mit: `template <UINT MaxSubresources>`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

