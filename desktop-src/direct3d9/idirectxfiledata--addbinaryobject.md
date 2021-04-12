---
description: Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Idirectxfiledata:: addbinaryobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219443"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>Idirectxfiledata:: addbinaryobject-Methode

Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Objekts. Geben Sie **null** an, wenn für das Objekt kein Name erforderlich ist.

</dd> <dt>

*pguid* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \***

Ein Zeiger auf die GUID, die das Objekt darstellt. Geben Sie **null** an, wenn das Objekt keine GUID benötigt.

</dd> <dt>

*szmimetype* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den MIME-Typ des Objekts.

</dd> <dt>

*pvData* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Daten des Objekts.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledata](idirectxfiledata.md)
</dt> <dt>

[**Idirectxfilebinary:: getmimetype**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
