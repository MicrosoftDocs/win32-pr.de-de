---
description: 'ID3DXMatrixStack-Schnittstelle: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.'
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: ID3DXMatrixStack-Schnittstelle (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65e9a5cd041431e1939346fec79dcf94fccd4ae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094408"
---
# <a name="id3dxmatrixstack-interface"></a>ID3DXMatrixStack-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.

## <a name="members"></a>Member

Die **ID3DXMatrixStack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMatrixStack** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXMatrixStack-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Ruft die aktuelle Matrix am anfang des Stapels ab.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack-loadidentity.md)                       | Lädt die Identität in der aktuellen Matrix.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack-loadmatrix.md)                           | Lädt die gegebene Matrix in die aktuelle Matrix.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack-multmatrix.md)                           | Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.<br/>                                                              |
| [**Pop**](id3dxmatrixstack-pop.md)                                         | Entfernt die aktuelle Matrix vom anfang des Stapels.<br/>                                                                           |
| [**Drücken**](id3dxmatrixstack-push.md)                                       | Fügt dem Stapel eine Matrix hinzu.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack-rotateaxis.md)                           | Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.<br/>                                             |
| [**Skalieren**](id3dxmatrixstack-scale.md)                                     | Skalieren Sie die aktuelle Matrix über den Ursprung der Weltkoordinaten.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack-scalelocal.md)                           | Skalieren Sie die aktuelle Matrix über den Objektursprung.<br/>                                                                               |
| [**Übersetzen**](id3dxmatrixstack-translate.md)                             | Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.<br/> |
| [**TranslateLocal**](id3dxmatrixstack-translatelocal.md)                   | Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DX10MATRIXStack-Schnittstelle wird durch Aufrufen der [**D3DXCreateMatrixStack-Funktion**](d3d10-d3dxcreatematrixstack.md) abgerufen.

Der LPD3DX10MATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMatrixStack-Schnittstelle** definiert.


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
