---
description: Löst Daten Verweise auf. Veraltet.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Idirectxfiledatareferen:: Resolve-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364377"
---
# <a name="idirectxfiledatareferenceresolve-method"></a>Idirectxfiledatareferen:: Resolve-Methode

Löst Daten Verweise auf. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdataobj* \[ Out, retval\]
</dt> <dd>

Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledatareferenzierung](idirectxfiledatareference.md)
</dt> </dl>

 

 




