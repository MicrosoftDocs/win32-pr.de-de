---
description: Greifen Sie auf die X-Dateidaten zu.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: ID3DXFileData::Lock-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520707"
---
# <a name="id3dxfiledatalock-method"></a>ID3DXFileData::Lock-Methode

Greifen Sie auf die X-Dateidaten zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Zeiger auf die Größe der X-Dateidaten.

</dd> <dt>

*ppData* \[ In\]
</dt> <dd>

Typ: **const \* \* VOID**

Adresse eines Zeigers zum Empfangen des Schnittstellenzeigers des [**Id3DXFileData-Dateidatenobjekts.**](id3dxfiledata.md) Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Der *ppData-Zeiger* ist nur während einer **ID3DXFileData::Lock ...** [**ID3DXFileData::Unlock-Sequenz.**](id3dxfiledata--unlock.md) Sie können mehrere Sperraufrufe tätigen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperraufrufe der Anzahl der Entsperraufrufe entspricht.

Da dateidaten nicht garantiert ordnungsgemäß an Bytegrenzen ausgerichtet sind, sollten Sie mit UNALIGNED-Zeigern auf *ppData* zugreifen.

Es wird nicht garantiert, dass zurückgegebene Parameterwerte aufgrund einer möglichen Dateibeschädigung gültig sind. Daher sollte Ihr Code die zurückgegebenen Parameterwerte überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
