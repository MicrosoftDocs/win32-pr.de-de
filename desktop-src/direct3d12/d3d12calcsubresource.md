---
title: D3D12CalcSubresource-Funktion (D3dx12. h)
description: Berechnet einen subresource-Index für eine Textur.
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
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371884"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource-Funktion

Berechnet einen subresource-Index für eine Textur.

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

*Mipslice* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der null basierte Index für die zu Adressier nende MipMap-Ebene. 0 gibt die erste, ausführlichste MipMap-Ebene an.

</dd> <dt>

*Arrayslice* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der null basierte Index für die zu Adressier gende Array Ebene. Verwenden Sie immer 0 für volumenvolumes (3D).

</dd> <dt>

*Planeslice* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der null basierte Index für die zu Adressier Ebene der Ebene.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl von MipMap-Ebenen in der Ressource.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Index, der mipslice + (arrayslice- \* miplevels) gleicht.

## <a name="remarks"></a>Bemerkungen

Ein Puffer ist eine unstrukturierte Ressource und wird daher als eine einzelne untergeordnete Quelle definiert. APIs, die Puffer akzeptieren, benötigen keinen unter Quell Index. Eine Textur auf der anderen Seite ist stark strukturiert. Jedes Textur Objekt kann abhängig von der Größe des Arrays und der Anzahl von MipMap-Ebenen eine oder mehrere unter Ressourcen enthalten.

Bei volumevolumes (3D) handelt es sich bei allen Slices für eine bestimmte MipMap-Ebene um einen einzelnen subresource-Index.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

