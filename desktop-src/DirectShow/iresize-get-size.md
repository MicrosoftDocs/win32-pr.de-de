---
description: Die get \_ size-Methode gibt die aktuelle Ausgabegröße und den Stretch-Modus zurück.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Iresize:: get_Size-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372717"
---
# <a name="iresizeget_size-method"></a>Iresize:: get \_ size-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_Size` Methode gibt die aktuelle Ausgabegröße und den Stretch-Modus zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piheight* \[ vorgenommen\]
</dt> <dd>

Empfängt die Höhe des Videos in Pixel.

</dd> <dt>

*piwidth* \[ vorgenommen\]
</dt> <dd>

Empfängt die Video Breite in Pixel.

</dd> <dt>

*PFLAG* \[ vorgenommen\]
</dt> <dd>

Empfängt ein Flag, das den streckungs Modus angibt. Informationen zu möglichen Werten finden Sie unter [**Größenänderung für Flags**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der Ausgabetyp nicht festgelegt wurde, sollte der Filter Standardwerte zurückgeben. Diese Werte können zur Entwurfszeit willkürlich ausgewählt werden.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**Iresize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




