---
description: Ruft die Titelbeschreibung ab.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: ID3DXAnimationController::GetTrackDesc-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af3c8fbddc841f345ab0dcdea67f35706bba26c13d81ffae781ab4d3def9c7bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026810"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a>ID3DXAnimationController::GetTrackDesc-Methode

Ruft die Titelbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nachverfolgungsbezeichner.

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**

Zeiger auf die Trackbeschreibung. Siehe [**D3DXTRACK \_ DESC**](d3dxtrack-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
