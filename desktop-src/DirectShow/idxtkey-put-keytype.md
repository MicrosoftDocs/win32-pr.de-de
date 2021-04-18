---
description: Die Put \_ KeyType-Methode gibt den Schlüsseltyp an.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: Idxtkey::p ut_KeyType-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372331"
---
# <a name="idxtkeyput_keytype-method"></a>Idxtkey::p UT- \_ KeyType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_KeyType` Methode gibt den Typ des Schlüssels an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt den Schlüsseltyp an. Dieser Parameter muss einen der folgenden Enumerationswerte aufweisen.



| Wert             | BESCHREIBUNG                                           |
|-------------------|-------------------------------------------------------|
| dxtkey \_ RGB       | Chroma-Schlüssel. (Schlüssel für RGB-Wert.)                       |
| dxtkey \_ nicht rot    | Nicht-rote Taste. (Macht blaue und grüne Bereiche transparent.) |
| dxtkey- \_ Leuchtkraft | Der Schlüssel für die Leuchtkraft.                                        |
| dxtkey \_ Alpha     | Schlüssel nach Alpha Wert.                                   |
| dxtkey- \_ Farbton       | Schlüssel nach Farbton.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idxtkey-Schnittstelle**](idxtkey.md)
</dt> </dl>

 

 




