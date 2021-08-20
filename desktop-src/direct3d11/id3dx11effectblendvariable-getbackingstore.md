---
title: ID3DX11EffectBlendVariable GetBackingStore-Methode (D3dx11effect.h)
description: Abrufen eines Zeigers auf eine Mischungszustandsvariable.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- GetBackingStore-Methode Direct3D 11
- GetBackingStore-Methode Direct3D 11 , ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11 , GetBackingStore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f02f09c0db4ec56ee592dc39ddbb7fef1ae52d328edec5d9a5c9fd17b769ef58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046558"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a>ID3DX11EffectBlendVariable::GetBackingStore-Methode

Abrufen eines Zeigers auf eine Mischungszustandsvariable.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Blendzustandsbeschreibungen. Wenn der Effekt nur eine Blendzustandsvariable enthält, verwenden Sie 0.

</dd> <dt>

*pBlendDesc* 
</dt> <dd>

Typ: **[ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***

Ein Zeiger auf eine Beschreibung des Blendzustands (siehe [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Effektvariablen werden im Speicher im Sicherungsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungsspeicher auf das Gerät kopiert. Sicherungsspeicherdaten können verwendet werden, um die Variable bei Bedarf neu zu erstellen.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectBlendVariable](id3dx11effectblendvariable.md)
</dt> </dl>

 

