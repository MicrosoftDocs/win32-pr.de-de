---
description: Fügt dem Animations Controller eine Animations Ausgabe hinzu und registriert Zeiger für die Transformation für Skalierung, Drehung und Übersetzung (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController:: registeranimationoutput-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350716"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>ID3DXAnimationController:: registeranimationoutput-Methode

Fügt dem Animations Controller eine Animations Ausgabe hinzu und registriert Zeiger für die Transformation für Skalierung, Drehung und Übersetzung (SRT).

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der Animations Ausgabe.

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die Daten der SRT-Transformation enthält. Kann **null** sein.

</dd> <dt>

*pscale* \[ in\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Skala des Animations Satzes beschreibt. Kann **null** sein.

</dd> <dt>

*protation* \[ in\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, die die Drehung des Animations Satzes beschreibt. Kann **null** sein.

</dd> <dt>

*ptranslation* \[ in\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Übersetzung des Animations Satzes beschreibt. Kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Wenn die Ausgabe der Animation bereits registriert ist, wird pmatrix mit den Eingabe Transformations Daten aufgefüllt.

Mit [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) erstellte Animations Sätze registrieren automatisch alle geladenen Animations Sätze.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
