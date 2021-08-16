---
title: ID3DX11EffectGroup GetAnnotationByName-Methode (D3dx11effect.h)
description: Abrufen einer Anmerkung anhand des Namens. | ID3DX11EffectGroup GetAnnotationByName-Methode (D3dx11effect.h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- GetAnnotationByName-Methode Direct3D 11
- GetAnnotationByName-Methode Direct3D 11 , ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11 , GetAnnotationByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d80c0d59a1fd0a58c756d72f6215f13b4e3391e44828aa8e1bcff23063292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535739"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a>ID3DX11EffectGroup::GetAnnotationByName-Methode

Abrufen einer Anmerkung anhand des Namens.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name des Annotation-Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Beachten Sie, dass die zurückgegebene **ID3DX11EffectVariable** leer ist, wenn die Anmerkung nicht gefunden wird. Die [**ID3DX11EffectVariable::IsValid-Methode**](id3dx11effectvariable-isvalid.md) sollte aufgerufen werden, um zu bestimmen, ob die Anmerkung gefunden wurde.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

