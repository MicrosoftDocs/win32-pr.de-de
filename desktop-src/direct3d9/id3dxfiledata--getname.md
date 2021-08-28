---
description: Ruft den Namen dieses Dateidatenobjekts ab.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: ID3DXFileData::GetName-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f98e20d5bfa5efdb756e414808cda2506fda56fdf417f54b658f17d0b5c9658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847930"
---
# <a name="id3dxfiledatagetname-method"></a>ID3DXFileData::GetName-Methode

Ruft den Namen dieses Dateidatenobjekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ In\]
</dt> <dd>

Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**

Adresse eines Zeigers zum Empfangen des Namens dieses Dateidatenobjekts. Wenn dieser Parameter **NULL ist,** gibt puiSize die Größe der Zeichenfolge zurück. Wenn szName auf gültigen Speicher verweist, wird der Name dieses Dateidatenobjekts bis zur Anzahl der von puiSize angegebenen Zeichen in szName kopiert.

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Zeiger auf die Größe der Zeichenfolge, die den Namen dieses Dateidatenobjekts darstellt. Dieser Parameter kann NULL **sein,** wenn szName einen Verweis auf den Namen enthält. Dieser Parameter gibt die Größe der Zeichenfolge zurück, wenn szName NULL **ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Damit diese Methode erfolgreich ist, muss szName oder *puiSize* nicht NULL **sein.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
