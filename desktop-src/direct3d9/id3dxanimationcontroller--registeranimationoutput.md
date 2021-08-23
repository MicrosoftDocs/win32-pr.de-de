---
description: Fügt dem Animationscontroller eine Animationsausgabe hinzu und registriert Zeiger für Skalierungs-, Dreh- und Übersetzungstransformationen (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: ID3DXAnimationController::RegisterAnimationOutput-Methode (D3dx9anim.h)
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
ms.openlocfilehash: dc48eb9f2fd6ee5fee6c04936801997145a5ea21542b9b5ff8ec6d257eee80e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987820"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>ID3DXAnimationController::RegisterAnimationOutput-Methode

Fügt dem Animationscontroller eine Animationsausgabe hinzu und registriert Zeiger für Skalierungs-, Dreh- und Übersetzungstransformationen (SRT).

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

*Name* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Animationsausgabe.

</dd> <dt>

*pMatrix* \[ In\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die SRT-Transformationsdaten enthält. Kann NULL **sein.**

</dd> <dt>

*pScale* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf einen [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Skalierung des Animationssets beschreibt. Kann NULL **sein.**

</dd> <dt>

*pRotation* \[ In\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Quaternion,**](d3dxquaternion.md) die die Drehung des Animationssets beschreibt. Kann NULL **sein.**

</dd> <dt>

*pTranslation* \[ In\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf einen [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Übersetzung des Animationssets beschreibt. Kann NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn die Animationsausgabe bereits registriert ist, wird pMatrix mit den Eingabetransformationsdaten gefüllt.

Mit [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) erstellte Animationssätze registrieren automatisch alle geladenen Animationssätze.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
