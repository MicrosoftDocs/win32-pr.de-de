---
title: ID3DX11EffectVariable GetAnnotationByName-Methode (D3dx11effect.h)
description: Erhalten Sie eine Anmerkung nach Namen. | ID3DX11EffectVariable GetAnnotationByName-Methode (D3dx11effect.h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- GetAnnotationByName-Methode Direct3D 11
- GetAnnotationByName-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , GetAnnotationByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766366497187fec9c6dab3c5f92f5fbca23f5729297976d2c9e2c7e4ffb0deef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119376460"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a>ID3DX11EffectVariable::GetAnnotationByName-Methode

Erhalten Sie eine Anmerkung nach Namen.

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

Der Anmerkungsname.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Beachten Sie, dass die zurückgegebene **ID3DX11EffectVariable** leer ist, wenn die Anmerkung nicht gefunden wird. Die [**ID3DX11EffectVariable::IsValid-Methode**](id3dx11effectvariable-isvalid.md) sollte aufgerufen werden, um zu bestimmen, ob die Anmerkung gefunden wurde.

## <a name="remarks"></a>Hinweise

Annonationen können an eine Technik, einen Pass oder eine globale Variable angefügt werden.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

