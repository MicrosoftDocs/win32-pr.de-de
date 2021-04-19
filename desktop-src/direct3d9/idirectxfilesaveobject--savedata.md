---
description: Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei. Veraltet.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Idirectxfilesaveobject:: SaveData-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364359"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>Idirectxfilesaveobject:: SaveData-Methode

Speichert ein Datenobjekt und seine untergeordneten Elemente in einer DirectX-Datei. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdataobj* \[ in\]
</dt> <dd>

Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)**

Zeiger auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das zu speichernde Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badarraysize, dxfileerr \_ badvalue.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfilesaveobject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




