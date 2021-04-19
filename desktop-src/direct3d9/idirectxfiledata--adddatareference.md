---
description: Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Idirectxfiledata:: adddatareferenzierungsmethode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366455"
---
# <a name="idirectxfiledataadddatareference-method"></a>Idirectxfiledata:: adddatareferenzierungsmethode

Erstellt ein Daten Verweis Objekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szref* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Datenobjekts, auf das verwiesen wird. Dieser Parameter kann **null** sein, wenn pguidref einen Verweis auf die GUID bereitstellt.

</dd> <dt>

*pguidref* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \***

Zeiger auf die GUID, die die Daten darstellt. Dieser Parameter kann **null** sein, wenn szref einen Verweis auf den Namen bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue

## <a name="remarks"></a>Bemerkungen

Damit diese Methode erfolgreich ausgeführt werden kann, darf der szref-oder pguidref-Parameter nicht **null** sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledata](idirectxfiledata.md)
</dt> </dl>

 

 
