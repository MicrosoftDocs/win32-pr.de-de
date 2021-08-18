---
title: ID3DX11Effect GetConstantBufferByName-Methode (D3dx11effect.h)
description: Abrufen eines konstanten Puffers anhand des Namens.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- GetConstantBufferByName-Methode Direct3D 11
- GetConstantBufferByName-Methode Direct3D 11 , ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , GetConstantBufferByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400be04e6955807bb6b2a60e712323f8993e55ecc031086afb3597f3962091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632560"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>ID3DX11Effect::GetConstantBufferByName-Methode

Abrufen eines konstanten Puffers anhand des Namens.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Der Konstantenpuffername.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Ein Zeiger auf den konstanten Puffer, der durch den Namen angegeben wird. Siehe [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Hinweise

Ein Effekt, der eine Variable enthält, die von einer Anwendung gelesen/geschrieben wird, erfordert mindestens einen konstanten Puffer. Um eine optimale Leistung zu erzielen, sollte ein Effekt Variablen basierend auf ihrer Aktualisierungshäufigkeit in einem oder mehreren konstanten Puffern organisieren.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

