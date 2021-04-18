---
title: D3D12IsLayoutOpaque-Funktion (D3dx12. h)
description: Gibt an, ob das Layout nicht transparent ist.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque-Funktion
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351925"
---
# <a name="d3d12islayoutopaque-function"></a>D3D12IsLayoutOpaque-Funktion

Gibt an, ob das Layout nicht transparent ist.

## <a name="syntax"></a>Syntax


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Layout* 
</dt> <dd>

Type: **[ **D3D12 \_ Texture \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

Das zu überprüfen Layout als [**D3D12 \_ Textur \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Ein **boolescher** Wert, der angibt, ob das Layout nicht transparent ist. Ein Layout ist nicht transparent, wenn es D3D12 \_ Texture \_ Layout \_ unknown oder D3D12 \_ Texture \_ Layout \_ 64 KB \_ undefiniertes \_ Swizzle ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





