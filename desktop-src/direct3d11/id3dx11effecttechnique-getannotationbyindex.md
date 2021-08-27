---
title: ID3DX11EffectTechnique GetAnnotationByIndex-Methode (D3dx11effect.h)
description: Abrufen einer Anmerkung nach Index. | ID3DX11EffectTechnique GetAnnotationByIndex-Methode (D3dx11effect.h)
ms.assetid: 703663b0-ee00-4686-a038-6c99ce61266b
keywords:
- GetAnnotationByIndex-Methode Direct3D 11
- GetAnnotationByIndex-Methode Direct3D 11 , ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11 , GetAnnotationByIndex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7de800e05dfb6731340ad7255019d4017eefb0cc88f9069e8c4aae4f327071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532568"
---
# <a name="id3dx11effecttechniquegetannotationbyindex-method"></a>ID3DX11EffectTechnique::GetAnnotationByIndex-Methode

Abrufen einer Anmerkung nach Index.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Index des Schnittstellenzeigers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie eine Anmerkung, um ein Element von Metadaten an eine Technik anzufügen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

