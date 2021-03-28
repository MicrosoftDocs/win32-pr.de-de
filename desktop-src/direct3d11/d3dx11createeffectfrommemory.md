---
title: D3DX11CreateEffectFromMemory-Funktion (D3dx11effect. h)
description: Erstellt einen Effekt aus einem binären Effekt oder einer Datei.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- D3DX11CreateEffectFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996010"
---
# <a name="d3dx11createeffectfrommemory-function"></a>D3DX11CreateEffectFromMemory-Funktion

Erstellt einen Effekt aus einem binären Effekt oder einer Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* 
</dt> <dd>

Typ: **void \***

BLOB der kompilierten Effekt Daten.

</dd> <dt>

*DATALENGTH* 
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

Länge des Daten-BLOBs.

</dd> <dt>

*Fxflags* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Es sind keine Auswirkungs Flags vorhanden. Auf NULL festlegen.

</dd> <dt>

*pdevice* 
</dt> <dd>

Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Zeiger auf den [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , auf dem die Effekt Ressourcen erstellt werden sollen.

</dd> <dt>

*ppeer-ect* 
</dt> <dd>

Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Adresse der neu erstellten [**ID3DX11Effect**](id3dx11effect.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Sie müssen die [Effekte 11-Quelle](https://github.com/Microsoft/FX11) verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Funktionen](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

