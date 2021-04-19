---
description: Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab. Veraltet.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Idirectxfiledata:: GetData-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350711"
---
# <a name="idirectxfiledatagetdata-method"></a>Idirectxfiledata:: GetData-Methode

Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szMember* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Members, für den die Daten abgerufen werden sollen. Geben Sie **null** an, um alle erforderlichen Elementdaten abzurufen.

</dd> <dt>

*pcbSize* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger zum Empfangen der ppvData-Puffergröße in Bytes.

</dd> <dt>

*ppvData* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Adresse eines Zeigers auf den Puffer, der die mit "szMember" verknüpften Daten empfangen soll. Wenn szMember den Wert **null** hat, wird ppvData so festgelegt, dass es auf einen Puffer verweist, der alle erforderlichen Elementdaten in einem zusammenhängenden Speicherblock enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badarraysize, dxfileerr \_ baddatareferenzierung, dxfileerr \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Daten für erforderliche Member eines Datenobjekts ab, aber keine Daten für optionale (untergeordnete) Member. Verwenden Sie [**idirectxfiledata:: getnextobject**](idirectxfiledata--getnextobject.md) zum Abrufen von untergeordneten Objekten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledata](idirectxfiledata.md)
</dt> <dt>

[**Idirectxfiledata:: getnextobject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
