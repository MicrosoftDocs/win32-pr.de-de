---
title: ID3DX11EffectRasterizerVariable getbackingstore-Methode (D3dx11effect. h)
description: Ein Zeiger auf eine Variable, die den rasteriser-Zustand enthält, wird angezeigt.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Getbackingstore-Methode Direct3D 11
- Getbackingstore-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable Interface Direct3D 11, getbackingstore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050912"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>ID3DX11EffectRasterizerVariable:: getbackingstore-Methode

Ein Zeiger auf eine Variable, die den rasteriser-Zustand enthält, wird angezeigt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indizieren Sie in ein Array von rasteriser-State-Beschreibungen. Wenn nur eine rasteriser-Variable vorhanden ist, verwenden Sie 0.

</dd> <dt>

*"prasterizerde"* 
</dt> <dd>

Typ: **[ **D3D11 \_ Rasterizer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Ein Zeiger auf eine rasteriser-State Description (siehe [**D3D11 \_ Rasterizer \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)Debug).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert. Das Sichern von Speicherdaten kann verwendet werden, um die Variable bei Bedarf neu zu erstellen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

