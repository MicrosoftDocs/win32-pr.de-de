---
title: ID3DX11Effect getconstantbufferbyname-Methode (D3dx11effect. h)
description: Einen konstanten Puffer anhand des Namens erhalten.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Getconstantbufferbyname-Methode Direct3D 11
- Getconstantbufferbyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getconstantbufferbyname-Methode
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
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870172"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>ID3DX11Effect:: getconstantbufferbyname-Methode

Einen konstanten Puffer anhand des Namens erhalten.

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

Der Name des Konstanten Puffers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Ein Zeiger auf den konstanten Puffer, der durch den Namen angegeben wird. Siehe [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Bemerkungen

Ein Effekt, der eine Variable enthält, die von einer Anwendung gelesen/geschrieben wird, erfordert mindestens einen konstanten Puffer. Um die optimale Leistung zu erzielen, sollten Sie die Variablen basierend auf Ihrer Aktualisierungshäufigkeit in mindestens einen konstanten Puffer anordnen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

