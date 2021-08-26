---
description: Die ID3DXLine-Schnittstelle implementiert die Linienzeichnung mithilfe von strukturierten Dreiecken.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: ID3DXLine-Schnittstelle (D3dx9core.h)
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
ms.openlocfilehash: a9677ca802a800624b374212c6942ab6676423f8d63e62cbf136a8b9e69c533d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951370"
---
# <a name="id3dxline-interface"></a>ID3DXLine-Schnittstelle

Die ID3DXLine-Schnittstelle implementiert die Linienzeichnung mithilfe von strukturierten Dreiecken.

## <a name="members"></a>Member

Die **ID3DXLine-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLine** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXLine-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Starten**](id3dxline--begin.md)                     | Bereitet ein Gerät für das Zeichnen von Linien vor.<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | Zeichnet einen Linienstreifen im Bildschirmbereich. Die Eingabe hat die Form eines Arrays, das Punkte [**(von D3DXVECTOR2)**](d3dxvector2.md)auf dem Linienstreifen definiert.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Zeichnet einen Linienstreifen im Bildschirmbereich mit einer angegebenen Eingabetransformationsmatrix.<br/>                                                                                                      |
| [**Ende**](id3dxline--end.md)                         | Stellt den Gerätezustand wieder in dem Zustand wieder auf, in dem [**ID3DXLine::Begin**](id3dxline--begin.md) aufgerufen wurde.<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Ruft den Antialiasingzustand der Zeile ab.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Ruft das Direct3D-Gerät ab, das dem Zeilenobjekt zugeordnet ist.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Ruft den Linienzeichnungsmodus im OpenGL-Stil ab.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Ruft das Zeilenausschnittmuster ab.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Ruft den Skalierungswert des Ausschnittmusters ab.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Ruft die Linienstärke ab.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen frei zu geben und alle Zustandsblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurücksetzungen.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Umschaltet Zeilen-Antialiasing.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Umschaltet den Modus, um Linien im OpenGL-Stil zu zeichnen.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Wendet ein Ausschnittmuster auf die Zeile an.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Streckt das Ausschnittmuster entlang der Linienrichtung.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Gibt die Linienstärke an.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Hinweise

Erstellen Sie mit [**D3DXCreateLine ein Linienzeichnungsobjekt.**](d3dxcreateline.md)

Der LPD3DXLINE-Typ wird als Zeiger auf die **ID3DXLine-Schnittstelle** definiert.


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
