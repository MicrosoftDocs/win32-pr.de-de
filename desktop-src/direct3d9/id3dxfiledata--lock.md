---
description: Greift auf die x-Datei Daten zu.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData:: Lock-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371925"
---
# <a name="id3dxfiledatalock-method"></a>ID3DXFileData:: Lock-Methode

Greift auf die x-Datei Daten zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Psize* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Größe der x-Datei Daten.

</dd> <dt>

*ppData* \[ in\]
</dt> <dd>

Typ: Konstante **void \* \***

Adresse eines Zeigers, mit dem der Schnittstellen Zeiger des [**ID3DXFileData**](id3dxfiledata.md) -Datei Datenobjekts empfangen werden soll. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Der *ppData* -Zeiger ist nur während der **ID3DXFileData:: Lock** ... [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) -Sequenz. Sie können mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe übereinstimmt.

Da es nicht garantiert wird, dass Datei Daten ordnungsgemäß mit Byte-Begrenzungen ausgerichtet werden, sollten Sie mit nicht ausgerichteten Zeigern auf *ppData* zugreifen.

Die Rückgabe von Parameterwerten ist aufgrund einer möglichen Datei Beschädigung nicht garantiert. Daher sollte der Code die zurückgegebenen Parameterwerte überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
