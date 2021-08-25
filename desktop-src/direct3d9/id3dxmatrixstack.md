---
description: 'ID3DXMATRIXStack-Schnittstelle: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.'
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: ID3DXMATRIXStack-Schnittstelle (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8fa483be72d29cc869b2bd468cff25033a80187bef69317af4894fc05b096dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856450"
---
# <a name="id3dxmatrixstack-interface"></a>ID3DXMATRIXStack-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.

## <a name="members"></a>Member

Die **ID3DXMATRIXStack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMATRIXStack** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXMATRIXStack-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Ruft die aktuelle Matrix am oberen Rand des Stapels ab.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack--loadidentity.md)                       | Lädt die Identität in der aktuellen Matrix.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack--loadmatrix.md)                           | Lädt die angegebene Matrix in die aktuelle Matrix.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.<br/>                                                              |
| [**Pop**](id3dxmatrixstack--pop.md)                                         | Entfernt die aktuelle Matrix vom oberen Rand des Stapels.<br/>                                                                           |
| [**Drücken**](id3dxmatrixstack--push.md)                                       | Fügt dem Stapel eine Matrix hinzu.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.<br/>                                             |
| [**Skalieren**](id3dxmatrixstack--scale.md)                                     | Skalieren Sie die aktuelle Matrix über den Ursprung der Weltkoordinaten.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | Skalieren Sie die aktuelle Matrix über den Objektursprung.<br/>                                                                               |
| [**Übersetzen**](id3dxmatrixstack--translate.md)                             | Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **ID3DXMATRIXStack-Schnittstelle** wird durch Aufrufen der [**D3DXCreateMatrixStack-Funktion**](d3dxcreatematrixstack.md) abgerufen.

Der LPD3DXMATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMATRIXStack-Schnittstelle** definiert.


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
