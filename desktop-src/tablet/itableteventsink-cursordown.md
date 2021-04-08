---
description: Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'Itableteventsink:: Cursor down-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757056"
---
# <a name="itableteventsinkcursordown-method"></a>Itableteventsink:: Cursor down-Methode

Tritt auf, wenn der tablettstifttipp die digitalisierende Tablet-Oberfläche kontaktiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*CID* \[ in\]
</dt> <dd>

Der Bezeichner des Tablettstifts.

</dd> <dt>

*nserialnumber* \[ in\]
</dt> <dd>

Die Seriennummer des Tablettstifts.

</dd> <dt>

*cbpkt* \[ in\]
</dt> <dd>

Die Anzahl von Bytes in einem Tablettstift-Datenpaket.

</dd> <dt>

*pbpkt* \[ in\]
</dt> <dd>

Die Tablettstiftdaten, die den Ort angeben, an dem der Tablettstift das Tablet berührt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itableteventsink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




