---
title: Updatesubresources-Funktion (D3dx12. h)
description: Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von ID3D12Device getcopyablefootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369332"
---
# <a name="updatesubresources-function"></a>Updatesubresources-Funktion

Aktualisiert unter Berichte, alle unter Quell Arrays sollten aufgefüllt werden, in der Regel durch Aufrufen von [**ID3D12Device:: getcopyablefootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

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

*Firstsubresource* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten unter Quelle in der Ressource. Der Bereich gültiger Werte ist 0 bis D3D12 \_ req \_ subresources.

</dd> <dt>

*Numsubresources* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der unter Ressourcen in der Ressource. Der Bereich gültiger Werte ist 0 bis (D3D12 \_ req \_ subresources- *firstsubresource*).

</dd> <dt>

*Requirements-size* 
</dt> <dd>

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die erforderliche Größe (in Bytes) für das Update.

</dd> <dt>

*playouts* \[ in\]
</dt> <dd>

Typ: Konstante **[**D3D12 \_ Platzierung \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) der untergeordneten Quelle \***

Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf die Strukturen, die die Beschreibung und Platzierung der unter Ressourcen der Ressource enthalten.

</dd> <dt>

*pnumrows* \[ in\]
</dt> <dd>

Typ: Konstante **[**uint**](/windows/desktop/WinProg/windows-data-types) \***

Zeiger auf ein Array (der Länge *numsubresources*) von uints, das die Anzahl der Zeilen für die einzelnen unter Berichte enthält.

</dd> <dt>

*prowsizesinbytes* \[ in\]
</dt> <dd>

Typ: **Konstanten [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Zeiger auf ein Array (der Länge *numsubresources*) von uints, das die Größe (in Bytes) der einzelnen Zeilen enthält.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Zeiger auf ein Array (der Länge *numsubresources*) von Zeigern auf D3D12-unter Berichts [**\_ \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Strukturen, die Beschreibungen der für das Update verwendeten unter Berichtsdaten enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Cookies in Bytes.

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

 

