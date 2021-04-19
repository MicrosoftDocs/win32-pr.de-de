---
description: Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird. Veraltet.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Idirectxfileobject:: GetId-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355177"
---
# <a name="idirectxfileobjectgetid-method"></a>Idirectxfileobject:: GetId-Methode

Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* \[ Out, retval\]
</dt> <dd>

Typ: **lpguid**

Zeiger auf eine GUID, um die Objekt-ID zu erhalten. Die-Funktion legt die GUID auf eine **null** -GUID fest, wenn das Objekt nicht über eine ID verfügt.

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

[Idirectxfileobject](idirectxfileobject.md)
</dt> </dl>

 

 




