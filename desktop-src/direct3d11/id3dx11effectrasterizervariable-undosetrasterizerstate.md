---
title: ID3DX11EffectRasterizerVariable undotartrasterizerstate-Methode (D3dx11effect. h)
description: Stellt einen zuvor festgelegten Raster-Zustand wieder her.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Undotartrasterizerstate-Methode Direct3D 11
- Undotartrasterizerstate-Methode Direct3D 11, ID3DX11EffectRasterizerVariable-Schnittstelle
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11, undotartrasterizerstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219715"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a>ID3DX11EffectRasterizerVariable:: undotartrasterizerstate-Methode

Stellt einen zuvor festgelegten Raster-Zustand wieder her.

## <a name="syntax"></a>Syntax


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index in ein Array von Raster-Schnittstellen. Wenn nur eine Raster-Schnittstelle vorhanden ist, verwenden Sie 0.

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

