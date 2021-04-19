---
title: D3DX12GetBaseSubobjectType-Funktion (D3dx12. h)
description: Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType-Funktion
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350661"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>D3DX12GetBaseSubobjectType-Funktion

Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.

## <a name="syntax"></a>Syntax


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Subobjecttype* 
</dt> <dd>

Type: **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**

Ein-Enumerationswert, der den Typ des untergeordneten Objekts angibt, an dem Sie interessiert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**

Wenn *subobjecttype* einem untergeordneten Datentyp entspricht, der von einem anderen untergeordneten Datentyp abgeleitet ist, wird der untergeordnete Typ des Basis-unter-Datentyps zurückgegeben. Andernfalls wird der bestandene untergeordnete Typ zurückgegeben. Wenn z. b. die **\_ \_ \_ \_ \_ Tiefe \_ STENCIL1 des D3D12 Pipeline State** -untergeordneten Typs überschritten wird, wird die **\_ \_ \_ \_ \_ tiefen \_ Schablone des D3D12-Pipeline Zustands** untergeordneten Typs zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





