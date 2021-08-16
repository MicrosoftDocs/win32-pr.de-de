---
description: Die get \_ KeyType-Methode ruft den Typ des Schlüssels ab.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: IDxtKey::get_KeyType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cfb8930df859771f61406ebab9a1e7f60cfdf149eaf66eae23120bb7292ebf74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819474"
---
# <a name="idxtkeyget_keytype-method"></a>IDxtKey::get \_ KeyType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_KeyType` -Methode ruft den Typ des Schlüssels ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt einen der folgenden Enumerationswerte.



| Wert             | Beschreibung                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Schlüssel des Schlüssels" (Schlüssel für RGB-Wert.)                       |
| DXTKEY \_ NONRED    | Nicht ed-Schlüssel. (Macht blaue und grüne Bereiche transparent.) |
| DXTKEY \_ LUDOMINANZ | Leuchtdichteschlüssel.                                        |
| DXTKEY \_ ALPHA     | Schlüssel nach Alphawert.                                   |
| DXTKEY \_ HUE       | Schlüssel nach Farbton.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> </dl>

 

 




