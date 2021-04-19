---
title: Getrequiredintermediatesize-Funktion (D3dx12. h)
description: Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Getrequiredintermediatesize-Funktion
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363160"
---
# <a name="getrequiredintermediatesize-function"></a>Getrequiredintermediatesize-Funktion

Gibt die erforderliche Größe eines Puffers zurück, der zum Hochladen von Daten verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdestinationresource* \[ in\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Ein Zeiger auf die [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) -Schnittstelle, die die Ziel Ressource darstellt.

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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Puffers in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

