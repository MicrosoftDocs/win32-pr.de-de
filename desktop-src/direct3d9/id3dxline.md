---
description: Die ID3DXLine-Schnittstelle implementiert die Zeilen Zeichnung mithilfe von Text Dreiecken.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: ID3DXLine-Schnittstelle (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050946"
---
# <a name="id3dxline-interface"></a>ID3DXLine-Schnittstelle

Die ID3DXLine-Schnittstelle implementiert die Zeilen Zeichnung mithilfe von Text Dreiecken.

## <a name="members"></a>Member

Die **ID3DXLine** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXLine** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXLine** -Schnittstelle verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dxline--begin.md)                     | Bereitet ein Gerät für Zeichnungs Zeilen vor.<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | Zeichnet einen Zeilen Streifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (of [**D3DXVECTOR2**](d3dxvector2.md)) im Zeilen Streifen definiert.<br/>                                   |
| [**Drawtransform**](id3dxline--drawtransform.md)     | Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.<br/>                                                                                                      |
| [**ENDE**](id3dxline--end.md)                         | Stellt den Zustand des Geräts in dem Zustand wieder her, in dem es sich beim Aufrufen von [**ID3DXLine:: begin**](id3dxline--begin.md) befand<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Ruft den Zustand der Zeilen-Antialiasing ab.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Ruft das Direct3D-Gerät ab, das dem-Zeilen Objekt zugeordnet ist.<br/>                                                                                                                        |
| [**Getgllines**](id3dxline--getgllines.md)           | Ruft den Modus im OpenGL-Stil ab.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Ruft das Zeilen stippingmuster ab.<br/>                                                                                                                                                        |
| [**Getpatternscale**](id3dxline--getpatternscale.md) | Ruft den Skalierungs Wert Stippel-Pattern ab.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Ruft die Stärke der Linie ab.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                       |
| [**Setantialias**](id3dxline--setantialias.md)       | Schaltet das Zeilen-Antialiasing um.<br/>                                                                                                                                                            |
| [**Setgllines**](id3dxline--setgllines.md)           | Schaltet den Modus um, um OpenGL-stillinien zu zeichnen.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Wendet ein stippingmuster auf die Zeile an.<br/>                                                                                                                                                |
| [**Setpatternscale**](id3dxline--setpatternscale.md) | Dehnt das Stippel Muster entlang der Zeilen Richtung aus.<br/>                                                                                                                               |
| [**"-Twidth"**](id3dxline--setwidth.md)               | Gibt die Stärke der Linie an.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie ein Zeilen Zeichnungsobjekt mit [**D3DXCreateLine**](d3dxcreateline.md).

Der LPD3DXLINE-Typ wird als Zeiger auf die **ID3DXLine** -Schnittstelle definiert.


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
