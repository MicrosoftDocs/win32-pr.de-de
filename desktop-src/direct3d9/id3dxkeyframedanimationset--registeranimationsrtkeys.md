---
description: Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet:: registeranimationsrtkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351985"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>ID3DXKeyframedAnimationSet:: registeranimationsrtkeys-Methode

Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen der Animation.

</dd> <dt>

*Numscalekeys* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Skalierungs Schlüssel.

</dd> <dt>

*Numrotationkeys* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Rotations Schlüsseln.

</dd> <dt>

*Numtranslationkeys* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Übersetzungs Schlüsseln.

</dd> <dt>

*pscalekeys* \[ in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugeordneter [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das von der Methode mit Skalierungs Daten gefüllt wird.

</dd> <dt>

" *protationkeys* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) -Quaternionen, die die Methode mit den Rotationsdaten füllt.

</dd> <dt>

*ptranslationkeys* \[ in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) Vektoren, das die Methode mit Übersetzungs Daten füllt.

</dd> <dt>

*panimationindex* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt den Animations Index zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: getnumscalekeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: getnumrotationkeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: getnumtranslationkeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
