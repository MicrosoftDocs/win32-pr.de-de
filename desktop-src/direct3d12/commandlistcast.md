---
title: Commandlistcast-Funktion (D3dx12. h)
description: Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Commandlistcast-Funktion
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350725"
---
# <a name="commandlistcast-function"></a>Commandlistcast-Funktion

Diese Funktions Vorlage wandelt einen Konstanten Zeiger auf eine beliebige Befehlsliste in einen Konstanten Zeiger auf einen ID3D12CommandList um.

Diese Umwandlung ist nützlich zum Übergeben von stark typisierten Befehlslisten Zeigern an [**executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="syntax"></a>Syntax


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Trupp* 
</dt> <dd>

Typ: **t \_ commandlisttype \* \* konstant**

Die stark typisierte Befehlsliste, die umgewandelt werden soll.

Das Vorlagen Argument **t \_ commandlisttype** gibt ein beliebiges stark typisiertes Befehlslisten Objekt an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **ID3D12CommandList \* konstant \***

Die stark typisierte Befehlsliste, die als [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)neu interpretiert wird.

## <a name="remarks"></a>Bemerkungen

Commandlistcast führt eine **uminterpretierungsumwandlung \_** aus. Die Umwandlung ist gültig, solange die Konstante der Befehlsliste respektiert wird.

Die commandlistcast-Funktion ist wie folgt definiert:


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





