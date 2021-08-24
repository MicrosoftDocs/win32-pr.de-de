---
description: Erstellt ein Datenverweisobjekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: IDirectXFileData::AddDataReference-Methode (DXFile.h)
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
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747260"
---
# <a name="idirectxfiledataadddatareference-method"></a>IDirectXFileData::AddDataReference-Methode

Erstellt ein Datenverweisobjekt als untergeordnetes Objekt und fügt es hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szRef* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Datenobjekts, auf das verwiesen wird. Dieser Parameter kann **NULL** sein, wenn pguidRef einen Verweis auf die GUID bereitstellt.

</dd> <dt>

*pguidRef* \[ In\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \***

Zeiger auf die GUID, die die Daten darstellt. Dieser Parameter kann **NULL** sein, wenn szRef einen Verweis auf den Namen bereitstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Hinweise

Damit diese Methode erfolgreich ausgeführt werden kann, muss der szRef- oder pguidRef-Parameter ungleich **NULL** sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
