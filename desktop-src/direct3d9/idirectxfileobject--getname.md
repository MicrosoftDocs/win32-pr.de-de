---
description: Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab. Veraltet.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Idirectxfileobject:: GetName-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367361"
---
# <a name="idirectxfileobjectgetname-method"></a>Idirectxfileobject:: GetName-Methode

Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrinnamebuf* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, in den der Name des DirectX-Datei Objekts kopiert wird. Legen Sie diesen Wert auf **null** fest, wenn nur die Pufferlänge benötigt wird.

</dd> <dt>

*pdwbuschlen* \[ in, out\]
</dt> <dd>

Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Ein Zeiger auf ein DWORD, das die Länge des Puffers angibt, auf den pstrinnamebuf zeigt. Der Wert des pdwbuflen-Parameters wird in die Pufferlänge geändert, die für den Namen des Objekts erforderlich ist, auch wenn pstrinnamebuf **null** ist. In beiden Fällen gibt die Funktion dxfileerr \_ badvalue zurück, wenn der ursprüngliche Wert von pdwbuflen nicht so groß wie die Länge ist, die zum Speichern des Objekt namens benötigt wird.

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

[Idirectxfileobject](idirectxfileobject.md)
</dt> </dl>

 

 
