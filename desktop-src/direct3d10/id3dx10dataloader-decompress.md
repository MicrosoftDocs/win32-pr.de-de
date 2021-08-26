---
description: Wird zum Dekomprimieren codierter Daten verwendet. In der Regel wird dies verwendet, um Ressourcen aus Dateisystemen wie ZIP-Dateien zu laden. Beim Laden aus einer nicht komprimierten Ressource muss die Dekomprimierungsphase keine Arbeit mehr tun.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader::D ecompress-Methode (D3DX10.h)
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
ms.openlocfilehash: c9e532bae8cb121fc93f3fdf2a5a1ee23e597c66599277b73b3b36b15ebbb963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989120"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader::D ecompress-Methode

Wird zum Dekomprimieren codierter Daten verwendet. In der Regel wird dies verwendet, um Ressourcen aus Dateisystemen wie ZIP-Dateien zu laden. Beim Laden aus einer nicht komprimierten Ressource muss die Dekomprimierungsphase keine Arbeit mehr tun.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Typ: **\* \* void**

Zeiger auf die zu dekomprimierenden Rohdaten.

</dd> <dt>

*pcBytes* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Die Größe der Daten, auf die ppData zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

[**Die ID3DX10DataLoader-Schnittstelle**](id3dx10dataloader.md) kann geerbt und ihre Member neu definiert werden. Dekomprimieren kann neu definiert werden, um Ihre eigenen benutzerdefinierten Dateiformate zu unterstützen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
