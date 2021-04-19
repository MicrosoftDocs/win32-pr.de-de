---
description: Gibt die Anzahl von Animations Sätzen zurück, die derzeit im Animations Controller registriert sind.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController:: getnumanimationsets-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367345"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>ID3DXAnimationController:: getnumanimationsets-Methode

Gibt die Anzahl von Animations Sätzen zurück, die derzeit im Animations Controller registriert sind.

## <a name="syntax"></a>Syntax


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Animations Sätze.

## <a name="remarks"></a>Bemerkungen

Der Controller enthält eine beliebige Anzahl von Animations Sätzen und-Spuren. Animations Sätze können mit [**registeranimationoutput**](id3dxanimationcontroller--registeranimationoutput.md)registriert werden. Ein Animations Controller, der durch einen [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) -Aufrufvorgang erstellt wird, registriert geladene Animations Sätze automatisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
