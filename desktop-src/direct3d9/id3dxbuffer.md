---
description: Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet, in dem Scheitelpunkt-, Adjaz- und Materialinformationen während Gitternetzoptimierungs- und Ladevorgängen gespeichert werden.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: ID3DXBuffer-Schnittstelle (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121678"
---
# <a name="id3dxbuffer-interface"></a>ID3DXBuffer-Schnittstelle

Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet, in dem Scheitelpunkt-, Adjaz- und Materialinformationen während Gitternetzoptimierungs- und Ladevorgängen gespeichert werden. Das Pufferobjekt wird verwendet, um Daten beliebiger Länge zurückzugeben. Außerdem werden Pufferobjekte verwendet, um Objektcode und Fehlermeldungen in Methoden zurückzugeben, die Scheitelpunkt- und Pixel-Shader zusammenstellen.

## <a name="members"></a>Member

Die **ID3DXBuffer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBuffer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | Beschreibung                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Ruft einen Zeiger auf die Daten im Puffer ab.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Ruft die Gesamtgröße der Daten im Puffer ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXBuffer-Schnittstelle** wird durch Aufrufen der [**D3DXCreateBuffer-Funktion**](d3dxcreatebuffer.md) abgerufen.

Der LPD3DXBUFFER-Typ wird als Zeiger auf die **ID3DXBuffer-Schnittstelle** definiert.


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
