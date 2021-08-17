---
title: D3DX11CreateEffectFromMemory-Funktion (D3dx11effect.h)
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
ms.openlocfilehash: c99cdef28acae9419a5b597d5be1703ea9e866d521d7f94bb330b151abc74842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124805"
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

*Pdata* 
</dt> <dd>

Typ: **\* void**

Blob der kompilierten Effektdaten.

</dd> <dt>

*Datalength* 
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Länge des Datenblobs.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Es sind keine Effektflags vorhanden. Auf NULL festlegen.

</dd> <dt>

*pDevice* 
</dt> <dd>

Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Zeiger auf die [**ID3D11Device,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) für die Effect-Ressourcen erstellt werden sollen.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Adresse der neu erstellten [**ID3DX11Effect-Schnittstelle.**](id3dx11effect.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Sie müssen [die Effects 11-Quelle](https://github.com/Microsoft/FX11) verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Effects 11-Quelle finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11 Funktionen](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

