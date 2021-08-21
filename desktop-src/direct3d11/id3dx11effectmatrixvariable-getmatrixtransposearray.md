---
title: ID3DX11EffectMatrixVariable GetMatrixTransposeArray-Methode (D3dx11effect.h)
description: Transponieren und abrufen eines Arrays von Gleitkommamatrizen.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- GetMatrixTransposeArray-Methode Direct3D 11
- GetMatrixTransposeArray-Methode Direct3D 11 , ID3DX11EffectMatrixVariable-Schnittstelle
- ID3DX11EffectMatrixVariable-Schnittstelle Direct3D 11 , GetMatrixTransposeArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07ba32807b4acdd4f244b7b4c3cc82b3941cb5a52d899f1e8361c841b58d53ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046168"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a>ID3DX11EffectMatrixVariable::GetMatrixTransposeArray-Methode

Transponieren und abrufen eines Arrays von Gleitkommamatrizen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pdata* 
</dt> <dd>

Typ: **\* float**

Ein Zeiger auf das erste Element eines Arrays von transponierten Matrizen.

</dd> <dt>

*Offset* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Offset (in Anzahl von Matrizen) zwischen dem Anfang des Arrays und der ersten abzurufenden Matrix.

</dd> <dt>

*Count* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der abzurufenden Matrizen im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Durch das Transponieren einer Matrix wird die Datenreihenfolge von der Zeilenspaltenreihenfolge in die Spaltenreihenfolge (oder umgekehrt) neu angeordnet.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

