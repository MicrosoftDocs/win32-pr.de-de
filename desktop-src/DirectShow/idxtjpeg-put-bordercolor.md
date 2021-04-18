---
description: Die Put \_ BorderColor-Methode gibt die Farbe des Rahmens um die Ränder des Abbild Musters an.
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: Idxtjpeg::p ut_BorderColor-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371012"
---
# <a name="idxtjpegput_bordercolor-method"></a>Idxtjpeg::p UT- \_ BorderColor-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_BorderColor` Methode gibt die Farbe des Rahmens um die Ränder des-Token für das Löschen an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BorderColor(
  [in] long newVal
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

[**Idxtjpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 




