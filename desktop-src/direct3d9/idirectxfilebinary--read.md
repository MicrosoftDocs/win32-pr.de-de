---
description: Liest die Binärdaten. Veraltet.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Idirectxfilebinary:: Read-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050904"
---
# <a name="idirectxfilebinaryread-method"></a>Idirectxfilebinary:: Read-Methode

Liest die Binärdaten. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvData* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die gelesenen Daten empfängt.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt (in Bytes).

</dd> <dt>

*pcbread* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Ein Zeiger auf die Anzahl der tatsächlich gelesenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badvalue, dxfileerr \_ nomoredata.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfilebinary](idirectxfilebinary.md)
</dt> </dl>

 

 
