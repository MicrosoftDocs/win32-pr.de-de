---
description: Ruft den Namen dieses ID3DXFileSaveData-Dateidatenknotens ab.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: ID3DXFileSaveData::GetName-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7aa6ef69a5296830b2f3bb992fb24ac23fa58adeeea629fd0e1bdeacf6173344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856649"
---
# <a name="id3dxfilesavedatagetname-method"></a>ID3DXFileSaveData::GetName-Methode

Ruft den Namen dieses [**ID3DXFileSaveData-Dateidatenknotens**](id3dxfilesavedata.md) ab.

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

Adresse eines Zeigers zum Empfangen des Namens dieses Dateidatenknotens. Wenn dieser Parameter **NULL ist,** gibt *puiSize* die Größe der Zeichenfolge zurück. Wenn szName auf gültigen Speicher verweist, wird der Name dieses Dateidatenknotens in szName bis zur Anzahl von Zeichen kopiert, die *von puiSize angegeben werden.*

</dd> <dt>

*puiSize* \[ in, out\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Zeiger auf die Größe der Zeichenfolge, die den Namen dieses Dateidatenknotens darstellt. Dieser Parameter kann NULL **sein,** wenn szName einen Verweis auf den Namen enthält. Dieser Parameter gibt die Größe der Zeichenfolge zurück, wenn szName NULL **ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Hinweise

Damit diese Methode erfolgreich ist, muss *szName* oder *puiSize* nicht NULL **sein.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
