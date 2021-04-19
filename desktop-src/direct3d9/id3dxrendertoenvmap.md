---
description: Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Renderingvorgang in Umgebungs Zuordnungen zu generalisieren.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: ID3DXRenderToEnvMap-Schnittstelle (D3dx9core. h)
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
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369330"
---
# <a name="id3dxrendertoenvmap-interface"></a>ID3DXRenderToEnvMap-Schnittstelle

Die ID3DXRenderToEnvMap-Schnittstelle wird verwendet, um den Renderingvorgang in Umgebungs Zuordnungen zu generalisieren.

## <a name="members"></a>Member

Die **ID3DXRenderToEnvMap** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXRenderToEnvMap** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXRenderToEnvMap** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Begincube**](id3dxrendertoenvmap--begincube.md)             | Initiieren Sie das Rendering einer kubischen Umgebungs Zuordnung.<br/>                                                                                                                                    |
| [**Beginhemisphäre**](id3dxrendertoenvmap--beginhemisphere.md) | Initiieren Sie das Rendering einer Hemispheric-Umgebungs Zuordnung.<br/>                                                                                                                              |
| [**Beginparser**](id3dxrendertoenvmap--beginparabolic.md)   | Initiieren des Renderings einer paramegigramm-Umgebungs Zuordnung.<br/>                                                                                                                                |
| [**Beginsphere**](id3dxrendertoenvmap--beginsphere.md)         | Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.<br/>                                                                                                                                |
| [**ENDE**](id3dxrendertoenvmap--end.md)                         | Stellen Sie alle Renderziele wieder her, und erstellen Sie, falls erforderlich, alle gerenderten Gesichter in der Umgebungs Zuordnungs Oberfläche.<br/>                                                                           |
| [**Gesichtserkennung**](id3dxrendertoenvmap--face.md)                       | Initiieren Sie die Zeichnung der einzelnen Gesichter einer Umgebungs Zuordnung.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Ruft die Beschreibung der Renderoberfläche ab.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Ruft das Direct3D-Gerät ab, das der Umgebungs Zuordnung zugeordnet ist.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Verwenden Sie diese Methode, um alle Verweise auf Videospeicher Ressourcen freizugeben und alle stateblocks zu löschen. Diese Methode sollte immer dann aufgerufen werden, wenn ein Gerät verloren geht oder ein Gerät zurückgesetzt wird.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Verwenden Sie diese Methode, um Ressourcen erneut abzurufen und den Anfangszustand zu speichern.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Eine Umgebungs Zuordnung wird für Textur kartogramm verwendet, um eine anspruchsvollere Szene ohne komplexe Geometrie bereitzustellen. Diese Schnittstelle unterstützt das Erstellen von Oberflächen für die folgenden Arten von Geometrie: Cube, Halbkugel oder Hemispheric, Parser oder Kugel.

Die **ID3DXRenderToEnvMap** -Schnittstelle wird durch Aufrufen der [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) -Funktion abgerufen.

Der LPD3DXRenderToEnvMap-Typ wird als Zeiger auf die **ID3DXRenderToEnvMap** -Schnittstelle definiert.


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
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

 

 
