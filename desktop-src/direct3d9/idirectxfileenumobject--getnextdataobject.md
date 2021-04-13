---
description: Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Idirectxfileenumubject:: getnextdataobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354227"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>Idirectxfileenumubject:: getnextdataobject-Methode

Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdataobj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoreobjects

## <a name="remarks"></a>Bemerkungen

Objekte der obersten Ebene sind immer Datenobjekte. Daten Verweis Objekte und binäre Objekte können nur untergeordnete Elemente von Datenobjekten sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfile-umubject](idirectxfileenumobject.md)
</dt> </dl>

 

 




