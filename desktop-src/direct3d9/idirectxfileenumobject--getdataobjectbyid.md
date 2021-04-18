---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Idirectxfileenduwbject:: getdataobjectbyid-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365067"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a>Idirectxfileendumuject:: getdataobjectbyid-Methode

Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rguid* \[ in\]
</dt> <dd>

Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Verweis auf die angeforderte GUID.

</dd> <dt>

*ppdataobj* \[ vorgenommen\]
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

[Idirectxfile-umubject](idirectxfileenumobject.md)
</dt> </dl>

 

 
