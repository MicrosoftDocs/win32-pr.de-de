---
description: Erstellt ein Enumeratorobjekt. Veraltet.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Idirectxfile:: kreatedenumuject-Methode (dxfile. h)'
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
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762249"
---
# <a name="idirectxfilecreateenumobject-method"></a>Idirectxfile:: deateeinumuject-Methode

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

*pvsource* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf Daten, deren Inhalt vom Wert von dwloadoption abhängt

</dd> <dt>

*dwloadoption* \[ in\]
</dt> <dd>

Typ: **[ **dxfileloadoptions**](dxfile.md)**

Der-Wert, der die Quelle der Daten angibt. Bei diesem Wert kann es sich um eines der dxfileload \_ xxx-Flags in [dxfile-Konstanten](dxfile.md)handeln.

</dd> <dt>

*ppumubj* \[ Out, retval\]
</dt> <dd>

Typ: **[ **lpdirectxfileerumubject**](idirectxfileenumobject.md)\***

Adresse eines Zeigers auf eine [**idirectxfileenumubject**](idirectxfileenumobject.md) -Schnittstelle, die das erstellte Enumeratorobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuweisung, dxfileerr \_ badfilefloatsize, dxfileerr \_ badfiletype, dxfileerr \_ badfileversion, dxfileerr \_ badresource, dxfileerr \_ badvalue, dxfileerr file \_ otfound, dxfileerr \_ resourcenotfound, dxfileerr \_ urlnotfound.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie diese Methode verwendet haben, verwenden Sie eine der idirectxfileenumubject-Methoden, um ein Datenobjekt abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfile](idirectxfile.md)
</dt> </dl>

 

 
