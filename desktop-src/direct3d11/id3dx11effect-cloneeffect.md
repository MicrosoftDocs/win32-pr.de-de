---
title: ID3DX11Effect cloneeffect-Methode (D3dx11effect. h)
description: Erstellt eine Kopie einer Effect-Schnittstelle.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Cloneeffect-Methode Direct3D 11
- Cloneeffect-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, cloneeffect-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982604"
---
# <a name="id3dx11effectcloneeffect-method"></a>ID3DX11Effect:: cloneeffect-Methode

Erstellt eine Kopie einer Effect-Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Flags, die sich auf die Erstellung des geklonten Effekts auswirken. Kann 0 oder einer der folgenden Werte sein.



| Flag                                    | Beschreibung                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Bibliothek d3dx11 \_ Effect \_ Klon \_ Force \_ nonsingle | Ignorieren Sie alle "einzelnen" Qualifizierer für cbuffers. Alle cBuffer verfügen über eigene [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s, die im geklonten Effekt erstellt werden. |



 

</dd> <dt>

*ppclonedebug* 
</dt> <dd>

Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Zeiger auf einen [**ID3DX11Effect**](id3dx11effect.md) -Zeiger, der auf die Kopie des Effekts festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

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

 

