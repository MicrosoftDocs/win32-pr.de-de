---
description: Wird verwendet, um codierte Daten zu decodieren. Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet. Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader::D eComPress-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373518"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader::D eComPress-Methode

Wird verwendet, um codierte Daten zu decodieren. Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet. Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Zeiger auf die zu entkomprimierenden Rohdaten.

</dd> <dt>

*pcbytes* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***

Die Größe der Daten, auf die von ppData verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Die [**ID3DX10DataLoader-Schnittstelle**](id3dx10dataloader.md) kann geerbt und deren Member neu definiert werden. DECOMPRESS konnte neu definiert werden, um Ihre eigenen benutzerdefinierten Dateiformate zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
