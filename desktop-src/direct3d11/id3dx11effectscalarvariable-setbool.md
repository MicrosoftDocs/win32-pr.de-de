---
title: ID3DX11EffectScalarVariable SetBool-Methode (D3dx11effect.h)
description: Legen Sie eine boolesche Variable fest.
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- SetBool-Methode Direct3D 11
- SetBool-Methode Direct3D 11, ID3DX11EffectScalarVariable-Schnittstelle
- ID3DX11EffectScalarVariable-Schnittstelle Direct3D 11 , SetBool-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f12837a0a6c33d4b5ae0345bd654bd5e0d19d31ea449a5eca8e77ba740c782c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408170"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a>ID3DX11EffectScalarVariable::SetBool-Methode

Legen Sie eine boolesche Variable fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* 
</dt> <dd>

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Ein Zeiger auf die Variable.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

