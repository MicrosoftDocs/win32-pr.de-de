---
title: UpdateSubresources-Funktion (D3dx12.h)
description: Aktualisiert Unterressourcen. Alle Unterressourcenarrays sollten aufgefüllt werden, in der Regel durch Aufrufen von ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- UpdateSubresources-Funktion
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
ms.openlocfilehash: bb1e48f4bc574d0b032b878c19c7749f63f86aba21a659c1c0a8f6f526f5bce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496600"
---
# <a name="updatesubresources-function"></a>UpdateSubresources-Funktion

Aktualisiert Unterressourcen. Alle Unterressourcenarrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Syntax


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCmdList* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Die Befehlsliste als Zeiger auf eine [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

</dd> <dt>

*pDestinationResource* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die Zielressource als Zeiger auf eine [**ID3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*pIntermediate* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die Zwischenressource als Zeiger auf eine [**ID3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*FirstSubresource* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten Unterressource in der Ressource. Der Bereich gültiger Werte ist 0 bis D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Unterressourcen in der Ressource. Der Bereich gültiger Werte ist 0 bis (D3D12 \_ REQ \_ SUBRESOURCES – *FirstSubresource*).

</dd> <dt>

*RequiredSize* 
</dt> <dd>

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die erforderliche Größe für das Update in Bytes.

</dd> <dt>

*pLayouts* \[ In\]
</dt> <dd>

Typ: **const [**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \***

Zeiger auf ein Array (mit der Länge *NumSubresources)* von Zeigern auf die Strukturen, die die Beschreibung und Platzierung der Unterressourcen der Ressource enthalten.

</dd> <dt>

*pNumRows* \[ In\]
</dt> <dd>

Typ: **const [**UINT**](/windows/desktop/WinProg/windows-data-types) \***

Zeiger auf ein Array *(numSubresources* der Länge ) von UINTS, das die Anzahl der Zeilen für jede Unterressource enthält.

</dd> <dt>

*pRowSizesInBytes* \[ In\]
</dt> <dd>

Typ: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Zeiger auf ein Array *(numSubresources* der Länge ) von UINTS, das die Größe jeder Zeile in Bytes enthält.

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Zeiger auf ein Array (mit der Länge *NumSubresources)* von Zeigern auf [**D3D12 \_ SUBRESOURCE \_ DATA-Strukturen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) mit Beschreibungen der für das Update verwendeten Unterressourcendaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Cookies in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

