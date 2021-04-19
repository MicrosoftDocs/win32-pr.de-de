---
description: Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet und speichert Vertex-, Informations-und Material Informationen während der Mesh-Optimierung und-Ladevorgänge.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: ID3DXBuffer-Schnittstelle (D3DX9Mesh. h)
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
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355810"
---
# <a name="id3dxbuffer-interface"></a>ID3DXBuffer-Schnittstelle

Die ID3DXBuffer-Schnittstelle wird als Datenpuffer verwendet und speichert Vertex-, Informations-und Material Informationen während der Mesh-Optimierung und-Ladevorgänge. Das Buffer-Objekt wird verwendet, um beliebige Längen Daten zurückzugeben. Außerdem werden Puffer Objekte zum Zurückgeben von Objektcode und Fehlermeldungen in Methoden verwendet, die Scheitelpunkt-und Pixel-Shader zusammenstellen.

## <a name="members"></a>Member

Die **ID3DXBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXBuffer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXBuffer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**Getbufferpointer**](id3dxbuffer--getbufferpointer.md) | Ruft einen Zeiger auf die Daten im Puffer ab.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Ruft die Gesamtgröße der Daten im Puffer ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **ID3DXBuffer** -Schnittstelle wird durch Aufrufen der [**D3DXCreateBuffer**](d3dxcreatebuffer.md) -Funktion abgerufen.

Der LPD3DXBUFFER-Typ wird als Zeiger auf die **ID3DXBuffer** -Schnittstelle definiert.


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
