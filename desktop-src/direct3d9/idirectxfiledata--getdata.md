---
description: Ruft die Daten für einen der -Elemente des -Objekts oder die Daten für alle Member ab. Veraltet.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: IDirectXFileData::GetData-Methode (DXFile.h)
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
ms.openlocfilehash: 428bff1f3fd76cd7c4589d5084435f8a675ab0d73bf0ff02052b2212d2c2dea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728966"
---
# <a name="idirectxfiledatagetdata-method"></a>IDirectXFileData::GetData-Methode

Ruft die Daten für einen der -Elemente des -Objekts oder die Daten für alle Member ab. Veraltet.

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

*szMember* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Namen des Members, für den Daten abgerufen werden sollen. Geben Sie **NULL** an, um die Daten aller erforderlichen Member abzurufen.

</dd> <dt>

*layoutSize* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger zum Empfangen der ppvData-Puffergröße in Bytes.

</dd> <dt>

*ppvData* \[ out\]
</dt> <dd>

Typ: **\* \* void**

Adresse eines Zeigers auf den Puffer zum Empfangen der daten, die szMember zugeordnet sind. Wenn szMember **NULL** ist, wird ppvData so festgelegt, dass es auf einen Puffer verweist, der alle erforderlichen Memberdaten in einem zusammenhängenden Speicherblock enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDataReference, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die Daten für erforderliche Member eines Datenobjekts ab, jedoch keine Daten für optionale (untergeordnete) Member. Verwenden Sie [**IDirectXFileData::GetNextObject,**](idirectxfiledata--getnextobject.md) um untergeordnete Objekte abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
