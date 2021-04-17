---
description: Dies ist eine vom Benutzer implementierte Schnittstelle, die es Benutzern ermöglicht, den Gerätezustand von einem Effekt festzulegen.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: ID3DXEffectStateManager-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355227"
---
# <a name="id3dxeffectstatemanager-interface"></a>ID3DXEffectStateManager-Schnittstelle

Dies ist eine vom Benutzer implementierte Schnittstelle, die es Benutzern ermöglicht, den Gerätezustand von einem Effekt festzulegen. Jede der Methoden in dieser Schnittstelle muss vom Benutzer implementiert werden und wird dann als Rückrufe für die Anwendung verwendet, wenn eine der folgenden Optionen auftritt:

-   Durch einen Effekt wird [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)aufgerufen.
-   Der Effekt Zustand wird durch Aufrufen der entsprechenden Zustands Änderungs-API dynamisch aktualisiert. Weitere Informationen finden Sie auf den einzelnen Methoden Seiten.

Wenn eine Anwendung den Zustands-Manager verwendet, um benutzerdefinierte Rückrufe zu implementieren, wird der Zustand beim Aufrufen von [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) und [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md)durch einen Effekt nicht mehr automatisch gespeichert und wieder hergestellt. Da die Anwendung ein benutzerdefiniertes Speicher-und Wiederherstellungs Verhalten in den Rückrufen implementiert hat, wird dieses automatische Verhalten umgangen.

## <a name="members"></a>Member

Die **ID3DXEffectStateManager** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXEffectStateManager** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXEffectStateManager** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Lightenable**](id3dxeffectstatemanager--lightenable.md)                           | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.<br/>                                 |
| [**Setf-VF**](id3dxeffectstatemanager--setfvf.md)                                     | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.<br/>                                         |
| [**Setlight**](id3dxeffectstatemanager--setlight.md)                                 | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht festzulegen.<br/>                                            |
| [**Setmaterial**](id3dxeffectstatemanager--setmaterial.md)                           | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.<br/>                                     |
| [**Setnpatchmode**](id3dxeffectstatemanager--setnpatchmode.md)                       | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.<br/>   |
| [**Setpixelshader**](id3dxeffectstatemanager--setpixelshader.md)                     | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen PixelShader festzulegen.<br/>                                     |
| [**Setpixelshaderconstantb**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.<br/>        |
| [**Setpixelshaderconstantf**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.<br/> |
| [**Setpixelshaderconstanti**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.<br/>        |
| [**"-Trend"**](id3dxeffectstatemanager--setrenderstate.md)                     | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.<br/>                                       |
| [**Setsamplerstate**](id3dxeffectstatemanager--setsamplerstate.md)                   | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.<br/>                                          |
| [**Settexturestagestate**](id3dxeffectstatemanager--settexturestagestate.md)         | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Status der Textur Stufe festzulegen.<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festzulegen.<br/>                                        |
| [**Setvertexshader**](id3dxeffectstatemanager--setvertexshader.md)                   | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festzulegen.<br/>                                    |
| [**Setvertexshaderconstantb**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.<br/>        |
| [**Setvertexshaderconstantf**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.<br/> |
| [**Setvertexshaderconstanti**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-ganzzahligen Konstanten festzulegen.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Ein Benutzer erstellt eine ID3DXEffectStateManager-Schnittstelle, indem er eine Klasse implementiert, die von dieser Schnittstelle abgeleitet wird, und alle Schnittstellen Methoden implementiert. Nachdem die Schnittstelle erstellt wurde, können Sie den Zustands-Manager mit [**ID3DXEffect:: getstatemanager**](id3dxeffect--getstatemanager.md) und [**ID3DXEffect:: setstatemanager**](id3dxeffect--setstatemanager.md)innerhalb eines Effekts aufrufen oder festlegen.

Der LPD3DXEFFECTSTATEMANAGER-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
