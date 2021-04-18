---
description: Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: ID3DXMatrixStack-Schnittstelle (d3dx10. h)
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
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355637"
---
# <a name="id3dxmatrixstack-interface"></a>ID3DXMatrixStack-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.

## <a name="members"></a>Member

Die **ID3DXMatrixStack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXMatrixStack** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXMatrixStack** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Ruft die aktuelle Matrix am Anfang des Stapels ab.<br/>                                                                           |
| [**Loadidentity**](id3dxmatrixstack-loadidentity.md)                       | Lädt die Identität in der aktuellen Matrix.<br/>                                                                                           |
| [**Loadmatrix**](id3dxmatrixstack-loadmatrix.md)                           | Lädt die angegebene Matrix in die aktuelle Matrix.<br/>                                                                                 |
| [**Multmatrix**](id3dxmatrixstack-multmatrix.md)                           | Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.<br/>                                                              |
| [**Multmatrixlocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.<br/>                                                              |
| [**Chor**](id3dxmatrixstack-pop.md)                                         | Entfernt die aktuelle Matrix vom oberen Rand des Stapels.<br/>                                                                           |
| [**Push**](id3dxmatrixstack-push.md)                                       | Fügt dem Stapel eine Matrix hinzu.<br/>                                                                                                     |
| [**Rotateaxis**](id3dxmatrixstack-rotateaxis.md)                           | Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.<br/>                                                          |
| [**Rotateaxislocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.<br/>                                             |
| [**Rotateyawpitchroll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.<br/>                                                          |
| [**Rotateyawpitchrolllocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.<br/>                                             |
| [**Migen**](id3dxmatrixstack-scale.md)                                     | Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.<br/>                                                                     |
| [**Skalelocal**](id3dxmatrixstack-scalelocal.md)                           | Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.<br/>                                                                               |
| [**Übersetzen**](id3dxmatrixstack-translate.md)                             | Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.<br/> |
| [**Translatelocal**](id3dxmatrixstack-translatelocal.md)                   | Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die ID3DX10MATRIXStack-Schnittstelle wird durch Aufrufen der [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) -Funktion abgerufen.

Der LPD3DX10MATRIXSTACK-Typ wird als Zeiger auf die **ID3DXMatrixStack** -Schnittstelle definiert.


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
