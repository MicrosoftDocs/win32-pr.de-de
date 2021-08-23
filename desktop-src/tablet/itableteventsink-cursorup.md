---
description: Tritt ein, wenn der Benutzer den Tablettstift von der Tablettdigisiereroberfläche ausgelöst hat.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: ITabletEventSink::CursorUp-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 586f18750e832bad653a3df92d14efb41b39547ee532913ac52c986a9b5e137c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712130"
---
# <a name="itableteventsinkcursorup-method"></a>ITabletEventSink::CursorUp-Methode

Tritt ein, wenn der Benutzer den Tablettstift von der Tablettdigisiereroberfläche ausgelöst hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tcid* \[ In\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*cid* \[ in\]
</dt> <dd>

Der Bezeichner des Stifts.

</dd> <dt>

*nSerialNumber* \[ In\]
</dt> <dd>

Die Seriennummer des Stifts.

</dd> <dt>

*cbPkt* \[ In\]
</dt> <dd>

Die Anzahl der Bytes in einem Stiftdatenpaket.

</dd> <dt>

*pbPkt* \[ In\]
</dt> <dd>

Die Tablettstiftdaten, die die Position angeben, an der der Tablettstift vom Tablett entfernt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




