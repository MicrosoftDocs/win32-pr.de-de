---
title: ID3DX11Effect getdesc-Methode (D3dx11effect. h)
description: Sie erhalten eine Beschreibung des Effekts.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Getdesc-Methode Direct3D 11
- Getdesc-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996123"
---
# <a name="id3dx11effectgetdesc-method"></a>ID3DX11Effect:: getdesc-Methode

Sie erhalten eine Beschreibung des Effekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* 
</dt> <dd>

Type: **[ **Bibliothek d3dx11 \_ Effect \_ DESC**](d3dx11-effect-desc.md)\***

Ein Zeiger auf eine Effekt Beschreibung (siehe [**Bibliothek d3dx11 \_ Effect \_ ensc**](d3dx11-effect-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Eine Effekt Beschreibung enthält grundlegende Informationen zu einem Effekt, wie z. b. die darin enthaltenen Techniken und die erforderlichen Konstanten Puffer Ressourcen.

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

 

 





