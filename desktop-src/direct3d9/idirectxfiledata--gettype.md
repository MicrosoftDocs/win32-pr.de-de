---
description: Ruft die GUID der Objekt Vorlage ab. Veraltet.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Idirectxfiledata:: GetType-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132377"
---
# <a name="idirectxfiledatagettype-method"></a>Idirectxfiledata:: GetType-Methode

Ruft die GUID der Objekt Vorlage ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppGUID* \[ Out, retval\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \* \***

Adresse eines Zeigers, der die GUID der Objekt Vorlage empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledata](idirectxfiledata.md)
</dt> </dl>

 

 




