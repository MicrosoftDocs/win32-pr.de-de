---
description: Legt einen Ereignis Schlüssel fest, der einen Animations Titel aktiviert oder deaktiviert.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController:: keytrackenable-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354256"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>ID3DXAnimationController:: keytrackenable-Methode

Legt einen Ereignis Schlüssel fest, der einen Animations Titel aktiviert oder deaktiviert.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner des zu ändernden Animations Titels.

</dd> <dt>

Kann nicht angezeigt werden  \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Flag aktivieren. Legen Sie diese Einstellung auf " **true** " fest, um den Animations Titel zu aktivieren, oder auf " **false** ", um die

</dd> <dt>

*StartTime* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Globaler Zeit Schlüssel. Gibt die globale Zeit an, zu der die Änderung stattfindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das Priority Blend-Ereignis. **Null** wird zurückgegeben, wenn der Titel ungültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
