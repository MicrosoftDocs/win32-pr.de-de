---
description: Gibt die Anzahl der derzeit im Animationscontroller registrierten Animationssätze zurück.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: ID3DXAnimationController::GetNumAnimationSets-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026820"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>ID3DXAnimationController::GetNumAnimationSets-Methode

Gibt die Anzahl der derzeit im Animationscontroller registrierten Animationssätze zurück.

## <a name="syntax"></a>Syntax


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Animationssätze.

## <a name="remarks"></a>Hinweise

Der Controller enthält eine beliebige Anzahl von Animationssätzen und -spuren. Animationssätze können mit [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)registriert werden. Ein Animationscontroller, der durch einen Aufruf von [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) erstellt wurde, registriert automatisch geladene Animationssätze.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
