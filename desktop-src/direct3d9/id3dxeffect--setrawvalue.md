---
description: Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect:: strawvalue-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354997"
---
# <a name="id3dxeffectsetrawvalue-method"></a>ID3DXEffect:: strawvalue-Methode

Legen Sie einen zusammenhängenden Bereich von shaderkonstanten mit einer Speicher Kopie fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle für den festzulegenden Wert oder den Namen des Werts, der als Zeichenfolge übertragen wird. Das Übergeben eines Handles ist effizienter. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Typ: **void \***

Zeiger auf einen Puffer, der die Daten enthält, die festgelegt werden sollen. "Strawvalue" prüft, ob ein gültiger Arbeitsspeicher vorhanden ist, überprüft jedoch keine gültigen Daten.

</dd> <dt>

*Offestinbytes* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl von Bytes zwischen dem Anfang der Wirkungs Daten und dem Anfang der Effekt Konstanten, die festgelegt werden.

</dd> <dt>

*Bytes* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Größe des festzulegenden Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: E \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Setrawvalue ist eine sehr schnelle Möglichkeit zum Festlegen von Effekt Konstanten, da eine Speicher Kopie ohne Validierung oder Datenkonvertierung (z. b. die Konvertierung einer Zeilen hauptmatrix in eine Spalten hauptmatrix) durchgeführt wird. Verwenden Sie setrawvalue, um eine Reihe zusammenhängender Wirkungs Konstanten festzulegen. Beispielsweise können Sie ein Array von 20 Matrizen mit 20 Aufrufen von [**ID3DXBaseEffect:: setMatrix**](id3dxbaseeffect--setmatrix.md) oder mithilfe eines einzelnen setrawvalue festlegen.

Alle Werte werden als "matrix4x4s" oder "float4s" erwartet, und es wird erwartet, dass alle Matrizen in der Spalten Hauptreihen Folge sind. Int-oder float-Werte werden in einen float4-Wert umgewandelt. Daher wird dringend empfohlen, dass Sie "strawvalue" nur mit "float4" oder "matrix4x4" verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
