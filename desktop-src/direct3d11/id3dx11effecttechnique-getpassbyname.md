---
title: ID3DX11EffectTechnique GetPassByName-Methode (D3dx11effect.h)
description: Erhalten Sie einen Pass nach Name.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- GetPassByName-Methode Direct3D 11
- GetPassByName-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11 , GetPassByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfad489fe6c4eda8ea417a9f272bcc0a7d4035eb04bc675cf599e4f5381234db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532362"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>ID3DX11EffectTechnique::GetPassByName-Methode

Erhalten Sie einen Pass nach Name.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Name des Durchgangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Ein Zeiger auf eine [**ID3DX11EffectPass.**](id3dx11effectpass.md)

## <a name="remarks"></a>Hinweise

Eine Technik enthält einen oder mehrere Durchläufe. einen Pass mit einem Namen oder Index erhalten.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

