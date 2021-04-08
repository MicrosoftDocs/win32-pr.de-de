---
description: Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: Itableteventsink::P ackets-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960177"
---
# <a name="itableteventsinkpackets-method"></a>Itableteventsink::P ackets-Methode

Tritt auf, wenn sich der Tablettstift auf dem Digitalisierer bewegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*cpkts* \[ in\]
</dt> <dd>

Die Anzahl der Pakete.

</dd> <dt>

*cbpkts* \[ in\]
</dt> <dd>

Die Größe des Paket Puffers.

</dd> <dt>

*pbpkts* \[ in\]
</dt> <dd>

Der Paket Puffer.

</dd> <dt>

*pnserialnumbers* \[ in\]
</dt> <dd>

Das Array der Seriennummer.

</dd> <dt>

*zid* 
</dt> <dd>

Der Bezeichner des Tablettstifts.

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

 

 




