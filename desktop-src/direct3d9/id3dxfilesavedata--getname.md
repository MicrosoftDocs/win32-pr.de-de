---
description: Ruft den Namen dieses ID3DXFileSaveData File Data-Knotens ab.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'ID3DXFileSaveData:: GetName-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050884"
---
# <a name="id3dxfilesavedatagetname-method"></a>ID3DXFileSaveData:: GetName-Methode

Ruft den Namen dieses [**ID3DXFileSaveData**](id3dxfilesavedata.md) File Data-Knotens ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**

Adresse eines Zeigers, der den Namen dieses Datei Daten Knotens empfängt. Wenn dieser Parameter **null** ist, gibt *puisize* die Größe der Zeichenfolge zurück. Wenn szName auf gültigen Speicher verweist, wird der Name dieses Datei Daten Knotens bis zu der Anzahl der Zeichen, die von *puisize* angegeben werden, in szName kopiert.

</dd> <dt>

*puisize* \[ in, out\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Größe der Zeichenfolge, die den Namen dieses Datei Daten Knotens darstellt. Dieser Parameter kann **null** sein, wenn szName einen Verweis auf den Namen bereitstellt. Dieser Parameter gibt die Größe der Zeichenfolge zurück, wenn szName **null** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Damit diese Methode erfolgreich ausgeführt werden kann, muss " *szName* " oder " *puisize* " nicht **null** sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
