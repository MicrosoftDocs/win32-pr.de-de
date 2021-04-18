---
description: Die get \_ RGB-Methode ruft die RGB-Farbe ab, nach der der Schlüssel abgerufen werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Idxtkey:: get_RGB-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368373"
---
# <a name="idxtkeyget_rgb-method"></a>Idxtkey:: get \_ RGB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_RGB` Methode ruft die RGB-Farbe ab, für die der Schlüssel abgerufen werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt die Farbe. Der zurückgegebene Wert ist eine hexadezimale Zahl im Format 0xRRGGBB, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.

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

[**Idxtkey:: get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




