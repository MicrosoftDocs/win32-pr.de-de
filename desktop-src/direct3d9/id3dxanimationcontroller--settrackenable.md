---
description: Aktiviert oder deaktiviert eine Spur im Animations Controller.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'ID3DXAnimationController:: settrackenable-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050908"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>ID3DXAnimationController:: settrackenable-Methode

Aktiviert oder deaktiviert eine Spur im Animations Controller.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner des Titels, der gemischt werden soll.

</dd> <dt>

*Aktivieren* \[ von in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Aktivieren Sie den Wert. Legen Sie diese Einstellung auf " **true** " fest, um diese Spur im Controller zu aktivieren, oder auf " **false** ", um eine Vermischung zu verhindern

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Das Enable-Flag muss auf " **true**" festgelegt werden, um eine Spur mit anderen Spuren zu mischen. Umgekehrt verhindert das Festlegen des Flags auf **false** , dass der Track nicht mit anderen Spuren gemischt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
