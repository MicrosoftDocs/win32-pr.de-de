---
title: ID3DX11Effect CloneEffect-Methode (D3dx11effect.h)
description: Erstellt eine Kopie einer Effektschnittstelle.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- CloneEffect-Methode Direct3D 11
- CloneEffect-Methode Direct3D 11 , ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , CloneEffect-Methode
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
ms.openlocfilehash: 9d9fa68fe05674573468eb684d8149d8dae45e540572f4d777bb860755c60e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124525"
---
# <a name="id3dx11effectcloneeffect-method"></a>ID3DX11Effect::CloneEffect-Methode

Erstellt eine Kopie einer Effektschnittstelle.

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

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Flags, die sich auf die Erstellung des geklonten Effekts auswirken. Kann 0 oder einer der folgenden Werte sein.



| Flag                                    | Beschreibung                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11 \_ EFFECT \_ CLONE \_ FORCE \_ NONSINGLE | Ignorieren Sie alle "einzelnen" Qualifizierer für Cbuffer. Alle Cbuffer verfügen über eigene [**ID3D11Buffer-S,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)die im geklonten Effekt erstellt werden. |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Zeiger auf einen [**ID3DX11Effect-Zeiger,**](id3dx11effect.md) der auf die Kopie des Effekts festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

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

 

