---
title: D3D12CalcSubresource-Funktion (D3dx12.h)
description: Berechnet einen Unterressourcenindex für eine Textur.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource-Funktion
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c704be7087d95d739685bc2823ec1c31a027b4406a3110986220927fdbbffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751720"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource-Funktion

Berechnet einen Unterressourcenindex für eine Textur.

## <a name="syntax"></a>Syntax


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MipSlice* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Index für die zu adressierende Mipmapebene. 0 gibt die erste, ausführlichste Mipmapebene an.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Index für die zu adressierende Arrayebene. Verwenden Sie immer 0 für Volumetexturen (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Index für die ebene Ebene, die adressiert werden soll.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Mipmapebenen in der Ressource.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index, der MipSlice + (ArraySlice \* MipLevels) entspricht.

## <a name="remarks"></a>Hinweise

Ein Puffer ist eine unstrukturierte Ressource und daher so definiert, dass er eine einzelne Unterressource enthält. APIs, die Puffer verwenden, benötigen keinen Unterressourcenindex. Eine Textur ist dagegen stark strukturiert. Jedes Texturobjekt kann abhängig von der Größe des Arrays und der Anzahl der Mipmap-Ebenen eine oder mehrere Unterressourcen enthalten.

Bei Volumetexturen (3D) sind alle Slices für eine bestimmte mipmap-Ebene ein einzelner Unterressourcenindex.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

