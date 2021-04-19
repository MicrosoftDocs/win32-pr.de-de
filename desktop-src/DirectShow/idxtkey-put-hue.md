---
description: Die Put \_ Hue-Methode gibt den Hue-Wert an, für den der Schlüssel bestimmt wird. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ Hue ist.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: Idxtkey::p ut_Hue-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369644"
---
# <a name="idxtkeyput_hue-method"></a>Idxtkey::p UT \_ Hue-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Hue` Methode gibt den Farbton Wert an, auf den der Schlüssel festgelegt wird Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ Hue ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Der Farbton Wert, für den der Schlüssel angezeigt werden soll. Der gültige Bereich liegt zwischen 0 und 360.

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

 

 




