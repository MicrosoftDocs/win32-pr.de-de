---
description: Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Prozess des Renderings in Umgebungszuordnungen zu generalisieren.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: ID3DXRenderToEnvMap-Schnittstelle (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94fc32654ca5bea81538a5dc56e7ca6b391287703a4a96dfccf62ceae497766a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095770"
---
# <a name="id3dxrendertoenvmap-interface"></a>ID3DXRenderToEnvMap-Schnittstelle

Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Prozess des Renderings in Umgebungszuordnungen zu generalisieren.

## <a name="members"></a>Member

Die **ID3DXRenderToEnvMap-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXRenderToEnvMap** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXRenderToEnvMap-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | Initiieren Sie das Rendering einer kubischen Umgebungskarte.<br/>                                                                                                                                    |
| [**BeginChemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | Initiieren Sie das Rendering einer hemispherischen Umgebungszuordnung.<br/>                                                                                                                              |
| [**BeginParaturic**](id3dxrendertoenvmap--beginparabolic.md)   | Initiieren Sie das Rendering einer parabolischen Umgebungszuordnung.<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | Initiieren Sie das Rendering einer sphärischen Umgebungszuordnung.<br/>                                                                                                                                |
| [**Ende**](id3dxrendertoenvmap--end.md)                         | Stellen Sie alle Renderziele wieder her, und erstellen Sie bei Bedarf alle gerenderten Gesichter in der Umgebungszuordnungsoberfläche.<br/>                                                                           |
| [**Gesicht**](id3dxrendertoenvmap--face.md)                       | Initiieren Sie das Zeichnen der einzelnen Gesichter einer Umgebungskarte.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Ruft die Beschreibung der Renderoberfläche ab.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Ruft das Direct3D-Gerät ab, das der Umgebungszuordnung zugeordnet ist.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Verwenden Sie diese Methode, um alle Verweise auf Videospeicherressourcen freizugeben und alle Zustandsblöcke zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder bevor ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Eine Umgebungskarte wird verwendet, um Szenengeometrie zu strukturieren, um eine anspruchsvollere Szene ohne komplexe Geometrie bereitzustellen. Diese Schnittstelle unterstützt das Erstellen von Oberflächen für die folgenden Arten von Geometrie: Cube, Halbkugel oder hemispheric, parabolisch oder kugel.

Die **ID3DXRenderToEnvMap-Schnittstelle** wird durch Aufrufen der [**D3DXCreateRenderToEnvMap-Funktion**](d3dxcreaterendertoenvmap.md) abgerufen.

Der LPD3DXRenderToEnvMap-Typ wird als Zeiger auf die **ID3DXRenderToEnvMap-Schnittstelle** definiert.


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
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

 

 
