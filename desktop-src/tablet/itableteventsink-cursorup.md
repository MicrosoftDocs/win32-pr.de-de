---
description: Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Itableteventsink:: Cursor Methode'
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
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218368"
---
# <a name="itableteventsinkcursorup-method"></a>Itableteventsink:: Cursor Methode

Tritt auf, wenn der Benutzer den Tablettstift von der tabletdigitalisiereroberfläche ausgelöst hat.

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

Die Tablettstiftdaten, die den Speicherort angeben, an dem der Tablettstift vom Tablet entfernt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

 

 




