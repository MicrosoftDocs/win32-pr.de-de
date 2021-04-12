---
description: Beendet eine aktive Technik.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect:: End-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355016"
---
# <a name="id3dxeffectend-method"></a>ID3DXEffect:: End-Methode

Beendet eine aktive Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt immer den Wert S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Alle Rendering in einem Effekt erfolgt in einem passenden Paar aus [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und **ID3DXEffect:: End** -aufrufen. Nachdem alle Durchgänge gerendert wurden, muss **ID3DXEffect:: End** aufgerufen werden, um die aktive Technik zu beenden. Das Effektsystem antwortet mithilfe des Zustands Blocks, der erstellt wurde, als **ID3DXEffect:: begin** aufgerufen wurde, um den Pipeline Zustand vor **ID3DXEffect:: begin** automatisch wiederherzustellen.

Standardmäßig übernimmt das Effektsystem das Speichern des Zustands vor einer Technik und das Wiederherstellen des Zustands nach einer Technik. Wenn Sie diese Speicher-und Wiederherstellungs Funktion deaktivieren möchten, finden Sie weitere Informationen unter [D3DXFX \_ donotsavesamplerstate](d3dxfx.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




