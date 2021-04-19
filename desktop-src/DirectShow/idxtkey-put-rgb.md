---
description: Die Put \_ RGB-Methode gibt die RGB-Farbe für den Schlüssel an. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: Idxtkey::p ut_RGB-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369128"
---
# <a name="idxtkeyput_rgb-method"></a>Idxtkey::p UT \_ RGB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_RGB` Methode gibt die RGB-Farbe für den Schlüssel an. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt die Farbe als hexadezimale Zahl mit dem Format 0xRRGGBB an, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.

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
</dt> <dt>

[**Idxtkey::p UT- \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




