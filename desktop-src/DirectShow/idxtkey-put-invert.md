---
description: Die Put \_ Invert-Methode gibt an, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: Idxtkey::p ut_Invert-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369485"
---
# <a name="idxtkeyput_invert-method"></a>Idxtkey::p UT \_ Invert-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Invert` Methode gibt an, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt einen booleschen Wert an. **True** gibt an, dass Pixel im überliegenden Bild in Bezug auf den Standard Vorgang invertiert werden. Wenn der Wert **false** ist, werden die Pixel im überliegenden Bild standardmäßig transparent gemacht.

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

 

 




