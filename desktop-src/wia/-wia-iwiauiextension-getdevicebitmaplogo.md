---
description: Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Iwiauiextension:: getdevicebitmaplogo-Methode (wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348789"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>Iwiauiextension:: getdevicebitmaplogo-Methode

Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.

</dd> <dt>

*phbitmap* \[ vorgenommen\]
</dt> <dd>

Typ: **hBitmap \** _

Verweist auf einen Speicherort, der ein Handle für das bitmaplogo für das Gerät empfängt.

</dd> <dt>

_nMaxWidth * \[ in\]
</dt> <dd>

Typ: **ulong**

Gibt die gewünschte Breite der Bitmap an.

</dd> <dt>

*nmaxheight* \[ in\]
</dt> <dd>

Typ: **ulong**

Gibt die gewünschte Höhe der Bitmap an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




