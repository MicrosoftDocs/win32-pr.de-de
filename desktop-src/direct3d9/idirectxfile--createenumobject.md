---
description: Erstellt ein Enumeratorobjekt. Veraltet.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: IDirectXFile::CreateEnumObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af10a0f46877a159ab8c6543fba9c1406d083e6b3f4a57cf1c41b9fb2d92612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985150"
---
# <a name="idirectxfilecreateenumobject-method"></a>IDirectXFile::CreateEnumObject-Methode

Erstellt ein Enumeratorobjekt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvSource* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf Daten, deren Inhalt vom Wert von dwLoadOptions abhängig ist

</dd> <dt>

*dwLoadOptions* \[ In\]
</dt> <dd>

Typ: **[ **DXFILELOADOPTIONS**](dxfile.md)**

Ein Wert, der die Quelle der Daten angibt. Dieser Wert kann eines der DXFILELOAD \_ xxx-Flags in [DXFILE-Konstanten sein.](dxfile.md)

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

Adresse eines Zeigers auf eine [**IDirectXFileEnumObject-Schnittstelle,**](idirectxfileenumobject.md) die das erstellte Enumeratorobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Hinweise

Verwenden Sie nach der Verwendung dieser Methode eine der IDirectXFileEnumObject-Methoden, um ein Datenobjekt abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
